# Лабораторная работа 3: Docker, Docker Compose и Portainer

## Студент: Yakush Elizaveta

---

## Задача 1: Создание и публикация custom-nginx образа

### Установка Docker и Docker Compose
<img width="913" height="806" alt="Снимок экрана 2025-11-20 в 15 13 00" src="https://github.com/user-attachments/assets/36804abb-a67f-4209-9078-11179aaeedf6" />
<img width="882" height="587" alt="Снимок экрана 2025-11-20 в 15 14 48" src="https://github.com/user-attachments/assets/4a04664c-c2ec-4974-9011-87bc5b6a5f51" />
### ссылка на страницу моего репозитория https://hub.docker.com/repository/docker/elizansk1/custom-nginx/general
## Задача 2  Работа с контейнером custom-nginx:
<img width="1112" height="112" alt="Снимок экрана 2025-11-20 в 15 32 45" src="https://github.com/user-attachments/assets/bbb932f4-2f3f-46bd-b51a-e097e708ab16" />
<img width="1011" height="79" alt="Снимок экрана 2025-11-20 в 15 35 05" src="https://github.com/user-attachments/assets/50e15ea7-f4b0-4300-b729-383a78e6e756" />
<img width="1007" height="312" alt="Снимок экрана 2025-11-20 в 15 36 08" src="https://github.com/user-attachments/assets/ce916c93-1b64-49b4-bb86-d90f7e2c605c" />
## Задача 3:
### Узнаём, как подключиться к контейнеру
Используем docker help:
docker help attach
Команда docker attach позволяет подключиться к контейнеру, чтобы видеть его stdout, stderr и при необходимости вводить команды через stdin.
<img width="605" height="187" alt="Снимок экрана 2025-11-20 в 15 38 59" src="https://github.com/user-attachments/assets/c9a19d15-8d9d-4003-8a21-208c46d45b73" />
<img width="1029" height="67" alt="Снимок экрана 2025-11-20 в 15 40 05" src="https://github.com/user-attachments/assets/305e4da2-4fed-4b37-89e5-992e2e1c424a" />
Почему контейнер остановился:
Контейнер работает, пока главный процесс внутри него активен.
При нажатии Ctrl-C, процесс nginx завершился → контейнер остановился.
<img width="821" height="388" alt="Снимок экрана 2025-11-20 в 15 42 54" src="https://github.com/user-attachments/assets/f20f913c-39b8-4d3e-bc2f-684c75618333" />
<img width="428" height="18" alt="Снимок экрана 2025-11-20 в 16 25 45" src="https://github.com/user-attachments/assets/0be8f5e4-f29f-4d7c-ab6b-f48de330cfcf" />

## Задача 4:

## Задача 5:

