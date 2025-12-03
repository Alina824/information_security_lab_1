### 1. POST /auth/login
Аутентификация пользователя.

**Request:**
```json
{
  "username": "admin",
  "password": "admin123"
}
```

**Response:**
```json
{
  "access_token": "eyJ0eXAiOiJKV1QiLCJhbGc...",
  "token_type": "Bearer",
  "user": {
    "id": 1,
    "username": "admin"
  }
}
```

### 2. GET /api/data
Получение данных (требуется аутентификация).

**Headers:**
```
Authorization: Bearer <access_token>
```

**Response:**
```json
{
  "user_id": 1,
  "posts": [...],
  "count": 0
}
```

### 3. POST /api/users
Создание нового пользователя.

**Request:**
```json
{
  "username": "newuser",
  "password": "securepassword123"
}
```

**Response:**
```json
{
  "message": "User created successfully",
  "user": {
    "id": 2,
    "username": "newuser"
  }
}
<img width="950" height="901" alt="image" src="https://github.com/user-attachments/assets/2190c991-062e-4977-8957-a4eaa2c4ae11" />
<img width="1517" height="911" alt="image" src="https://github.com/user-attachments/assets/888b448c-80b7-4dda-9aa0-893f8686d7cd" />
<img width="550" height="274" alt="image" src="https://github.com/user-attachments/assets/6cbc9861-e642-46f5-af20-4b3ed78774e8" />


