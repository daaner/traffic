# Auth

Авторизация и идентификация.

## Содержание
- [x] [Регистрация](Auth.md#register)
- [x] [Вход](Auth.md#login)


## Все методы модели
- [Register](#register)
- [Login](#login)


---



### `register`
NOT AUTH

Регистрация для пользователя.

```php
// POST
$url = '/api/auth/register';
// поля для запроса
$query = [
  "name" => 'User',
  "email" => 'user@site.com',
  "password" => 'password123456',
  "confirm_password" => 'password123456',
];

```

Пример ответа
```json
{
    "success": true,
    "info": {
        "access_token": "eyJ0eX...vX4x5OA",
        "expires_in": 3600,
        "user": {
            "name": "User",
            "email": "user@site.com",
            "role": {
                "id": 1,
                "name": "Пользователь"
            }
        }
    }
}
```

Пример ошибки
```json
{
    "success": false,
    "errors": {
        "name": [
            "Данные name должны быть переданы"
        ],
        "email": [
            "Данные email должны быть переданы"
        ],
        "password": [
            "Данные password должны быть переданы"
        ]
    }
}
```

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


### `login`
NOT AUTH

Вход для пользователя.

```php
// POST
$url = '/api/auth/login';
// поля для запроса
$query = [
  "email" => 'user@site.com',
  "password" => 'password123456',
];

```

Пример ответа
```json
{
    "success": true,
    "info": {
        "access_token": "eyJ0eX...vX4x5OA",
        "expires_in": 3600,
        "user": {
            "name": "User",
            "email": "user@site.com",
            "role": {
                "id": 1,
                "name": "Пользователь"
            }
        }
    }
}
```

Пример ошибки
```json
{
    "success": false,
    "errors": {
        "email": [
            "Данные email должны быть переданы"
        ],
        "password": [
            "Данные password должны быть переданы"
        ]
    }
}
```

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


