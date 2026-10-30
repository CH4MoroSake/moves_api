Movies API
-API для управления базой данных фильмов. EST API приложение на FastAPI 

! возможности:
-CRUD
-Проверка входящих данных на корректность
-Фильтрация и сортировка списка фильмов по различным параметрам
-Автоматическое управление структурой базы данных через миграции

──────────────────────────────────────────────────────────

moves_api/
├── alembic/
│   ├── versions/
│   ├── env.py
│   └── script.py.mako
├── src/
│   ├── models/
│   │   ├── __init__.py
│   │   └── movie.py
│   ├── repositories/
│   │   └── movies.py
│   ├── routers/
│   │   └── movies.py
│   ├── schemas/
│   │   ├── __init__.py
│   │   └── movie.py
│   ├── database.py
│   └── main.py
├── tests/
├── alembic.ini
├── movie.db
├── requirements.txt
└── README.md

──────────────────────────────────────────────────────────

-GET /movies/ — список фильмов
-GET /movies/{id} — фильм по id
-POST /movies/ — добавить
-PUT /movies/{id} — обновить фильм
-PATCH /movies/{id} — частично обновить
-DELETE /movies/{id} — удалить 

Ограничения БД
-Рейтинг: от 0 до 10.
-Год: не меньше 1888.-
-Название и жанр: не пустые.

pip install -r requirements.txt \ alembic upgrade head \ uvicorn src.main:app --reload
id — уникальный нмер
title — название 
genre — жанр (2-100 символов)
rating — рейтинг (0.0 - 10.0)
year — год (от 1888)