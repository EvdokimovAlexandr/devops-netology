**Ответ на вопрос №1:**  
![Sec answer 1](Pass.PNG)  
**Ответ на вопрос №2:**  
![Sec answer 2](GoogleAuth.PNG)  
**Ответ на вопрос №3:**  
добавил самоподписанный сертификат:  
sudo openssl req -x509 -nodes -days 365 -new -keyout /etc/ssl/private/apache-selfsigned.key -out /etc/ssl/certs/apache-selfsigned.pem  
проверил пусть к сертификату и ключу в файле default-ssl.conf  
создал жесткую ссылку на файл настроек ssl в папку sites-enabled:  
sudo ln default-ssl.conf ../sites-enabled/default-ssl.conf  
включил ssl в apache:
sudo a2enmod ssl
перезапустил apache, загрузился сайт https://localhost (до этого пробросил порт 443)  
![Sec answer 3](apache_ssl.PNG)  
**Ответ на вопрос №4:**  
![Sec answer 4](testssl.PNG)  
**Ответ на вопрос №5:**  
![Sec answer 5](ssh_by_key.PNG)  
**Ответ на вопрос №6:**  
Переименовал файл ключа в id_rsa_new  
Добавил в ssh agent новый ключ:  
ssh-add ~\.ssh\id_rsa_new  
Добавил файл [config](config)  
Подключился по имени:  
![Sec answer 6](ssh_by_new_key.PNG)  
**Ответ на вопрос №7:**  
Собрал tcpdump 100 пакетов в файл [0001.pcap](0001.pcap)  
![Sec answer 7](tcpdump.PNG)  
Открыл полученный файл в wireshark:  
![Sec answer 7_1](wireshark.PNG)  
**Ответ на вопрос №8:**  
22/tcp - ssh  
80/tcp - http  
9929/tcp - nrip-echo  
31337/tcp - tcpwrapped  
![Sec answer 8](Nmap.PNG)  
**Ответ на вопрос №9:**  
Установил ufw, закрыл все входящие соединения открыл порты 22,80,443.  
Включил ufw, ssh не отвалился web сервер доступен  
![Sec answer 7](ufw.PNG)  
