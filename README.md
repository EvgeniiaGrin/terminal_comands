# terminal_comands
1) Посмотреть где я

pwd 

2) Создать папку

mkdir test2022

3) Зайти в папку

cd test2022

4) Создать 3 папки

mkdir test_1 test_2 test_3
(base) MacBook-Pro:test2022 grinevgeniya$ ls -la
total 0
drwxr-xr-x   5 grinevgeniya  staff   160 20 май 10:57 .
drwxr-xr-x+ 92 grinevgeniya  staff  2944 20 май 10:53 ..
drwxr-xr-x   2 grinevgeniya  staff    64 20 май 10:57 test_1
drwxr-xr-x   2 grinevgeniya  staff    64 20 май 10:57 test_2
drwxr-xr-x   2 grinevgeniya  staff    64 20 май 10:57 test_3


5) Зайти в любоую папку

cd test_3
(base) MacBook-Pro:test_3 grinevgeniya$ 

6) Создать 5 файлов (3 txt, 2 json)

touch proba_1.txt proba_2.txt proba_3.txt proba_01.js proba_02.js
(base) MacBook-Pro:test_3 grinevgeniya$ ls -la
total 0
drwxr-xr-x  7 grinevgeniya  staff  224 20 май 11:00 .
drwxr-xr-x  5 grinevgeniya  staff  160 20 май 10:57 ..
-rw-r--r--  1 grinevgeniya  staff    0 20 май 11:00 proba_01.js
-rw-r--r--  1 grinevgeniya  staff    0 20 май 11:00 proba_02.js
-rw-r--r--  1 grinevgeniya  staff    0 20 май 11:00 proba_1.txt
-rw-r--r--  1 grinevgeniya  staff    0 20 май 11:00 proba_2.txt
-rw-r--r--  1 grinevgeniya  staff    0 20 май 11:00 proba_3.txt

7) Создать 3 папки

mkdir 111test 222test 333test
(base) MacBook-Pro:test_3 grinevgeniya$ 

8. Вывести список содержимого папки

(base) MacBook-Pro:test_3 grinevgeniya$ cd ../..
(base) MacBook-Pro:~ grinevgeniya$ cd test2022
(base) MacBook-Pro:test2022 grinevgeniya$ ls -la
total 0
drwxr-xr-x   5 grinevgeniya  staff   160 20 май 10:57 .
drwxr-xr-x+ 92 grinevgeniya  staff  2944 20 май 10:53 ..
drwxr-xr-x   2 grinevgeniya  staff    64 20 май 10:57 test_1
drwxr-xr-x   2 grinevgeniya  staff    64 20 май 10:57 test_2
drwxr-xr-x  10 grinevgeniya  staff   320 20 май 11:02 test_3

9) + Открыть любой txt файл

nano /proba_1.txt


  UW PICO 5.09                                        File: /proba_1.txt                                           
















^G Get Help        ^O WriteOut        ^R Read File       ^Y Prev Pg         ^K Cut Text        ^C Cur Pos         
^X Exit            ^J Justify         ^W Where is        ^V Next Pg         ^U UnCut Text      ^T To Spell        


10) + написать туда что-нибудь, любой текст.

(base) MacBook-Pro:/ grinevgeniya$ cat /Users/grinevgeniya/test2022/test_3/proba_2.txt
(base) MacBook-Pro:/ grinevgeniya$ cat >> /Users/grinevgeniya/test2022/test_3/proba_2.txt
ghfhsfsf
fasfjgfvs


0973634jh
kjsfhai

IUYIOP
gfjhs

fwlf-=32873eyh


11) + сохранить и выйти.

^C

12) Выйти из папки на уровень выше

cd ..

—
13) переместить любые 2 файла, которые вы создали, в любую другую папку.

(base) MacBook-Pro:test2022 grinevgeniya$ mv /Users/grinevgeniya/test2022/test_3/proba_1.txt /Users/grinevgeniya/test2022/test_2/proba_1.txt
(base) MacBook-Pro:test2022 grinevgeniya$ 


