## Домашняя работа Git Bash №1
1. Создать папку;
```	
mkdir testgit1
```
2. Зайти в папку;
```	
cd testgit1
```
3. Создать 3 папки;
```	
mkdir test1 test2 test3
```
4. Зайти в любую папку;
```	
cd test1
```
5. Создать 5 файлов (3 txt, 2 json);
```	
touch 1_txt_file.txt 2_txt_file.txt 3_txt_file.txt 1_json_file.json 2_json_file.json
```
6. Создать 3 папки;
```	
mkadir file1 file2 file3
```
7. Вывести список содержимого папки;
```	
ls -la
```
8. Открыть любой txt файл;
```	
vim 1_txt_file.txt
```
9. Написать туда что-нибудь, любой текст;
```	
"i" welcome to my world
```
10. Сохранить и выйти;
```	
"esc" :wq
```
11. Выйти из папки на уровень выше;
```	
cd ..
```
12. Переместить любые 2 файла, которые вы создали, в любую другую папку;
```	
mv 1_json_file.json 2_json_file.json file1
```
13. Скопировать любые 2 файла, которые вы создали, в любую другую папку;
```	
cp 1_txt_file.txt 2_txt_file.txt file1/
```
14. Найти файл по имени;
```	
find ./ -type f -name "1_json_file.json"
```
15. Просмотреть содержимое в реальном времени (команда grep);
```
grep -i insert HW/HW_GitBash.txt
tail -f HW/HW_GitBash.txt
```
16. Вывести несколько первых строк из текстового файла;
```	
cat 1_txt_file.txt | sed -n 1,2p
```
17. Вывести несколько последних строк из текстового файла;
```	
cat 1_txt_file.txt | sed -n 6,7p
```
18. Просмотреть содержимое длинного файла (команда less);
```	
less 1_txt_file.txt
```
19. Вывести дату и время;
```	
date
```
20. Отправить http запрос на сервер;
```	
curl -p 'http://162.55.220.72:5005/object_info_3?name=Vadim&age=32&salary=1000'
```
21. Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13;
```	
touch myscript.sh
vim myscript.sh

#!/bin/bash
cd file_script
mkdir test1 test2 test3
cd test1
touch file1.txt file2.txt file3.txt file4.json file5.json
mkdir test4 test5 test6
ls -la
mv file4.json file5.json test4

chmod +x ./myscript.sh
./myscript.sh
```
____
## Домашняя работа Git Bash №2
1. На локальном репозитории сделать ветки для:- Postman – Jmeter – CheckLists - Bag Reports – SQL – Charles - Mobile testing;
```	
git checkout –b Postman
git checkout –b Jmeter
git checkout –b CheckLists
git checkout –b Bag Reports
git checkout –b SQL
git checkout –b Charles
git checkout –b Mobile testing
```
2. Запушить все ветки на внешний репозиторий;
```	
git push --set-upstream origin Postman Jmeter CheckList BagReports SQL Charles MobileTesting
```
3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта;
```	
touch Structure.txt
```
4. Запушить структуру багрепорта на внешний репозиторий;
```
git push
```
5. Вмержить ветку Bag Reports в Main;
```	
git checkout master
git merge BagReports
git checkout BagReports
```
6. Запушить main на внешний репозиторий;
```	
git push -u origin BagReports
```
7. В ветке CheckLists набросать структуру чек листа;
```	
git checkout CheckLists
touch Structure2
```
8. Запушить структуру на внешний репозиторий;
```	
git add Structure2
git commit -m "Structure2"
git push
```
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main;
```	
git checkout master
git merge CheckLists
git checkout CheckLists
```
10. Синхронизировать Внешнюю и Локальную ветки Main;
```	
git fetch origin
git reser --hard origin/master
git clean -f –d
```
