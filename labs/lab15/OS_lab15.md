﻿# <a name="титульный-лист"></a>**Титульный лист**
РОССИЙСКИЙ УНИВЕРСИТЕТ ДРУЖБЫ НАРОДОВ

Факультет физико-математических и естественных наук




**Лабораторная работа 15**

По дисциплине "Операционные системы"






Выполнил:

Студент группы НПМбв-01-19

Студенческий билет №: 1032187017

Кушнирчук Дарья Вадимовна

Руководитель: Валиева Татьяна Рефатовна











Москва 2023

# <a name="цель-работы"></a>**Цель работы**
Приобретение практических навыков работы с именованными каналами.
# <a name="начало-работы"></a>**Начало работы**
Я изучил приведенные в тексте программы server.c и client.c. Взяв данные примеры за образец, напишем аналогичные программы, внеся следующие изменения.

- Для этого создадим *common.h, server.c, client.c, Makefile*.
  ![](Aspose.Words.9a12dc13-5cd2-46c5-9664-80405ed44487.001.png)

  *Рисунок 1*
- Запишем в файл common.h следующий код:

  ![](Aspose.Words.9a12dc13-5cd2-46c5-9664-80405ed44487.002.jpeg)

  *Рисунок 2*
- Запишем в файл server.c следующий код:

  ![](Aspose.Words.9a12dc13-5cd2-46c5-9664-80405ed44487.003.jpeg)

  *Рисунок 3*
- Запишем в файл client.c следующий код:

  ![](Aspose.Words.9a12dc13-5cd2-46c5-9664-80405ed44487.004.jpeg)

  *Рисунок 4*
- Запишем в файл Makefile следующий код:

  ![](Aspose.Words.9a12dc13-5cd2-46c5-9664-80405ed44487.005.jpeg)

  *Рисунок 5*
- Проверим на работоспособность.

  ![](Aspose.Words.9a12dc13-5cd2-46c5-9664-80405ed44487.006.jpeg)

  *Рисунок 6*


  ![](Aspose.Words.9a12dc13-5cd2-46c5-9664-80405ed44487.007.png)
# <a name="вывод"></a>**Вывод**
Мы приобрели практические навыки работы с именованными каналами.
# <a name="контрольные-вопросы"></a>**Контрольные вопросы**
1. У именованных каналов есть идентификатора канала, а у неименованных его нет
1. Возможно создание неименованного канала из командной строки, но только с созданием временного канала с индикатором.
1. Да. При помощи mknod.
1. #include int fd[2]; 

   pipe(fd); 

   /\* возвращает 0 в случае успешного завершения, -1 - в случае ошибки;\*/ Это значит, что функция возвращает два файловых дескриптора: fd[0] и fd[l]
1. #include <sys/types.h>

   #include <sys/stat.h>

   int mkfifo(const char \*pathname, mode\_t mode);
1. При чтении меньшего числа байтов, чем находится в канале или FIFO, возвращается требуемое число байтов, остаток сохраняется для последующих чтений. При чтении большего числа байтов, чем находится в канале или FIFO, возвращается доступное число байтов. Процесс, читающий из канала, должен соответствующим образом обработать ситуацию, когда прочитано меньше, чем требуется в программе
1. Запись числа байтов, меньшего числа битов у канала или FIFO, в случае, когда несколько процессов одновременно записывают в канал, порции данных от этих процессов не перемешиваются. При записи большего числа байтов, чем это позволяет канал или FIFO, вызов write(2) блокируется до освобождения занятой нами до этого памяти.
1. Могут ли два и более процессов читать или записывать в канал? Ответ: Да. Если у buff достаточное количество памяти.
1. Функция записывает length памяти из буфера buffer в файл, определенный дескриптором файла fd. Эта операция чисто ‘двоичная’ и без буферизации. При единице возвращает действительное число байтов. При -1 сообщение об ошибке.
1. Интерпретирует номер ошибки, передаваемый в функцию в качестве аргумента — errornum, в понятное для человека текстовое сообщение (строку). Откуда берутся эти ошибки? Ошибки эти возникают при вызове функций стандартных Си-библиотек. То есть хорошим тоном программирования будет — использование этой функции в паре с другой, и если возникнет ошибка, то пользователь или программист поймет, как исправить ошибку, прочитав сообщение функции strerror. Возвращенный указатель ссылается на статическую строку с ошибкой, которая не должна быть изменена программой. Дальнейшие вызовы функции strerror перезапишут содержание этой строки. Интерпретированные сообщения об ошибках могут различаться, это зависит от платформы и компилятора.
