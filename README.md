# Trello-like API with Telegram Bot

## 📌 Описание проекта
Backend-сервис для управления задачами (аналог Trello) с интеграцией Telegram-бота. Реализован на FastAPI с использованием современных подходов:
- **Асинхронность** (async/await)
- **Контейнеризация** (Docker)
- **Кэширование** (Redis)
- **Мониторинг** (Prometheus + Grafana)

## 🏗 Архитектура (Clean Architecture + DDD)

trello-fastapi-bot/

├── api/ # FastAPI приложение

├── bot/ # Telegram бот (aiogram)

└── infra/ # DevOps (Docker, мониторинг)

## 🔧 Технологии
| Компонент       | Технологии                          |
|-----------------|-------------------------------------|
| Backend         | FastAPI, SQLAlchemy 2.0, Pydantic V2|
| База данных     | PostgreSQL (asyncpg)                |
| Бот             | aiogram (асинхронный)               |
| Инфраструктура  | Docker, Redis, Prometheus           |

## 🚀 Запуск проекта
1. **Клонировать репозиторий**:

git clone https://github.com/L1inkoln/trello-fastapi-bot.git

cd trello-fastapi-bot

2. **Настроить окружение**:
   
cp .env.example .env

3. **Запустить сервисы**:

docker-compose -f infra/docker-compose.yml up --build

## 📡 Основные API-эндпоинты
GET /health - Проверка статуса

POST /boards - Создание доски

GET /boards/{id} - Получение доски

## 🤖 Команды бота
/start - Начало работы

/newboard Название - Создать доску

/task Добавить "Описание" - Новая задача

## 🛡️ Безопасность
JWT-аутентификация

Rate limiting (Redis)

Валидация данных (Pydantic)

## 📊 Мониторинг
Prometheus: http://localhost:9090

Grafana: http://localhost:3000
