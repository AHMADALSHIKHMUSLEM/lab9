# Отчет по лабораторной работе №9

----

# Тема:
## Текстовой редактор vi

----

## Российский Университет Дружбы Народов

### Факультет Физико-Математических и Естественных Наук

*Дисциплина: Операционные системы*

Студент: Алших Маслем Ахмад 

Группа: НФИБД-02-20

Москва, 2021г.

----

### Цель работы

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.


### Последовательность выполнения работы
1. Ознакомиться с теоретическим материалом.
2. Ознакомиться с редактором vi.
3. Выполнить упражнения, используя команды vi.

----

### Ход работы:

#### Задание 1. Создание нового файла с использованием vi.

1. Создал каталог с именем ~/work/os/lab06.
2. Перешел во вновь созданный каталог.
3. Вызвал vi и создал файл hello.sh

![1c8cee76db312aa4d.png](https://ic.wampi.ru/2021/05/22/1c8cee76db312aa4d.png)

4. Нажав клавишу i, ввел следующий текст:
#!/bin/bash
HELL=Hello
function hello {
LOCAL HELLO=World
echo $HELLO
}
echo $HELLO
hello

![2c7cc2083854a4746.png](https://ic.wampi.ru/2021/05/22/2c7cc2083854a4746.png)

5. Нажав клавишу Esc, перешел в командный режим, после завершения ввода текста.

![3198a63c4263abe80.png](https://ic.wampi.ru/2021/05/22/3198a63c4263abe80.png)

6. Нажал «:» для перехода в режим последней строки и внизу экрана появилось приглашение в виде двоеточия.

![45536e874814df6e5.png](https://ic.wampi.ru/2021/05/22/45536e874814df6e5.png)

7. Нажал w (записать) и q (выйти), а затем нажал клавишу Enter для сохранения текста и завершения работы.

![5be72a07cba2262d1.png](https://ic.wampi.ru/2021/05/22/5be72a07cba2262d1.png)

8. Сделал файл исполняемым. 

![6635bc867e53d4c11.png](https://ic.wampi.ru/2021/05/22/6635bc867e53d4c11.png)

#### Задание 2. Редактирование существующего файла.

1. Вызвал vi на редактирование файла.

![7eaac5e9552175adf.png](https://ic.wampi.ru/2021/05/22/7eaac5e9552175adf.png)

2. Установил курсор в конец слова HELL второй строки.

![8c1710d2dc972e0c5.png](https://ic.wampi.ru/2021/05/22/8c1710d2dc972e0c5.png)

3. Перешел в режим вставки и заменил на HELLO. Нажал Esc для возврата в командный режим.

![8c1710d2dc972e0c5.png](https://ic.wampi.ru/2021/05/22/8c1710d2dc972e0c5.png)
4. Установил курсор на четвертую строку и стёр слово LOCAL.

![10d1ea18acc054a081.png](https://ic.wampi.ru/2021/05/22/10d1ea18acc054a081.png)

5. Перешел в режим вставки и набрал следующий текст: local, нажала Esc для возврата в командный режим.

![11b53f5cc489f34d6c.png](https://ic.wampi.ru/2021/05/22/11b53f5cc489f34d6c.png)

6. Установил курсор на последней строке файла. Вставил после неё строку, содержащую следующий текст: echo $HELLO.

![12ebe100f260c3774a.png](https://ic.wampi.ru/2021/05/22/12ebe100f260c3774a.png)

7. Нажал Esc для перехода в командный режим.

8. Удалил последнюю строку.

![135942da2b58a7837c.png](https://ic.wampi.ru/2021/05/22/135942da2b58a7837c.png)

9. Ввел команду отмены изменений u для отмены последней команды.

![142ca97724e6613710.png](https://ic.wampi.ru/2021/05/22/142ca97724e6613710.png)
10. Ввел символ «:» для перехода в режим последней строки. Записал произведённые изменения и вышел из vi. 

![152a89e9ae01e454de.png](https://ic.wampi.ru/2021/05/22/152a89e9ae01e454de.png)

----

### Вывод

Познакомился с операционной системой Linux, получил практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

----

### Библиография

[Работа с редактором vi](https://docs.altlinux.org/ru-RU/archive/2.3/html-single/junior/alt-docs-extras-linuxnovice/ch02s10.html)

## Ответы на контрольные вопросы:

1.Краткая характеристика режимов работы редактора vi:
* командный режим — предназначен для ввода команд редактирования и навигации по редактируемому файлу;
* режим вставки — предназначен для ввода содержания редактируемого файла;
* режим последней (или командной) строки — используется для записи изменений
в файл и выхода из редактора.
2. Выйти из редактора, не сохраняя произведённые изменения, можно используя клавиши «:q!» в командном режиме.
3. Краткую характеристика команд позиционирования:
* 0 (ноль) — переход в начало строки;
* $ — переход в конец строки;
* G — переход в конец файла;
* n G — переход на строку с номером n.
4. Для редактора vi словом является: пробел; буквы, находящиеся между двумя пробелами.
5. Из любого места редактируемого файла перейти в конец файла можно с помощью клавишы G и курсора вниз, а в начало – курсор вверх.
6. Краткая характеристика основных групп команд редактирования:
Вставка текста
* а — вставить текст после курсора;
* А — вставить текст в конец строки;
* i — вставить текст перед курсором;
* n i — вставить текст n раз;
* I — вставить текст в начало строки.
Вставка строки
* о — вставить строку под курсором;
* О — вставить строку над курсором.  Удаление текста
* x — удалить один символ в буфер;
* d w — удалить одно слово в буфер;
* d $ — удалить в буфер текст от курсора до конца строки;
* d 0 — удалить в буфер текст от начала строки до позиции курсора;
* d d — удалить в буфер одну строку;
* n d d — удалить в буфер n строк.  Отмена и повтор произведённых изменений
* u — отменить последнее изменение;
* . — повторить последнее изменение.
Копирование текста в буфер
* Y — скопировать строку в буфер;
* n Y — скопировать n строк в буфер;
* y w — скопировать слово в буфер.
Вставка текста из буфера
* p — вставить текст из буфера после курсора;
* P — вставить текст из буфера перед курсором.  Замена текста
* c w — заменить слово;
* n c w — заменить n слов;
* c $ — заменить текст от курсора до конца строки;
* r — заменить слово;
* R — заменить текст.
Поиск текста
* / текст — произвести поиск вперёд по тексту указанной строки символов текст;
* ? текст — произвести поиск назад по тексту указанной строки символов текст. 7. Чтобы заполнить строку символами $ можно использовать клавиши ni(вставить текст n раз).
8. Отменить некорректное действие, связанное с процессом редактирования, можно с помощью клавиши «.».
9. Характеристика основных групп команд режима последней строки:
Копирование и перемещение текста
* : n,m d — удалить строки с n по m;
* : i,j m k — переместить строки с i по j, начиная со строки k;
* : i,j t k — копировать строки с i по j в строку k;
* : i,j w имя-файла — записать строки с i по j в файл с именем имя-файла.
Запись в файл и выход из редактора
* : w — записать изменённый текст в файл, не выходя из vi;
* : w имя-файла — записать изменённый текст в новый файл с именем имяфайла;
* : w ! имя-файла — записать изменённый текст в файл с именем имяфайла;
* : w q — записать изменения в файл и выйти из vi;
* : q — выйти из редактора vi;
* : q ! — выйти из редактора без записи;
* : e ! — вернуться в командный режим, отменив все изменения, произведённые со времени последней записи.
10. Определить, не перемещая курсора, позицию, в которой заканчивается строка, можно используя клавишу $ (переход в конец строки).
11. Опции редактора vi позволяют настроить рабочую среду. Для задания опций
используется команда set (в режиме последней строки):
* : set all — вывести полный список опций;
* : set nu — вывести номера строк;
* : set list — вывести невидимые символы;
* : set ic — не учитывать при поиске, является ли символ прописным или
строчным.
Если вы хотите отказаться от использования опции, то в команде set перед именем опции надо поставить no.
12. Определить режим работы редактора vi можно по последней командной строке.
13. Взаимосвязь режимов работы редактора vi:
«Командный режим»     -     «Режим вставки»
                          \                             /
                 «Режим командной строки»
