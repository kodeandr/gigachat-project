# 🤖 GigaChat AI — Итоговый проект по Frontend-разработке

Веб-приложение для общения с нейросетью **GigaChat** от Сбера.  
Проект состоит из клиентской части (React) и прокси-сервера (Node.js).  
Выполнено в рамках итогового домашнего задания по дисциплине «Основы frontend-разработки».

## 🔗 Репозиторий

Актуальный код: [github.com/kodeandr/gigachat-project](https://github.com/kodeandr/gigachat-project)

## 📋 Функциональные возможности

### 💬 Чат с ИИ
- Полноценный диалог с сохранением контекста
- Потоковая генерация ответов (streaming)
- Поддержка **Markdown**: заголовки, списки, блоки кода, таблицы
- Подсветка синтаксиса кода (более 100 языков)
- Копирование ответа в буфер обмена
- Остановка генерации длинного ответа

### 📂 Управление чатами
- Создание чата с автоматическим названием
- Редактирование названия
- Удаление с подтверждением
- Поиск по названию и содержимому
- Сохранение истории в `localStorage`

### ⚙️ Настройки
- Выбор модели, регулировка `temperature`, `top_p`, `max_tokens`
- Системный промпт
- Переключение светлой / тёмной темы

## 🛠 Технологии

### Frontend
- React 19 + TypeScript
- Zustand (стейт-менеджмент)
- React Router DOM
- React Markdown + remark-gfm
- rehype-highlight + highlight.js
- CSS (кастомная тема в стиле AI-агентов)

### Backend
- Node.js + Express
- CORS
- node-fetch
- dotenv

## 🚀 Запуск проекта

### 📋 Требования
- Node.js 16+
- Git
- Ключ авторизации GigaChat ([получить](https://developers.sber.ru/studio))

### 1. Клонирование

git clone https://github.com/kodeandr/gigachat-project.git
cd gigachat-project

### 2. Установка зависимостей

# Бэкенд
cd backend
npm install

# Фронтенд
cd ../frontend
npm install

### 3. Настройка бэкенда
В папке backend создайте файл .env (или проверьте существующий) и укажите порт при необходимости:

text
PORT=3001

### 4. Запуск
Терминал 1 – Бэкенд

cd backend
npm run dev
Сервер запустится на http://localhost:3001.

Терминал 2 – Фронтенд

cd frontend
npm start
Приложение откроется на http://localhost:3000.

### 5. Вход в приложение
Вставьте скопированный Authorization Key в поле ввода.

Выберите Scope (рекомендуется GIGACHAT_API_PERS).

Нажмите «Войти».

Начните диалог с GigaChat.

❗ Возможные проблемы
Фронтенд не видит бэкенд (Network Error)
Убедитесь, что бэкенд запущен на порту 3001.

Проверьте URL в файле frontend/src/services/gigachatApi.ts (должен быть http://localhost:3001).

Ошибка авторизации GigaChat
Проверьте ключ на лишние пробелы.

Попробуйте другой Scope.

Порт занят
Для фронтенда при запуске npm start нажмите Y для смены порта.

Для бэкенда измените PORT в .env или server.js.


👤 Автор
Korobov Denis (kodeandr)
Проект выполнен в учебных целях, 2026 г.