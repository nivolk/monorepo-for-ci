# Simple Microservices Monorepo Example

Этот репозиторий демонстрирует **минимальную структуру монорепозитория** для тестирования CI/CD сборки нескольких микросервисов через Docker.

## Структура

- `service1/Dockerfile`
- `service2/Dockerfile`
- ...

В каждом сервисе — **простейший Dockerfile**, который выводит тестовую строку.

## Зачем это нужно?

- Для проверки работы CI/CD pipeline (например, GitHub Actions matrix build).
- Для отладки автоматической сборки и публикации Docker-образов из монорепозитория.

## Быстрый старт (локально)

```bash
docker build -t test1 ./service1
docker run --rm test1
# Вывод: Hello from microservice!
