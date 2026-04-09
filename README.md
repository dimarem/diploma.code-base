# Дипломная работа: Momo Store aka Пельменная №2

<img width="900" alt="image" src="https://storage.yandexcloud.net/diploma-image-bucket/landing.png">

## Ссылки на ресурсы

- [Momo Store](https://momostore-std-046-13.ru/)
- [Инфраструктурный репозиторий](https://gitlab.praktikum-services.ru/std-046-13/momo-store-infra)
- [Репозиторий артефактов сборки для frontend](https://nexus.praktikum-services.tech/#browse/browse:std-046-13-diploma-front)
- [Репозиторий артефактов сборки для backend](https://nexus.praktikum-services.tech/#browse/browse:std-046-13-diploma-back)
- [Репозиторий helm-чартов для frontend](https://nexus.praktikum-services.tech/#browse/browse:std-046-13-diploma-helm-front)
- [Репозиторий helm-чартов для backend](https://nexus.praktikum-services.tech/#browse/browse:std-046-13-diploma-helm-back)

## Использованные технологии в проекте

- Gitlab
- Kubernetes
- ArgoCD
- Helm
- Terraform
- CLI Yandex
- Ресурсы облачной платформы Yandex

Приложение запущено под управлением Kubernetes на одном узле с 4 CPU и 8 ГБ RAM.

Для поддержки HTTPS используется [Yandex Certificate Manager](https://yandex.cloud/ru/docs/certificate-manager/).

Для хранения и раздачи статики используется [Yandex Object Storage](https://yandex.cloud/ru/docs/storage/).

Больше подробносте в инфраструктурном репозитории.

## Чек-лист задания

Код хранится в GitLab с использованием любого git-flow ✅
В проекте присутствует .gitlab-ci.yml, в котором описаны шаги сборки ✅
Артефакты сборки (бинарные файлы, docker-образы или др.) публикуются в систему хранения (Nexus или аналоги) ✅
Артефакты сборки версионируются ✅
Написаны Dockerfile'ы для сборки Docker-образов бэкенда и фронтенда ✅
Бэкенд: бинарный файл Go в Docker-образе ✅
Фронтенд: HTML-страница раздаётся с Nginx ✅
В GitLab CI описан шаг сборки и публикации артефактов ✅
В GitLab CI описан шаг тестирования ✅
В GitLab CI описан шаг деплоя ✅
Развёрнут Kubernetes-кластер в облаке ✅
Kubernetes-кластер описан в виде кода, и код хранится в репозитории GitLab ✅
Конфигурация всех необходимых ресурсов описана согласно IaC ✅
Состояние Terraform'а хранится в S3 ✅
Картинки, которые использует сайт, или другие небинарные файлы, необходимые для работы, хранятся в S3 ✅
Секреты не хранятся в открытом виде ✅
Написаны Kubernetes-манифесты для публикации приложения ✅
Написан Helm-чарт для публикации приложения ✅
Helm-чарты публикуются и версионируются в Nexus ✅
Приложение подключено к системам логирования и мониторинга ✅
Есть дашборд, в котором можно посмотреть логи и состояние приложения ✅

---

## Локальный запуск

```bash
docker compose up
```
