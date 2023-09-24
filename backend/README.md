[![.github/workflows/main.yml](https://github.com/zaylyalow/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/zaylyalow/kittygram_final/actions/workflows/main.yml)

#  Kittygram

## О проекте

В данном проекте реализована мини соцсеть для владельцев кошек, в которой можно делиться фотками котиков и их достижениями

## Технологии
Python 3.9, Django 4.1, Django REST framework, React, Docker, Nginx

## Запуск проекта на локальном компьютере

Для запуска проекта необходимо иметь на установленные: node.js, python, pip.

клонировать проект:
https://github.com/zaylyalow/kittygram_final.git
frontend:
cd frontend
npm i
rpm run dev

backend:
cd backend
python -m venv venv

# Linux/macOS:
```
  source env/bin/activate
  ```
# windows:
  ```
  source venv/Scripts/activate
  ```

```
pip install -r requirements.txt
```
```
python manage.py migrate
```
```
python manage.py runserver
```
При успешном старте получим backend приложение на 127.0.0.1:9000

## Альтернативная установка возможна при налиичи на локальом компьютере Docer compose

Запустите проект из корня с помощью команды:
```
docker compose up
```
Соберите статику Django с помощью команды:
```
docker compose exec backend python manage.py collectstatic
```
Скопируйте статику командой:
```
docker compose exec backend cp -r /app/collected_static/. /static/static/
```
По адресу http://127.0.0.1:9000/ сайт будет доступен.


### Автор проекта Зайлялов Шамиль