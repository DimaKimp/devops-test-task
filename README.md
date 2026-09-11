# DevOps Test Task — Hello World

Тестовое задание: приложение "Hello, World", упакованное в Docker и запущенное в Kubernetes.

## Что сделано

1. Веб-приложение "Hello, World" на Python + Flask, слушает порт **32777**
2. Docker-образ собран и опубликован на Docker Hub: `dimakimpinskiy/hello-world:1.0`
3. Развёрнут кластер Minikube (driver=docker)
4. Deployment `hello-world` с **2 репликами**
5. Service типа NodePort (`hello-world-service`) для доступа к подам
6. Проверка работы через `minikube service`

## Структура проекта

- `app.py` — приложение Flask
- `requirements.txt` — зависимости Python
- `Dockerfile` — сборка Docker-образа
- `deployment.yaml` — манифест Deployment (2 реплики)
- `service.yaml` — манифест Service (NodePort)
- `screenshots/` — скриншоты работы

## Технологии

- Python 3.12 + Flask 3.0
- Docker
- Kubernetes (Minikube v1.39)
- Docker Hub

## Ссылки

- Docker Hub: https://hub.docker.com/r/dimakimpinskiy/hello-world
- GitHub: https://github.com/твой_username/devops-test-task

## Как запустить локально

### Через Docker

```bash
docker run -d -p 32777:32777 dimakimpinskiy/hello-world:1.0
# Открыть http://localhost:32777