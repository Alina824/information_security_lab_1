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