14) скопировать любые 2 файла, которые вы создали, в любую другую папку.

(base) MacBook-Pro:~ grinevgeniya$ cd test2022
(base) MacBook-Pro:test2022 grinevgeniya$ cp /Users/grinevgeniya/test2022/test_2/proba_1.txt test_1

15) Найти файл по имени

(base) MacBook-Pro:test2022 grinevgeniya$ find . -name "test"

16) просмотреть содержимое в реальном времени (команда grep) изучите как она работает.

nano /Users/grinevgeniya/test2022/test_2/proba_1.txt

grep -i fas /Users/grinevgeniya/test2022/test_3/proba_2.txt
fasfjgfvs

17) вывести несколько первых строк из текстового файла

(base) MacBook-Pro:test2022 grinevgeniya$ head -2 /Users/grinevgeniya/test2022/test_3/proba_2.txt
ghfhsfsf
fasfjgfvs


18) вывести несколько последних строк из текстового файла

(base) MacBook-Pro:test2022 grinevgeniya$ tail -5 /Users/grinevgeniya/test2022/test_3/proba_2.txt

IUYIOP
gfjhs

fwlf-=32873eyh

19) просмотреть содержимое длинного файла (команда less) изучите как она работает.

less /Users/grinevgeniya/test2022/test_3/proba_2.txt

20) вывести дату и время

(base) MacBook-Pro:test2022 grinevgeniya$ date
пятница, 20 мая 2022 г. 12:44:16 (+03)

=========

Задание *
1) Отправить http запрос на сервер.
http://162.55.220.72:5005/terminal-hw-request

curl http://162.55.220.72:5005/get_method?name=Evgeniia\&age=40

2) Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13

(base) MacBook-Pro:~ grinevgeniya$ cd /Users/grinevgeniya
(base) MacBook-Pro:~ grinevgeniya$ nano bash_script_mac.sh

#!/bin/bash

cd test2022
mkdir test_1 test_2 test_3
cd test_3
touch proba_1.txt proba_2.txt proba_3.txt proba_01.js proba_02.js
mkdir 111test 222test 333test
cd ../..
test2022
mv /Users/grinevgeniya/test2022/test_3/proba_1.txt /Users/grinevgeniya/test2022/test_2/proba_1.txt

bash bash_script_mac.sh


Termial. HW_2
 1. Сделать папку dir_1

mkdir dir_1
-------------------------------
 2. Зайти в папку dir_1

cd /Users/grinevgeniya/dir_1/
-------------------------------
 3. Создать папку inner_dir_1

 mkdir inner_dir_1

 4. Посмотреть где ты находишься

pwd
-------------------------------

 5. Находясь в папке dir_1 создать пустой текстовый файл tf_1.txt

touch tf_1.txt
-------------------------------

 6. Находясь в папке dir_1 через команду cat создать текстовый файл tf_2.txt со следующими строками:
- the first 1
- the second 2
- the third 3

-------------------------------
cat > tf_2.txt
- the first 1
- the second 2
- the third 3
^C
-------------------------------

 7. Зайти в папку inner_dir_1

cd /Users/grinevgeniya/dir_1/inner_dir_1/
-------------------------------

 8. Через cat сделать текстовый файл tf_3.txt  c любыми строками

cat > tf_3.txt
String 1
String 2
String 3
^C
-------------------------------

 9. Через cat добавить в текстовый файл tf_3.txt строку “the second 2”

cat >> tf_3.txt
the second 2
^C
-------------------------------

 10. Через cat добавить в текстовый файл tf_3.txt строку “the sec 2”

cat >> tf_3.txt
the sec 2
^C
-------------------------------

 11. Через cat добавить в текстовый файл tf_2.txt строку “the sec 3”

cat >> tf_2.txt
the sec 3
^C
-------------------------------

 12. Через cat добавить в текстовый файл tf_3.txt строку “the SeCoNd 2”

