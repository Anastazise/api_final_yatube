Описание:
Это REST API для блог-платформы Yatube.
Позволяет просматривать и отправлять посты, просматривать группы, подписываться на авторов.

Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:

git clone git@github.com:Anastazise/api_final_yatube.git
cd api_final_yatube
Cоздать и активировать виртуальное окружение:

python -m venv venv
source venv/Scripts/activate 
Установить зависимости из файла requirements.txt:

python -m pip install --upgrade pip
pip install -r requirements.txt
Выполнить миграции:

python manage.py migrate
Запустить проект:

python manage.py runserver

Примеры ответа

Получить все посты
[GET] localhost:8000/api/v1/posts/
Ответ

[
    {
        "id": 0,
        "text": "string",
        "author": "string",
        "pub_date": "2019-08-24T14:15:22Z"
    }
]

Опубликовать пост

localhost:8000/api/v1/posts/
Ответ - содержимое объекта поста

[
    {
        "id": 0,
        "text": "string",
        "author": "string",
        "pub_date": "2019-08-24T14:15:22Z"
    }
]

Остальные примеры запросов можно посмотреть в файле \api_final_yatube\yatube_api\static\redoc.yaml