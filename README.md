# Задача 1
https://hub.docker.com/r/gregtimokhin/custom-nginx

# Задача 2
![image](https://github.com/user-attachments/assets/1e636d2b-1960-4d1b-93e2-1b3354a0eed4)
![image](https://github.com/user-attachments/assets/fb12346b-402e-4154-b85c-e7900c2aed27)
![image](https://github.com/user-attachments/assets/824e1bbd-04f3-4019-8066-b3943bcf527f)
![image](https://github.com/user-attachments/assets/d76bb22c-22f5-49e2-a941-ee8703f209d8)

# Задача 3
![image](https://github.com/user-attachments/assets/6ce1ad27-2372-4854-84f3-f8b7e0e3a9d2)
![image](https://github.com/user-attachments/assets/6d173c44-d7f6-4cf7-9483-71ca692b0bc8)

Контейнер остановился, потому что сочетание клавиш Ctrl+C зарезервировано под отправку сигнала SIGKILL в контейнер, которое при --sig-proxy==true вызывает отправку сигнала остановки SIGINT в главный процесс контейнера (https://docs.docker.com/reference/cli/docker/container/attach/)

Запуск контейнера в интерактивном режиме и установка nano в контейнере
![image](https://github.com/user-attachments/assets/077d1de9-3ddd-4f88-8f85-98f2d92bf8c0)

Редактирование конфига nginx
![image](https://github.com/user-attachments/assets/772ce74a-314a-47cb-bdc7-33a26a215c6c)

Перезагрузка nginx
![image](https://github.com/user-attachments/assets/ae62e273-7e2d-4da4-ac91-999ffe8d4c47)

Обращение к локальному хосту по curl (обратиться получается только по порту 81, т.к конфиг nginx был изменен)
![image](https://github.com/user-attachments/assets/04d72016-b641-4641-bb00-00ad7a564ac8)

Порт 8080 не используется в прослушиваемых адресах, поэтому вывод команды с grep будет пустым, т.к контейнер не опубликован на порту 127.0.0.1:8080, потому что на ВМ этого сделать нельзя. Чтобы отчасти эмулировать это, можно опубликовать контейнер так, как это было сделано в Задаче 2 (через маппинг портов 
![image](https://github.com/user-attachments/assets/c754187b-deb0-492b-8f92-ba53ca0d10d0)

Чтобы удалить запущенный контейнер, предварительно его не останавливая, необходимо использовать  















