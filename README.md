## Описание.

Проект «API для Yatube» предоставляет доступ
к постам, комментариям, группам и подпискам 
Yatube, в зависимости от статуса пользователя. 
Аутентификация реализована по JWT-токену.

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/MihVS/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv venv
```

```
source venv/bin/activate
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

## Примеры запросов к API.

Получить список всех публикаций. При указании параметров limit и offset выдача работает с пагинацией.

```
GET /api/v1/posts/
```

Получение публикации по id.

```
GET /api/v1/posts/{id}/
```

Получение комментария к публикации по id.

```
GET /api/v1/posts/{post_id}/comments/{id}/
```

После запуска сервера подробная документация доступна по адресу: http://localhost:8000/redoc/ 
