# Momo Store aka Пельменная №2

<img width="900" alt="image" src="https://user-images.githubusercontent.com/9394918/167876466-2c530828-d658-4efe-9064-825626cc6db5.png">

## Локальный запуск

```bash
docker compose up
```

## Устройство репозитория

1. Приложение разделено на две части: backend (Go) и frontend (js, Vue).
2. Каждая часть упаковывается в docker-контейнер. См. Dockerfile в каждой из директорий.
3. Создание образов осуществляется в Gitlab, после чего они публикуются в Nexus. См. .gitlab-ci.yml в корне проекта и в каждой из директорий.