cat >> tf_3.txt
the SeCoNd 2
^C
-------------------------------

 13. Через cat добавить в текстовый файл tf_2.txt строку “the seConD 2”

cat >> tf_2.txt
the seConD 2
^C
-------------------------------

 14. Сделать текстовый файл tf_4.txt в котором будет 15 строк.

cat > tf_4.txt
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
^C
-------------------------------

 15. Сделать текстовый файл tF_5.txt в котором будет 13 строк.

cat > tF_5.txt
1
2
3
4
5
6
7
8
9
10
11
12
13
^C
-------------------------------

 16. Вывести список всех файлов в папке.

(base) MacBook-Pro:inner_dir_1 grinevgeniya$ ls -la
total 48
drwxr-xr-x  7 grinevgeniya  staff   224 28 май 09:43 .
drwxr-xr-x  8 grinevgeniya  staff   256 28 май 09:40 ..
-rw-r--r--@ 1 grinevgeniya  staff  6148 28 май 09:40 .DS_Store
-rw-r--r--  1 grinevgeniya  staff    30 28 май 09:43 tF_5.txt
-rw-r--r--  1 grinevgeniya  staff    23 28 май 09:38 tf_2.txt
-rw-r--r--  1 grinevgeniya  staff    53 28 май 09:37 tf_3.txt
-rw-r--r--@ 1 grinevgeniya  staff     3 28 май 09:41 tf_4.txt
-------------------------------

 17. Выйти из папки inner_dir_1

(base) MacBook-Pro:inner_dir_1 grinevgeniya$ cd ..
(base) MacBook-Pro:dir_1 grinevgeniya$ pwd
/Users/grinevgeniya/dir_1
-------------------------------


 18. Вывести содержимое файла tf_3.txt в терминал.

cat /Users/grinevgeniya/dir_1/inner_dir_1/tf_3.txt
String 1
String2
the second 2
the sec 2
the SeCoNd 2
-------------------------------


 19. Найти путь к файлу tf_4.txt

 find . -name "tf_4.txt"
./tf_4.txt
(base) MacBook-Pro:inner_dir_1 grinevgeniya$ 
-------------------------------


 20. Отчистить файл tf_4.txt от содержимого без удаления самого файла.

> tf_4.txt
-------------------------------

 21. Найти путь к файлам у которых есть  “tf” в названии.

ls | grep _tf_
ls -la
total 40
drwxr-xr-x  7 grinevgeniya  staff   224 28 май 09:43 .
drwxr-xr-x  8 grinevgeniya  staff   256 28 май 09:40 ..
-rw-r--r--@ 1 grinevgeniya  staff  6148 28 май 09:40 .DS_Store
-rw-r--r--  1 grinevgeniya  staff    30 28 май 09:43 tF_5.txt
-rw-r--r--  1 grinevgeniya  staff    23 28 май 09:38 tf_2.txt
-rw-r--r--  1 grinevgeniya  staff    53 28 май 09:37 tf_3.txt
-rw-r--r--@ 1 grinevgeniya  staff     0 28 май 13:58 tf_4.txt
-------------------------------

 22. Найти путь к файлам у которых есть  “tf” в названии и буквы в любом регистре.

grep -rnw -i "tf"
-------------------------------

 23. Найти строки в файлах где есть комбинация букв “sec” в текущей папке

grep -R sec /Users/grinevgeniya/dir_1/inner_dir_1
/Users/grinevgeniya/dir_1/inner_dir_1/tf_3.txt:the second 2
/Users/grinevgeniya/dir_1/inner_dir_1/tf_3.txt:the sec 2
/Users/grinevgeniya/dir_1/inner_dir_1/tf_2.txt:the sec 3
-------------------------------

 24. Найти строки в файлах где есть комбинация букв “sec” в любом регистре в текущей папке

