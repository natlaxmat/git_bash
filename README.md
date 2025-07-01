# git_bash
**Работа с git и bash**

Task 1

01. *created the bash1.txt file                  Предварительно создайте файл bash1.txt, в который вы будете добавлять выполненные команды.
02. cd ~                                         Открыть домашнюю директорию через терминал  
03. pwd                                          Определить имя папки, в которой вы находитесь
04. mkdir test1                                  Создать внутри этой папки каталог с именем test1
05. cd test1                                     Перейти в папку test1
06. touch 1 2 3                                  Создать файл 1,2 и 3 внутри каталога test1
07. ls                                           Проверить содержимое каталога test1
08. cd ~                                         Перейти в домашнюю директорию
09. mkdir test2                                  Создать папку test2 внутри домашней директории
10. rmdir test2                                  Удалить папку test2
11. rm test1/2                                   Удалить файл 2 из папки test1
12. mkdir test3                                  Создать папку в домашней директории test3 и добавить в нее два файла
    touch ~/test3/1 ~/test3/2
13.	rm ~/test3                                   Удалить папку test3 
14. mkdir test4                                  Создать папку test4 в домашней директории
15. mv test1/1 test/3 test4/                     Переместить файлы 1 и 3 из папки test1 в папку test4 
16. echo "line" >> test1/1                       Добавить в файл 1 три строки со словами line
    echo "line" >> test1/1
    echo "line" >> test1/1	
-or-
    echo -e "line\nline\nline" >> test1/1
17. cat test1/1                                  Посмотреть содержимое файла 1
18.	echo "line" >> test1/3                       Добавьте в файл 3 три строки со словами line
    echo "line" >> test1/3
	  echo "line" >> test1/3
-or-
    echo -e "line\nline\nline" >> test1/3
19. cat test1/1 test1/3                          Просмотрите содержимое двух файлов (1 и 3) сразу
20. nano test1/1                                 Используя один из редакторов замените все строки в файле 1 
  	line -> hello
  	line -> wonderful
	  line -> world

Task 2

01. *created the bash2.txt file                            Предварительно создайте файл bash2.txt, в который вы будете добавлять выполненные команды.
02. cd ~                                                   Зайти в домашнюю директорию через терминал
03. mkdir test3                                            Создать папку test 3
04. echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/4           Добавить в папку test 3 три файла 4, 5 и 6, в каждом из которых должно быть по 4 строки row1, row2, row3, row4
    echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/5
    echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/6
05. grep "row2" ~/test3/5                                  Найдите строку row2 в файле 5
06. grep "row" ~/test3/*                                   Найдите строку row в папке test3
07. grep -c "row" ~/test3/6                                Посчитайте сколько строк с содержимым row в файле 6
08. find ~/test3 -name "5"                                 Найдите файл 5 внутри папки test3
09. find . -name "5" -delete                               Используя команду find, удалите файл 5
10. echo "test" > ~/test3/4                                Используя команду echo, добавьте слово test в файл 4 (без сохранения содержимого)
11. sed 's/test/fail/g' ~/test3/4                          Замените слово test в файле 4 на fail
12. echo "test" >> ~/test3/4                               Добавьте в файл 4 слово test так, чтобы сохранилось содержимое
13. ps aux                                                 Просмотрите все процессы для юзеров не только в консоли, которые происходят в системе
-or-
	  tasklist (для Windows)
14. kill 666                                               Убейте процесс 666 в консоли (можно не убивать, а просто написать команду)  
-or-
	  taskkill /PID 666 /F (для Windows)          
15. ping rusau.net                                         Узнайте доступность ресурса rusau.net, используя ping
16. ping -c 5 rusau.net                                    Отправьте 5 пакетов на сайт rusau.net
17. curl https://petstore.swagger.io/v2/pet                Используя GET и команду curl, получите информацию о зарегистрированных питомцах с любым статусом на https://petstore.swagger.io/ 
    /findByStatus?status=available,pending,sold    
18. curl -X POST "https://petstore.swagger.io/v2/user"     Используя POST и команду curl, создайте нового пользователя на https://petstore.swagger.io/
    -H "accept: application/json" 
	  -H "Content-Type: application/json"
	  -d "{\"id\":98765,
  	\"username\":\"nat_test_user\",
	  \"firstName\":\"Nat\",
	  \"lastName\":\"Tester\",
	  \"email\":\"nat@example.com\",
    \"password\":\"mySecurePass123\",
	  \"phone\":\"123456789\",
	  \"userStatus\":1}"
