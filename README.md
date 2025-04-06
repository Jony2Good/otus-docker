# Основы работы с Docker

### Основная задача
Обернуть приложение в docker-образ и запушить его на Dockerhub
1. Создать минимальный сервис, который:
 - отвечает на порту 8000;
 - имеет http-метод: GET /health/ RESPONSE: {"status": "OK"}

2. Cобрать локально образ приложения в докер контенер под архитектуру AMD64
 - запушить образ в dockerhub


------------

### Результат

------------
## Задача № 1
------------

**Клонировать проект в локальный репозиторий**
 - git clone
 - в корневой директории найти файл .env.example исправить его на .env
 - выполнить команду *docker-compose build и после docker-compose up -d*

**Чтобы направить запрос на endpoint /health:**

- Заходим в контейнер nginx командой: *docker exec OtusDocker-nginx sh*
- Прописываем и выполняем команду: curl *http://localhost:8080/api/health*

Другой вариант:
- С помощью программ POSTMAN, Hoppscotch и д.р. направить запрос методом GET по маршруту http://127.0.0.1:8080/api/health

------------
## Задача № 2
------------

**Имя репозитория:**
 - atrem2023/otus-docker


**Тэг на Dockerhub:**
 - atrem2023/otus-docker:amd64

[Ссылка на репозиторий в DockerHub](https://hub.docker.com/repository/docker/atrem2023/otus-docker/tags/amd64/sha256:e12911a9ade123c6a2cc034bc438477c4fd7ea904ec4a064f206717018f5a75f)
