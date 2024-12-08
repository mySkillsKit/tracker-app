# tracker-app

## Запуск приложения Tracker с помощью файла docker-compose.yml (frontendApp + backendApp + postgres)

- Клонируем проект на свой ПК https://github.com/mySkillsKit/tracker-app.git
- Запускаем приложение [Docker Desktop](https://www.docker.com/products/docker-desktop/);

- Запускаем терминал в папке `/tracker-app`:
- В терминале выполнить команду:
- создать сеть:

 ```shell
docker network create traccar-network
```

- запуск:

```shell
docker compose up -d
```

- В докере будет 3 приложения:
- Backend App -> ```http://localhost:8082```
- Frontend App -> ```http://localhost:3000```
- Database Postgres 16 -> ```http://localhost:5432```

![file 2024-12-08 в 19.20.20.png](file%202024-12-08%20%D0%B2%2019.20.20.png)

## Подключение к базе данных через DBeaver

```
jdbc:postgresql://localhost:5432/traccar
      POSTGRES_DB: traccar
      POSTGRES_USER: postgres
      POSTGRES_PASSWORD: postgres
```

![file 2024-12-08 в 19.22.45.png](file%202024-12-08%20%D0%B2%2019.22.45.png)
![file 2024-12-08 в 19.25.53.png](file%202024-12-08%20%D0%B2%2019.25.53.png)

## Зарегистрировать нового пользователя

![file 2024-12-08 в 19.24.33.png](file%202024-12-08%20%D0%B2%2019.24.33.png)
![file 2024-12-08 в 19.24.57.png](file%202024-12-08%20%D0%B2%2019.24.57.png)
![file 2024-12-08 в 19.25.21.png](file%202024-12-08%20%D0%B2%2019.25.21.png)

## Удалить приложение

```shell
docker compose down
```

## remote url ngrok macos

```shell
brew install --cask ngrok
```

- https://ngrok.com/ зарегистрироваться и получить authtoken

```shell
https://dashboard.ngrok.com/get-started/your-authtoken
```

```shell
ngrok config add-authtoken 2YYlAAQoSfHj0P4kpt
```

- запустить ngrok

```shell
ngrok http http://localhost:3000
```

- Теперь вы можете протестировать свое приложение!

```shell
https://cbfb-62-4-43-37.ngrok-free.app
```
