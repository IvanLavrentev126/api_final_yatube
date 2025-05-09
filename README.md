# api_final_yatube
## 1. Описание проекта:

REST API для социальной платформы Yatube. Полнофункциональное API позволяет взаимодействовать со всеми основными сущностями платформы: публикациями, комментариями, группами и подписками.
## 2. Как запустить проект
Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:IvanLavrentev126/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

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
___
## 3. Примеры использования
```http
POST /api/v1/jwt/create/
Content-Type: application/json

{
  "username": "ваш_логин",
  "password": "ваш_пароль"
}
```
### Получение публикаций
```
GET /api/v1/posts/
[
    {
        "id": свое,
        "author": "свое",
        "image": null,
        "text": "свое", #обязательное поле
        "pub_date": "свое",
        "group": null
    }
]
```
### Создание публикации
```
POST /api/v1/posts/
{
    "text": "свое"
}