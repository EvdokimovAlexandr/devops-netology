**Ответ на вопрос №1:** Исходя из вывода командры "type cd" cd - это встроенная в bash команда. Представить ее в виде внешней программы сложно, непонятно как вычислять домашний каталог  
**Ответ на вопрос №2:** grep -с <some_string> <some_file>  
**Ответ на вопрос №3:** Init  
**Ответ на вопрос №4:** ls not-exists-file 2> /dev/pts/X, где X - номер терминальной сессии  
**Ответ на вопрос №5:** Одновременно не получится, т.к. для вывода требуются минимальное время, а если имелось в виду в одну строку, то это: cat test-file | grep last > new-file  
C учетом комментария преподавателя решение будет такое:  
![Terminal answer 5](../raw/img.png)
**Ответ на вопрос №6:** Да, получится  
**Ответ на вопрос №7:** К создания дескриптора №5 и перенаправление его вывод в stdout, будет выведено слово netology, потому что вывод потока №5 перенаправлен в stdout   
**Ответ на вопрос №8:** (dir && ls —ppp) 3>&1 1>&2 2>&3 | wc -l  
**Ответ на вопрос №9:** переменные текущего процесса bash, вместо $$ можно подставить PID процесса.  
**Ответ на вопрос №10:**   /proc/<PID>/cmdline - содержит команды выполненные при запуске процесс с целевым PID, /proc/<PID>/exe - файл, содержащий символьную ссылку на текущий путь выполняемой инструкции процесс PID.   
**Ответ на вопрос №11:** cat /proc/cpuinfo | grep sse  
**Ответ на вопрос №12:** При удаленном подключении по ssh tty не выделяется 
**Ответ на вопрос №13:**  ctrl-z bg переносит процесс в screen, в другом сеансе достаточно набрать reptyr <PID>
**Ответ на вопрос №14:** Перезаписывает файл, работает с sudo  потому что это отдельная программа /usr/bin/tee, а echo - это часть оболочки bash 