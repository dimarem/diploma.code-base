# Momo Store aka Пельменная №2

<img width="900" alt="image" src="https://user-images.githubusercontent.com/9394918/167876466-2c530828-d658-4efe-9064-825626cc6db5.png">

## Локальный запуск

```bash
docker compose up
```

## Устройство репозитория

1. Приложение разделено на две части: backend (Go) и frontend (js, Vue).
2. Перед релизом каждая часть упаковывается в docker-контейнер. См. Dockerfile в каждой из директорий.
3. Создание образов осуществляется в Gitlab, после чего они публикуются в Nexus: [std-046-13-diploma-front](https://nexus.praktikum-services.tech/#browse/browse:std-046-13-diploma-front) и [std-046-13-diploma-back](https://nexus.praktikum-services.tech/#browse/browse:std-046-13-diploma-back). См. .gitlab-ci.yml в корне проекта и в каждой из директорий.
4. Публикация и версионирования helm-чартов происходит в инфраструктурном репозитории.

Инфраструктурный репозиторий доступен по [этой ссылке](https://gitlab.praktikum-services.ru/std-046-13/momo-store-infra).
