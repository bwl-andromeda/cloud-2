# Дипломная работа - Облачное хранилище MyCloud

## [Техническое задание](https://github.com/netology-code/fpy-diplom/blob/main/README.md)

## 🛠 Стэк технологий.

Python v.3.10+, NodeJS v.18+, PostgreSQL v.14+.
Django, React, Redux, etc.

## Инструкция для развертывания данного проекта для dev разработки:
- Создать .env файл.
- Установить docker-engine для вашей ОС. Рекомендуется использоваться семейство UNIX-подобных систем. (Пример для установки на Ubuntu 22.04 LTS - https://docs.docker.com/engine/install/ubuntu/)

#### .env файл:
В нем должны указываться такие значения:
- DJANGO_SECRET_KEY = ... (Сгенерировать нужно с помощью manage.py)
- POSTGRES_USER= ... (имя пользователя базы данных postgresql)
- POSTGRES_DB = django_db (нужно использовать именно это значение т.к. на нем завязаны все настройки server/settings.py для backend сервиса)
- POSTGRES_PASSWORD = ... (Пароль для пользователя базы данных postgresql)
- REACT_APP_API_URL = ... (Для dev-версии проекта рекомендую использовать http://localhost:8000 , для сервера IP сервера с 8000 портом)

#### После записи .env файла:
```
docker compose up --build
```

И вуаля , вы развернули проект!
