### Описание проекта:

Проект api_final_yatube - это "backend" API для учебной социальной сети yatube.

Автор: Сергей Квашин

### Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Atedzi/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv venv #для windows
```

```
source venv/bin/activate
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

### Примеры запросов к API:

```
(GET) /api/v1/posts/ - Получить список всех публикаций
В ответ должен получить список (если публикаций больше одной конечно же) такого вида:
[
    {
        "id": "int",
        "text": "string",
        "pub_date": "DateTime",
        "author": "string",
        "image"": "string",
        "group": "int"    
    },
    {
        ...
    },
]
```

```
(GET) /api/v1/groups/ - Получить список всех групп
```

```
(GET) /api/v1/posts/1/ - Получить определенную публикацию
```


Создать новую публикацию:

(Требуется аутентификация)
```
(POST) /api/v1/posts/
```