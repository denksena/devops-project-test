# Effective Mobile — DevOps Test Assignment

## Стек технологий
- Python 3.12 (http.server)
- nginx 1.27
- Docker
- Docker Compose

## Архитектура
Client → nginx:80 → backend:8080

Запрос от пользователя приходит на nginx (порт 80), nginx проксирует его на backend (порт 8080). Backend недоступен снаружи — только внутри docker-сети.

## Запуск

```bash
git clone https://github.com/denksena/devops-project-test.git
cd devops-project-test
docker compose up -d --build
```

## Проверка

```bash
curl http://localhost
```

Ожидаемый ответ:
Hello from Effective Mobile!

## Остановка

```bash
docker compose down
```
