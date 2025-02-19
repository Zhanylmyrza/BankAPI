# Money Management API

## Описание
Этот проект представляет собой RESTful API для управления финансами пользователей. API позволяет пользователям регистрироваться, пополнять счет, переводить деньги, брать и погашать кредиты, а также проверять баланс. Проект построен на Flask с использованием Flask-RESTful, базы данных MongoDB и библиотеки bcrypt для хеширования паролей.

## Стек технологий
- Python 3
- Flask
- Flask-RESTful
- MongoDB
- bcrypt
- Docker & Docker Compose

## Установка и запуск

### 1. Клонирование репозитория
```bash
  git clone (https://github.com/Zhanylmyrza/BankAPI.git)
  cd BankAPI
```

### 2. Установка зависимостей

Перед запуском убедитесь, что у вас установлен Python 3 и pip.
```bash
pip install -r requirements.txt
```

### 3. Запуск проекта без Docker
```bash
python app.py
```

### 4. Запуск проекта с Docker

#### Сборка и запуск контейнеров
```bash
docker-compose up --build
```

## Использование API

### 1. Регистрация пользователя
**POST** `/register`

#### Тело запроса:
```json
{
  "username": "user1",
  "password": "mypassword"
}
```

#### Ответ:
```json
{
  "status": 200,
  "msg": "You successfully signed up for the API"
}
```

---

### 2. Пополнение счета
**POST** `/add`

#### Тело запроса:
```json
{
  "username": "user1",
  "password": "mypassword",
  "amount": 100
}
```

#### Ответ:
```json
{
  "status": 200,
  "msg": "Amount Added Successfully to account"
}
```

---

### 3. Перевод денег другому пользователю
**POST** `/transfer`

#### Тело запроса:
```json
{
  "username": "user1",
  "password": "mypassword",
  "to": "user2",
  "amount": 50
}
```

#### Ответ:
```json
{
  "status": 200,
  "msg": "Amount added successfully to account"
}
```

---

### 4. Проверка баланса
**POST** `/balance`

#### Тело запроса:
```json
{
  "username": "user1",
  "password": "mypassword"
}
```

#### Ответ:
```json
{
  "Username": "user1",
  "Own": 100,
  "Debt": 0
}
```

---

### 5. Взять кредит
**POST** `/takeloan`

#### Тело запроса:
```json
{
  "username": "user1",
  "password": "mypassword",
  "amount": 200
}
```

#### Ответ:
```json
{
  "status": 200,
  "msg": "Loan Added to Your Account"
}
```

---

### 6. Погасить кредит
**POST** `/payloan`

#### Тело запроса:
```json
{
  "username": "user1",
  "password": "mypassword",
  "amount": 50
}
```

#### Ответ:
```json
{
  "status": 200,
  "msg": "Loan Paid"
}
```

## Файлы проекта

### `app.py`
Главный файл проекта, содержащий все обработчики API.

### `Dockerfile`
Определяет среду выполнения для запуска API в контейнере.

### `docker-compose.yml`
Файл конфигурации для запуска приложения и базы данных MongoDB в контейнерах.

### `requirements.txt`
Список зависимостей проекта.

## Дополнительные материалы 

![image](https://github.com/user-attachments/assets/64df11ab-e289-486a-977a-1f8979392655)

![image](https://github.com/user-attachments/assets/e6f18c37-0554-4250-93fa-feac11413410)

![image](https://github.com/user-attachments/assets/fb99c803-ccd0-435a-81f9-37a3deb02c1f)

И так далее, и тому подобное......