grep -Ri sec /Users/grinevgeniya/dir_1/inner_dir_1
/Users/grinevgeniya/dir_1/inner_dir_1/tf_3.txt:the second 2
/Users/grinevgeniya/dir_1/inner_dir_1/tf_3.txt:the sec 2
/Users/grinevgeniya/dir_1/inner_dir_1/tf_3.txt:the SeCoNd 2
/Users/grinevgeniya/dir_1/inner_dir_1/tf_2.txt:the sec 3
/Users/grinevgeniya/dir_1/inner_dir_1/tf_2.txt:the seConD 2
-------------------------------

 25. Найти строки в файлах где есть только комбинация букв “sec” в текущей папке

grep -rnw sec *
tf_2.txt:1:the sec 3
tf_3.txt:4:the sec 2
-------------------------------

 26. Найти строки в файлах где есть только комбинация букв “sec” в любом регистре в текущей папке

grep -rnw -i sec *
tf_2.txt:1:the sec 3
tf_3.txt:4:the sec 2
-------------------------------

 27. Найти строки в файлах где есть комбинация букв “second” в текущей папке

grep -n "second" *
tf_3.txt:3:the second 2
-------------------------------

 28. Найти строки в файлах где есть комбинация букв “second” в любом регистре в текущей папке

grep -ni "second" *
tf_2.txt:2:the seConD 2
tf_3.txt:3:the second 2
tf_3.txt:5:the SeCoNd 2
-------------------------------

 29. Найти строки в файлах где есть комбинация букв “second” во всех папках ниже уровнем

grep -rnw "second" ./*/

 30. Найти только путь и название файла в строках которых есть комбинация букв “second” в текущей папке

grep -li second ./*
./tf_2.txt
./tf_3.txt
-------------------------------

 31. Найти все строки во всех файлах где нет комбинации “second”

grep -inv second ./*
./tF_5.txt:1:1
./tF_5.txt:2:2
./tF_5.txt:3:3
./tF_5.txt:4:4
./tF_5.txt:5:5
./tF_5.txt:6:6
./tF_5.txt:7:7
./tF_5.txt:8:8
./tF_5.txt:9:9
./tF_5.txt:10:10
./tF_5.txt:11:11
./tF_5.txt:12:12
./tF_5.txt:13:13
./tf_2.txt:1:the sec 3
./tf_3.txt:1:String 1
./tf_3.txt:2:String2
./tf_3.txt:4:the sec 2
-------------------------------

 32. Найти только название и путь к файлам где нет комбинации “second”

grep -L second *
tF_5.txt
tf_2.txt
tf_4.txt
-------------------------------

 33. Вывести в терминал 4 последних строк любого текстового файла

tail -4 tF_5.txt
10
11
12
13
-------------------------------

 34. Вывести в терминал 4 первые строки любого текстового файла.

head -4 tF_5.txt
1
2
3
4
-------------------------------

 35. Команда в одну строку. Создать папку и создать текстовый файл с содержимым.

mkdir /Users/grinevgeniya/dir_1/test_test | touch /test_test/test.txt | echo 'Hi, everybody!' > ./test.txt
-------------------------------

 36. Команда в одну строку. Переместить в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”

grep 'sec' *.txt > relocate.txt
-------------------------------

 37. Команда в одну строку. Скопировать в любую одну папку текстовые файлы у которых в содержимом есть слово “sec”

grep 'sec' *.txt >> relocate_1.txt
-------------------------------

 38. Команда в одну строку. Найти все строки c “sec” во всех текстовых файлах, скопировать и вставить эти строки в один новый созданный текстовый файл.

grep 'sec' *.txt >> new_file.txt
-------------------------------

 39. Команда в одну строку. Удалить текстовые файлы у которых в содержимом есть слово “sec”

grep 'sec' *.txt && rm 'sec' *.txt
-------------------------------

 40. Просто вывести в терминал строку “Good job!!”

echo 'Good job!'
Good job!
-------------------------------

