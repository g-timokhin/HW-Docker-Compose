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

![image](https://github.com/user-attachments/assets/077d1de9-3ddd-4f88-8f85-98f2d92bf8c0)
![Снимок экрана (1511)](https://github.com/user-attachments/assets/72824c60-2c2d-4fa2-9649-21eed8c121ad)
Проблемы уже возникли на этапе перезагрузки nginx
![image](https://github.com/user-attachments/assets/ab95c098-6473-40d7-89af-1956b34c5cf4)
curl из контейнера и с хоста возвращает Connection refused, возвращение ошибки при вызове с хоста может объясняться тем, что после маппинга портов с помощью команды docker port, запрос перенаправляется в контейнер, где конфигурация nginx была изменена (однако она также может быть вызвана тем, что перезагрузка nginx в контейнере не прошла нормально)
![image](https://github.com/user-attachments/assets/3011a33d-aa6e-49b9-bcab-27315642936f)










