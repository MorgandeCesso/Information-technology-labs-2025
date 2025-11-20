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
файл /etc/nginx/conf.d/default.conf был отредактирован 
<img width="382" height="176" alt="Снимок экрана 2025-11-20 в 16 58 02" src="https://github.com/user-attachments/assets/04de3c81-7866-41d2-9dcc-a1bcafdb4fa8" />
<img width="666" height="444" alt="Снимок экрана 2025-11-20 в 17 01 44" src="https://github.com/user-attachments/assets/74df6827-7721-44d2-96e6-b0a22cbad7da" />
<img width="686" height="111" alt="Снимок экрана 2025-11-20 в 17 36 49" src="https://github.com/user-attachments/assets/75aad104-1b6f-42d3-a6dc-7cd742a8a2ef" />
<img width="445" height="23" alt="Снимок экрана 2025-11-20 в 18 29 48" src="https://github.com/user-attachments/assets/b2f8cbb1-be64-4b9a-bd70-2ff09cea7e48" />
## Задача 4:
<img width="1092" height="915" alt="Снимок экрана 2025-11-20 в 18 20 45" src="https://github.com/user-attachments/assets/0e303db9-6263-4e5a-bd4d-099c8efe88a3" />
## Задача 5:
Во время выполенения столкнулась с ошибкой в файле compose.yaml. Из за того что в  image: portainer/portainer-ce:latest стоит портейнер latest - тоесть последняя версия, присутсвуют ошибки при работе с Docker 29 версии. Решение нашла на https://github.com/orgs/portainer/discussions/12926
<img width="722" height="446" alt="image" src="https://github.com/user-attachments/assets/36588ad3-6e4a-4196-a69d-a13e8c4c841f" />
<img width="704" height="432" alt="image" src="https://github.com/user-attachments/assets/ceb107da-2890-46b5-99a8-8b49efbcaf51" />
<img width="702" height="524" alt="image" src="https://github.com/user-attachments/assets/42079eef-1677-416f-8864-7050d666103f" />
<img width="2834" height="1720" alt="image" src="https://github.com/user-attachments/assets/8ab9d453-e0df-4d36-aec0-e45951af3ecc" />
<img width="2826" height="1738" alt="image" src="https://github.com/user-attachments/assets/6d34a96c-984c-4191-8dc7-36e91961c305" />
<img width="3136" height="2084" alt="image" src="https://github.com/user-attachments/assets/775abf0d-4800-4653-aca2-28e56d734a21" />
<img width="539" height="48" alt="Снимок экрана 2025-11-20 в 19 13 26" src="https://github.com/user-attachments/assets/12ac5279-7c37-476e-ae51-1ccc142f4797" />
был удален docker-compose.yaml файл, при выполении команды docker compose up -d произошла ошибка, потому что файл compose.yaml внутри раздела include требует наличие docker-compose.yaml. Предложения от терминало не поступило(логично что нужно создать docker-compose.yaml)

<img width="2102" height="382" alt="image" src="https://github.com/user-attachments/assets/281d3e76-8930-4be4-829a-b8ff48ee65cf" />

 Далее при попытке выполнить комманду docker down также была ошибка
 
<img width="1162" height="126" alt="image" src="https://github.com/user-attachments/assets/552df1ce-ae35-45d3-bb98-5e8d67e41433" />

После этого было удаление по compose.

<img width="2226" height="332" alt="image" src="https://github.com/user-attachments/assets/45bf4728-f2e8-476a-a6b8-a8eaa13bf3d2" />








