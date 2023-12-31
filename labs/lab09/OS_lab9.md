﻿# <a name="титульный-лист"></a>**Титульный лист**
РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ

Факультет физико-математических и естественных наук




**Лабораторная работа 9**

По дисциплине "Операционные системы"






Выполнил:

Студент группы НПМбв-01-19

Студенческий билет №: 1032187017

Кушнирчук Дарья Вадимовна

Руководитель: Валиева Татьяна Рефатовна











Москва 2023

# <a name="цель-работы"></a>**Цель работы**
Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.
# <a name="начало-работы"></a>**Начало работы**
## <a name="xc8b3f3fd86afca6034f5298a8c0008a531294f7"></a>**Задание 1. Создание нового файла с использованием vi**
1. Создадим каталог с именем *~/work/os/lab06*.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.001.png)

   *Рисунок 1*
1. Перейдем во вновь созданный каталог.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.002.png)

   *Рисунок 2*
1. Вызовем vi и создайте файл *hello.sh* vi hello.sh

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.003.png)

   *Рисунок 3*
1. Нажмем клавишу *i* и вводите следующий текст:

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.004.png)

   *Рисунок 4*
1. Нажмем клавишу *Esc* для перехода в командный режим после завершения ввода текста.
1. Нажмем *:* для перехода в режим последней строки и внизу нашего экрана появится приглашение в виде двоеточия.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.005.png)

   *Рисунок 5*
1. Нажмем *w (записать)* и *q (выйти)*, а затем нажмем клавишу *Enter* для сохранения вашего текста и завершения работы.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.006.png)

   *Рисунок 6*
1. Сделаем файл исполняемым chmod +x hello.sh

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.007.png)

   *Рисунок 7*
## <a name="xda48bb01b5cbf0776af20974bad0747e65537be"></a>**Задание 2. Редактирование существующего файла**
1. Вызовем vi на редактирование файла vi ~/work/os/lab06/hello.sh.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.008.jpeg)

   *Рисунок 8*
1. Установите курсор в конец слова *HELL* второй строки.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.009.png)

   *Рисунок 9*
1. Перейдите в режим вставки и замените на *HELLO*. Нажмите *Esc* для возврата в командный режим

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.010.png)

   *Рисунок 10*
1. Установите курсор на четвертую строку и сотрите слово *LOCAL*.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.011.png)

   *Рисунок 11*
1. Перейдите в режим вставки и наберите следующий текст: *local*, нажмите *Esc* для возврата в командный режим.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.012.png)

   *Рисунок 12*
1. Установите курсор на последней строке файла. Вставьте после неё строку, содержащую следующий текст: echo $HELLO.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.013.png)

   *Рисунок 13*
1. Нажмите *Esc* для перехода в командный режим.
1. Удалите последнюю строку.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.014.png)

   *Рисунок 14*
1. Введите команду отмены изменений *u* для отмены последней команды.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.015.png)

   *Рисунок 15*
1. Введите символ *:* для перехода в режим последней строки. Запишите произведённые изменения и выйдите из vi.

   ![](Aspose.Words.ef2cb88b-fb86-4e5a-94aa-207de1ba98d2.016.png)

   *Рисунок 16*
# <a name="вывод"></a>**Вывод**
Мы познакомились с операционной системой Linux. Получили практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.
# <a name="контрольные-вопросы"></a>**Контрольные вопросы**
1. Редактор vi имеет три режима работы: 
   - *командный режим* — предназначен для ввода команд редактирования и навигации по редактируемому файлу;
   - *режим вставки* — предназначен для ввода содержания редактируемого файла;
   - *режим последней (или командной) строки* — используется для записи изменений в файл и выхода из редактора.
1. Набрать символ *q (или q!)*, если требуется выйти из редактора без сохранения.
1. Команды позиционирования: 
   - *0* (ноль) — переход в начало строки;
   - *$* — переход в конец строки;
   - *G* — переход в конец файла;
   - *n G* — переход на строку с номером n
1. Набор символов, которые указываются после команды vi.
1. *0* - переход в начало строки, *$* - переход в конец строки
1. Команды редактирования
   - Вставка текста
     - *а* — вставить текст после курсора; 
     - *А* — вставить текст в конец строки; 
     - *i* — вставить текст перед курсором; 
     - *n i* — вставить текст n раз; 
     - *I* — вставить текст в начало строки.
   - Вставка строки
     - *о* — вставить строку под курсором;
     - *О* — вставить строку над курсором
   - Удаление текста
     - *x* — удалить один символ в буфер;
     - *d w* — удалить одно слово в буфер; 
     - *d $* — удалить в буфер текст от курсора до конца строки; 
     - *d 0* — удалить в буфер текст от начала строки до позиции курсора;
     - *d d* — удалить в буфер одну строку;
     - *n d d* — удалить в буфер n строк.
   - Отмена и повтор произведенных изменений
     - *u* — отменить последнее изменение; 
     - *.* — повторить последнее изменение.
   - Копирование текста в буфер
     - *Y* — скопировать строку в буфер; 
     - *n Y* — скопировать n строк в буфер; 
     - *y w* — скопировать слово в буфер.
   - Вставка текста из буфера 
     - *p* — вставить текст из буфера после курсора; 
     - *P* — вставить текст из буфера перед курсором.
   - Замена текста
     - *c w* — заменить слово; 
     - *n c w* — заменить n слов; 
     - *c $* — заменить текст от курсора до конца строки; 
     - *r* — заменить слово; 
     - *R* — заменить текст.
   - Поиск текста
     - */* текст — произвести поиск вперёд по тексту указанной строки символов текст; 
     - *?* текст — произвести поиск назад по тексту указанной строки символов текст.
1. *y* (скопировать) > *p* (вставить)
1. *u* - отменить последнее изменение;
1. Опции редактора vi позволяют настроить рабочую среду. Для задания опций используется команда set (в режиме последней строки):
   - : set all — вывести полный список опций;
   - : set nu — вывести номера строк; 
   - : set list — вывести невидимые символы;
   - : set ic — не учитывать при поиске, является ли символ прописным или строчным. Если вы хотите отказаться от использования опции, то в команде *set* перед именем опции надо поставить *no*.
1. Команды позиционирования 
   - *0* (ноль) — переход в начало строки; 
   - *$* — переход в конец строки; 
   - *G* — переход в конец файла; 
   - *n G* — переход на строку с номером n.
1. : set all — вывести полный список опций;
1. Указывается в левом нижнем углу.
