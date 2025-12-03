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
```

### 2. Створи та налаштуй `.env`

```bash
cp .env.example .env
```

та заповни власні значення:

```bash
DB_NAME=exampledb
DB_USER=exampleuser
DB_PASSWORD=examplepass
DB_ROOT_PASSWORD=supersecretroot
```

### 3. Запусти контейнери

```bash
docker compose up -d
```

### 4. Відкрий у браузері

```
http://<IP_твого_сервера>:8080/
```

👉 З’явиться інсталятор WordPress.

---

## 📂 Структура проєкту

```bash
.
├── docker-compose.yml     # Основна конфігурація Docker Compose
├── .env.example           # Приклад змінних оточення
├── .gitignore             # Виключення для Git
└── /opt/wordpress/
    ├── wp_data/           # Файли WordPress (plugins, themes, media)
    └── db_data/           # Дані MySQL
```

---

## 🧩 Корисні команди

```bash
docker compose ps
docker compose logs -f
docker compose restart
docker compose down
```

---

## ⚙️ Використані технології

| Компонент      | Опис |
|----------------|------|
| **WordPress 6 (Apache)** | Офіційний образ WordPress |
| **MySQL 8.0**  | Стабільна версія MySQL |
| **Docker Compose v2** | Оркестрація контейнерів |
| **Bind Mounts** | Збереження даних на хості |

---

## 🔒 Безпека

- `.env` не потрапляє у Git  
- Використовуй складні паролі  
- Порт MySQL краще не відкривати зовні

---

## 👤 Автор

**ByteConqueror**


