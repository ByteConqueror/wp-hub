# 🐳 WordPress + MySQL via Docker Compose

[![Docker](https://img.shields.io/badge/Docker-Compose-blue?logo=docker)](https://www.docker.com/)
[![WordPress](https://img.shields.io/badge/WordPress-6.x-blue?logo=wordpress)](https://wordpress.org)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-orange?logo=mysql)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

Легкий спосіб розгорнути **WordPress + MySQL** за допомогою Docker Compose.  
Проєкт створено для навчальної практики та швидкого деплойменту WordPress-середовища.
---

## 🚀 Швидкий старт

### 1. Клонуй репозиторій

```bash
git clone https://github.com/ByteConqueror/wp-hub.git
cd wp-hub

### 2. Створи та налаштуй .env
```bash
 cp .env.example .env

та заповни власні значення:
```bash
DB_NAME=exampledb
DB_USER=exampleuser
DB_PASSWORD=examplepass
DB_ROOT_PASSWORD=supersecretroot

### 3. Запусти контейнери
```bash
docker compose up -d

### 4. Відкрий у браузері
```bash
http://<IP_твого_сервера>:8080/

👉 З’явиться інсталятор WordPress.

### Структура
```bash
.
├── docker-compose.yml   # Конфігурація сервісів WordPress + MySQL
├── .env.example          # Приклад змінних оточення (без секретів)
├── .gitignore            # Виключає .env, резервні копії тощо
└── /opt/wordpress/
    ├── wp_data/          # Файли WordPress (plugins, themes, media)
    └── db_data/          # Дані MySQL (таблиці, схеми)

🧩 Корисні команди

Перевірити статус:
```bash
docker compose ps

Переглянути логи:
```bash
docker compose logs -f

Зупинити:
```bash
docker compose down

💡 Примітки

Образ wordpress:6-apache — стабільна версія WordPress з Apache.

Дані зберігаються у bind mounts /opt/wordpress/wp_data та /opt/wordpress/db_data.

Секрети зберігаються в .env, який не потрапляє у Git.

Автор: ByteConqueror

Проєкт для практики роботи з Docker Compose та офіційними образами WordPress.
