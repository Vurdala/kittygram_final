[![Main Taski workflow](https://github.com/Vurdala/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/Vurdala/kittygram_final/actions/workflows/main.yml)

# 🐱 KittyGram

Веб-приложение для обмена фотографиями котиков с API на Django REST Framework и фронтендом на React.

## 📋 Оглавление

- [Функциональности](#-функциональности)
- [Технологический стек](#-технологический-стек)
- [Установка и запуск](#-установка-и-запуск)
- [API Endpoints](#-api-endpoints)
- [Разработка](#-разработка)
- [Деплой](#-деплой)
- [Автор](#-автор)

## 🚀 Функциональности

- 📸 Загрузка и управление фотографиями котиков
- 👤 Регистрация и аутентификация пользователей
- 💬 Комментарии к фотографиям
- 🏷️ Теги и категории для котиков
- 📱 Responsive дизайн
- 🔐 JWT аутентификация
- 🖼️ Загрузка медиа файлов

## 🛠 Технологический стек

### Backend
- **Python 3.11** - основной язык программирования
- **Django 4.2** - веб-фреймворк
- **Django REST Framework 3.14** - API
- **PostgreSQL** - база данных
- **Simple JWT** - аутентификация
- **Pillow** - работа с изображениями
- **CORS Headers** - кросс-доменные запросы

### Frontend
- **React** - пользовательский интерфейс
- **Axios** - HTTP клиент

### Инфраструктура
- **Nginx** - веб-сервер
- **Gunicorn** - WSGI сервер
- **Docker** (опционально) - контейнеризация

## 📦 Установка и запуск

### Предварительные требования
- Python 3.9+
- PostgreSQL 12+
- Node.js 14+ (для фронтенда)

### Backend установка

1. **Клонируйте репозиторий**
```bash
git clone https://github.com/Vurdala/kittygram_final.git
cd kittygram_final/backend
```
2.**Создайте виртуальное окружение**

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# или
venv\Scripts\activate  # Windows
```
3.**Установите зависимости**

```bash
pip install -r requirements.txt
```
3.**Настройте переменные окружения**

```bash
cp .env.example .env
# Отредактируйте .env файл с вашими настройками
```
4.**Примените миграции**

```bash
python manage.py migrate
```
5.**Создайте суперпользователя**
```
bash
python manage.py createsuperuser
```
6.**Запустите сервер**
```
bash
python manage.py runserver
```
7.**Frontend установка**
```
bash
cd ../frontend
npm install
npm start
```

### 🔌 API Endpoints
Аутентификация
POST /api/auth/login/ - вход в систему

POST /api/auth/register/ - регистрация

POST /api/auth/logout/ - выход из системы

POST /api/auth/token/refresh/ - обновление JWT токена

Котики
GET /api/cats/ - список всех котиков

POST /api/cats/ - создание нового котика

GET /api/cats/{id}/ - детали котика

PUT /api/cats/{id}/ - обновление котика

DELETE /api/cats/{id}/ - удаление котика

## Фотографии
GET /api/photos/ - все фотографии

POST /api/photos/ - загрузка фото

GET /api/photos/{id}/ - детали фото

## Комментарии
GET /api/comments/ - комментарии

POST /api/comments/ - создание комментария

## 👤 Автор
Vurdala - GitHub профиль