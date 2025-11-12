# 🐳 WordPress + MySQL via Docker Compose

Цей проєкт — приклад запуску WordPress із базою даних MySQL за допомогою Docker Compose.  
Використовується офіційний образ **WordPress** з Docker Hub та **MySQL 8.0**.

---

## 🚀 Як запустити

### 1. Клонуй репозиторій

git clone https://github.com/ByteConqueror/wp-hub.git

cd wp-hub

### 2. Створи .env файл на основі прикладу

 cp .env.example .env

та заповни власні значення:

DB_NAME=exampledb
DB_USER=exampleuser
DB_PASSWORD=examplepass
DB_ROOT_PASSWORD=supersecretroot

### 3. Запусти контейнери

docker compose up -d

### 4. Відкрий у браузері

http://<IP_твого_сервера>:8080/

👉 З’явиться інсталятор WordPress.

### Структура

.
├── docker-compose.yml   # Конфігурація сервісів WordPress + MySQL
├── .env.example          # Приклад змінних оточення (без секретів)
├── .gitignore            # Виключає .env, резервні копії тощо
└── /opt/wordpress/
    ├── wp_data/          # Файли WordPress (plugins, themes, media)
    └── db_data/          # Дані MySQL (таблиці, схеми)

🧩 Корисні команди

Перевірити статус:

docker compose ps

Переглянути логи:

docker compose logs -f

Зупинити:

docker compose down

💡 Примітки

Образ wordpress:6-apache — стабільна версія WordPress з Apache.

Дані зберігаються у bind mounts /opt/wordpress/wp_data та /opt/wordpress/db_data.

Секрети зберігаються в .env, який не потрапляє у Git.

Автор: ByteConqueror

Проєкт для практики роботи з Docker Compose та офіційними образами WordPress.
