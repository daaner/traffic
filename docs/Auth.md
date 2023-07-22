# Auth

Авторизация и идентификация.

## Содержание
- [x] [Регистрация](Auth.md#register)
- [x] [Вход](Auth.md#login)
- [x] [Восстановление пароля](Auth.md#forgot)
- [x] [Обновление токена](Auth.md#refresh)
- [x] [Выход](Auth.md#logout)
- [x] [Смена пароля](Auth.md#change-password)


## Все методы модели
- [register](#register)
- [login](#login)
- [forgot](#forgot)
- [logout](#logout)
- [change password](#change-password)


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



### `forgot`
NOT AUTH

Восстановление пароля.

```php
// POST
$url = '/api/auth/forgot';
// поля для запроса
$query = [
  "email" => 'user@site.com',
];

```

Пример ответа
```json
{
  "success": true,
  "message": "Проверьте почту и следуйте инструкциям"
}
```

Пример ошибки
```json
{
  "success": false,
  "errors": {
    "email": [
      "Данные email должны быть переданы"
    ]
  }
}
```
PS: Если почта не найдена (ошиблись email`ом или брутфорсят) в базе - выводится ответ о проверке почты

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


### `refresh`
AUTH Bearer JWT

Обновление токена.

```php
// POST
$url = '/api/auth/refresh';
// запрос не нужен
```

Пример ответа как при логине
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

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


### `logout`
AUTH Bearer JWT

Выход из системы.

```php
// POST
$url = '/api/auth/logout';
// запрос не нужен
```

Пример ответа
```json
{
  "success": true,
  "message": "Вы вышли из системы"
}
```

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


### `change-password`
AUTH Bearer JWT

Выход из системы.

```php
// POST
$url = '/api/auth/change-password';
// пример запроса
$query = [
  "password" => 'password123456',
  "confirm_password" => 'password123456',
];
```

Пример ответа
```json
{
  "success": true,
  "message": "Пароль успешно изменен"
}
```

Пример ошибки
```json
{
    "success": false,
    "errors": {
        "password": [
            "Данные password должны быть переданы"
        ],
        "confirm_password": [
            "Пароли должны совпадать"
        ]
    }
}
```

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***

