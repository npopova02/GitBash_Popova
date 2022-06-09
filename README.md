# GitBash_Popova
Popova Nadya @qa_pn 
HW_1. The first part
Linux terminal (GitBash) commands
_________________________________

1) Посмотреть где я
	$ pwd
2) Создать папку
	$ mkdir group_30_free
3) Зайти в папку
	$ cd group_30_free
4) Создать 3 папки
	$ mkdir qa_1 qa_2 qa_3
5) Зайти в любоую папку
	$ cd qa_1
6) Создать 5 файлов (3 txt, 2 json)
	$ touch qq_1.txt qq_2.txt qq_3.txt qq_4.json qq_5.json
7) Создать 3 папки
	$ mkdir qa_4 qa_5 qa_6
8. Вывести список содержимого папки
	$ls -la (или ls или ls -l или ls -a)
9) + Открыть любой txt файл
	$ cat qq_1.txt
10) + написать туда что-нибудь, любой текст.
	$ cat >> qq_1.txt 
	В открывшемся режиме редактирования, написать любой текст 
11) + сохранить и выйти.
	Enter
	Cntr+C
12) Выйти из папки на уровень выше
	$ cd ..
—
13) переместить любые 2 файла, которые вы создали, в любую другую папку.
	$ mv qa_1/qq_2.txt qa_1/qq_3.txt qa_2/

14) скопировать любые 2 файла, которые вы создали, в любую другую папку.
	$ cp qa_2/qq_2.txt qa_2/qq_3.txt qa_1/

15) Найти файл по имени
	$ find -name "qq_2.txt"
	./group_30_free/qa_2/qq_2.txt

16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.
	$ tail -f qa_1/qq_1.txt

17) вывести несколько первых строк из текстового файла
	$ head -2 qa_1/qq_1.txt

18) вывести несколько последних строк из текстового файла
	$ tail -2 qa_1/qq_1.txt

19) просмотреть содержимое длинного файла (команда less) изучите как она работает.
	$ less qa_1/qq_1.txt

20) вывести дату и время
	$ date
=========

Задание *
1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request
$ curl 'http://162.55.220.72:5005/terminal-hw-request'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   283  100   283    0     0   2774      0 --:--:-- --:--:-- --:--:--  2801{
  "Intro": "Hello!! This is your the first response from server",
  "Tasks": {
    "Task_1": "Send the next URL in terminal: http://162.55.220.72:5005/get_method?name=(set_your_String)&age=(set_your_number)",
    "result": [
      "Your_String",
      "Your_number"
    ]
  }
}
$ curl 'http://162.55.220.72:5005/get_method?name=Nadya&age=30'
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100    23  100    23    0     0    261      0 --:--:-- --:--:-- --:--:--   261[
  "Nadya",
  "30"
]


2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13
#!/bin/bash
cd D:/qa_Course/group_30_free
mkdir qa_1 qa_2 qa_3
cd qa_1
touch qq_1.txt qq_2.txt qq_3.txt qq_4.json qq_5.json
mkdir qa_4 qa_5 qa_6
ls -la
mv qq_2.txt qq_3.txt ../qa_2
