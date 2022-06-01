# Linux terminal (GitBash) commands

1.Посмотреть где я:
  > pwd

2.Создать папку:
  > mkdir hw1

3.Зайти в папку:
  > cd hw1

4.Создать 3 папки
  > mkdir hw2 hw3 hw4

5.Зайти в любоую папку:
  > cd hw2

6.Создать 5 файлов (3 txt, 2 json):
  > touch file1.txt file2.txt file3.txt file4.json file5.json

7.Создать 3 папки:
  > mkdir hw5 hw6 hw7

8.Вывести список содержимого папки:
  > ls -la

9.Открыть любой txt файл:
  > vim file1.txt

10.Написать туда что-нибудь, любой текст
  > в открывшемся текстовом редакторе vim (из п.9) нажать латинскую кнопку "i
  > мы окажемся в режиме "INSERT", набираем любой текст

11.Сохранить и выйти
  > выйти из режима "INSERT" с помощью клавиши ESC, ввести :wq (сохранить и выйти)

12.Выйти из папки на уровень выше:
  > cd ..
13.Переместить любые 2 файла, которые вы создали, в любую другую папку:
  > mv {file1.txt file2.txt} hw6/

14.Скопировать любые 2 файла, которые вы создали, в любую другую папку:
  > cp {file4.json file5.json} hw6/

15.Найти файл по имени:
  > find . -name "file1.txt"

16.Просмотреть содержимое в реальном времени (команда grep) изучите как она работает:
  > tail -f file1.txt

17.Вывести несколько первых строк из текстового файла:
  > head -2 file1.txt

18.Вывести несколько последних строк из текстового файла:
  > tail -2 file1.txt

19.Просмотреть содержимое длинного файла (команда less) изучите как она работает:
  > less file1.txt, для выхода из режима просмотра нажать клавишу q

20.Вывести дату и время:
  > date

# Задание 
## Отправить http запрос на сервер.
http162.55.220.725005terminal-hw-request

> 1.  отправляем запрос: curl http://162.55.220.72:5005/terminal-hw-request
>     получаем ответ: {"Intro":"Hello!! This is your the first response from server","Tasks":{"Task_1":"Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)","result":["Your_String","Your_number"]}}

> 2.  изменяем запрос: curl "http://162.55.220.72:5005/get_method?name=NaN&age=111"
>     получаем ответ: ["NaN","111"]

# Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

> 1.  touch script.txt
> 2.  cat >> script.txt

> #!/bin/bash

> cd hw1
> mkdir hw2 hw3 hw4
> cd hw2
> touch file1.txt file2.txt file3.txt file4.json file5.json
> mkdir hw5 hw6 hw7
> ls -la
> mv file1.txt file2.txt hw6/

> 3.  энтер, а затем ctrl + c
> 4.  ./script.txt