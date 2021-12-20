# api_final

## Описание
Это учебный проект в рамках 9 спринта курса Питон-разработчик, посвященный ключевому инструментарию работы с DRF

## Установка
Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Ostenya/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение (для Windows):

```
python -m venv venv
```

```
source venv/scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

## Примеры

### Получение публикаций
Получить список всех публикаций. При указании параметров limit и offset выдача должна работать с пагинацией.

Запрос:
```
GET http://127.0.0.1:8000/api/v1/posts/
```

Ответ:
```
{
"count": 123,
"next": "http://api.example.org/accounts/?offset=400&limit=100",
"previous": "http://api.example.org/accounts/?offset=200&limit=100",
"results": [
{}
]
}
```
