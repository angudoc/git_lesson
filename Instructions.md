# Инструкция для работы в Маркдаун

## Выделение текста
Чтобы выделить текст курсивом, необходимо обрамить его звездочками (*) или знаком нижнего подчеркивания (_) *Вот так* или _Вот так_

Чтобы выделить текст полужирным, необходимо обрамить его двумя (*) или двойными нижними подчеркиваниями (__) **Вот так** или __Вот так__

Альтернативные способы выделения текста курсивом и полужирным нужны для того, чтобы мы могли совмещать оба этих способа. Напимер, _текст может быть выделен курсивом и при этом быть **полужирным**_

Зачёркнутый текст   ~~Зачеркнутый текст~~

Подчеркнутый текст <u>Подчеркнутый текст</u>

## Списки
Чтобы добавить ненумерованные списки необходимо пункты выделить (*), например вот так
* Элемент 1
* Элемент 2
* Элемент 3
* Элемент 4

Чтобы добавить нумерованные списки необходимо пункты пронумеровать, например вот так
1. Элемент
2. Элемент
3. Элемент
## Работа с изображениями

Чтобы вставить изображение в текст необходимо написать следующее:
![Привет, это доктор](doctor.jpg)

## Цитаты
> Первый уровень цитирования
>>Второй уровень 
>>>Третий уровень
>
> Продолжение основной цитаты

## WEB ссылки
Текст [пример ссылки](http:/example.com "всплывающая подсказка")

### Cпособ поместить ссылку в Markdown — заключить её в угловые скобки.
<https://gb.ru/media/code/>

### Чтобы оформить ссылкой часть текста, используется синтаксис: [текст](ссылка). Можно сделать всплывающую подсказку при наведении курсора. Для этого в круглых скобках после ссылки нужно поставить пробел и написать текст подсказки в кавычках.

[Gikbranes Media](https://gb.ru/media/) без подсказки

[Gikbranes Media](https://gb.ru/media/ "Всплывающая подсказка") с подсказкой

## Чекбоксы

* [x] Отмеченный пункт

* [ ] Неотмеченный пункт


## Вставка кода (code)
Функция `print (x)` выводит содержимое переменной ```x```.
```
#include <studio.h>
int main() {
   printf("Hello, World!");
   return 0;
}
```

	let x = 50;
	let y = 4;
	console.log(x + y);

### Если обрамлять код тремя обратными апострофами, то после первой тройки можно указать язык программирования — тогда Markdown правильно подсветит элементы кода.
```python
if x > 0:
	print (x)
else:
	print ('Hello, World!')
```

```c
#include <stdio.h>
int main() {
   printf("Hello, World!");
   return 0;
}
```

```javascript
let x = 12;
let y = 6;
console.log(x + y);
```

## Работа с таблицами
### Столбцы разделяются вертикальными линиями |, а строка с шапкой отделяется от остальных дефисами -? количество которых не ограничено

|Столбец 1|Столбец 2|Столбец 3|
|-|--------|---|
|Длинная запись в первом столбце|Запись в столбце 2|Запись в столбце 3|
|Кртк зпс| |Слева нет записи|

### Чтобы выровнять весь столбец по правому краю, в строке с дефисами сразу после дефисов можно поставить двоеточие :. Чтобы выровнять содержимое по центру, надо поставить двоеточия с обеих сторон.
|Столбец 1|Столбец 2|Столбец 3|
|:-|:-:|-:|
|Равнение по левому краю|Равнение по центру|Равнение по правому краю|
|Запись|Запись|Запись|

# Подсказка по GIT

## Создание репозитория: 
```
sh
```

## Подготовка репозитория: 
```
git init
```

## Создание коммитов

## Добавление изменений в коммиты
``` 
git add 
```

Для добавления изменения в коммиты выполняется команда *git add*
Чтобы использовать команду необходимо ввести  *git add <File>*

## Просмотр состояния репозитория:
``` 
git status
```

## Создание коммитов:
``` 
git commit -m "Message"
```

## Просмотр истории коммитов:
``` 
git log
```
## Просмотр истории в одну строку для каждого коммита:
```
git log --oneline
```
## Сравнение изменений в коммитах: 
```
git diff
```
## Откат изменений:
### При необходимости отменить последние изменения, которые еще не были закоммичены,  используется команда *git checkout* для файлов или *git restore* для отмены изменений в рабочем каталоге
``` 
git checkout -- <file>
``` 
```
git restore -- <file>
```
## Ветвление и слияние

### Cоздать новую ветку и переключиться на нее:
``` 
git checkout -b <branch_name>
```

### Переключиться на уже существующую ветку:
``` 
git checkout <branch_name>
```

## Переключиться на самую актуальную версию
```
git checkout master
```
## Работа с удаленными репозиториями
### Основные команды и последовательность
1. Делаем fork (клон) интересующего нас репозитория.
2. Мы делаем clone (клонирование) для нашей версии этого репозитория.
3. Мы создаем ветку с предполагаемыми изменениями.
4. Производим все изменения только в этой ветке.
5. Отправляем эти изменения на свой аккаунт (push).
```
git remote add origin https://github.com/angudoc/git_lesson.git
git branch -M main
git push -u origin main
```
Все последующие изменения также отправляем, используя команду
```
git push -u origin main
```
6. Если случайно не удалось связать свой аккаунт на Github с Git, меняем SSH-keygen 
```
ssh-keygen -t rsa -b 4096 -C "angudoc@gmail.com"
```
и удаляем origin
```
 git remote remove origin       
 ```
   затем заново повторяем команды из **пункта 5.**

7. В окне на GitHub появляется возможность отправить pull request.

## Заключение
Создадим одну новую ветку, затем третью и четвертую