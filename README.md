# Taski - Управление задачами

## Описание проекта
Taski - это веб-приложение для управления задачами, построенное на Django REST Framework. Проект предоставляет REST API для создания, редактирования и управления задачами.

## Структура проекта

```
.
├── .github
├── backend
├── frontend
├── gateway
├── .gitignore
├── LICENSE
├── README.md
├── docker-compose.production.yml
├── docker-compose.yml
└── setup.cfg
```
## API Endpoints

### Задачи (Tasks)

```
GET /api/tasks/ - Получить список задач
POST /api/tasks/ - Создать новую задачу
GET /api/tasks/{id}/ - Получить конкретную задачу
PUT /api/tasks/{id}/ - Обновить задачу
PATCH /api/tasks/{id}/ - Частично обновить задачу
DELETE /api/tasks/{id}/ - Удалить задачу
```

## Модель данных

### Task

- id: Уникальный идентификатор задачи
- title: Заголовок задачи
- description: Описание задачи
- completed: Статус выполнения (true/false)

## Установка и запуск

### Требования
- Python 3.8+
- Docker (для разработки и деплоя)
### Установка
1. Клонируйте репозиторий:
```
 git clone https://github.com/Niros0/taski-docker
```
2. Создайте и активируйте виртуальное окружение:
```
python -m venv venv
source venv/bin/activate
```
3. Установите зависимости:
```
pip install -r requirements.txt
```
4. Создайте и примените миграции:
```
python manage.py makemigrations
python manage.py migrate
```
5. Запустите локальный сервер:
```
python manage.py runserver
```
### Запуск через Docker
```
docker compose up -d
```
