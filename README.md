# YaTube - Сервис ведения дневников.

## Используемые технолологии:

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Django](https://img.shields.io/badge/Django-005571?style=for-the-badge&logo=Django)
![sql](https://img.shields.io/badge/sql-%2300f.svg?style=for-the-badge)


## О проекте:

Мой первый проект на котором я обкатывал Django, DRF и работал с базой данных. Сам по себе проект довольно простой, но зато можно посмотреть с чего я начинал.

### Контакты: [t.me/gl_ready](https://t.me/gl_ready/)

## Оглавление:

- [Yatube](#Yatube)
- [API](#API)


## Yatube

Cоздать и активировать виртуальное окружение внутри yatube/:

```
python3 -m venv env
```

* Если у вас Linux/macOS

    ```
    source env/bin/activate
    ```

* Если у вас windows

    ```
    source env/scripts/activate
    ```

```
python3 -m pip install --upgrade pip
```

Установить зависимости из файла requirements.txt:

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```

## API

Запуск API идентичен запуску основной части проекта

Аунтификация токена:

Создание временного токена на сутки:

```
http://127.0.0.1:8000/api/v1/auth/jwt/create/
```

Обновить токен:

```
http://127.0.0.1:8000/api/v1/auth/jwt/refresh/
```

Получить токен обновления:

```
http://127.0.0.1:8000/api/v1/auth/jwt/verify/
```

## Примеры запросов к Api:

Получить список всех публикаций. При указании параметров limit и offset выдача должна работать с пагинацией.

```
http://127.0.0.1:8000/api/v1/posts/?offset=400&limit=100
```

Получение публикации по id.

```
http://127.0.0.1:8000/api/v1/posts/1/
```
