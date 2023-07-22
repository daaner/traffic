# Transactions

Получение данных по транзакциям.

## Содержание
- [x] [Вывод списка транзакций](Transactions.md#showTransaction)
- [x] [Вывод конкретной транзакции](Transactions.md#edit)


## Все методы модели
- [showTransaction](#showTransaction)
- [edit](#edit)


---



### `showTransaction`
AUTH Bearer JWT

Вывод списка транзакций пользователя.

```php
// Транзакции для пользователя
// GET
$url = '/api/transactions/show';
// поля для запроса (все не обязательные)
$query = [
  "from" => '2023-06-01', //необязательно
  "to" => '2023-07-30', //необязательно
  "page" => 2, // по умолчанию 1
  "count" => 15,  //по умолчанию 25
];
```

Пример ответа
```json
{
    "currentPage": 1,
    "lastPage": 674,
    "perPage": 15,
    "total": 10103,
    "items": [
        {
            "id": 1,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "e7789b02-b55a-4023-8078-dbb19d4eb560",
            "comment": "a10IBGHcyGCJCtZx03iYZsDLCzp31vxMlyJhvmmp4wXbpKelGV43AeHErpP6SsGTqaYJuQNXuHnYterb3gDm1KCc7nMUvR9vmSl8",
            "created_at": "2023-07-04T11:49:22.000000Z"
        },
        {
            "id": 2,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "a80f28e4-d116-464d-98a0-799b79f9bdd0",
            "comment": "PwPsvwA5SLAr5J9xkp3jtQnjBcQ6p7tsnN4nmqH2p072rThxNM6WylhBqS9An25izhQi1jhh6sx9lPU7kfjeRrZ54bL4dAJd0ktM",
            "created_at": "2023-07-07T11:49:22.000000Z"
        },
        {
            "id": 3,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "41c089a7-42ce-4ae6-9056-ab6127504075",
            "comment": "n4GrWpZPdq6GlJ5mrkCUFJBv9r0EEymUL2Y2xWOYxckSqGJGTPdlwM2rpBinEqCkYvxOhVYQottlftdX85pgCuA3EkavXvatTcu4",
            "created_at": "2023-07-05T11:49:22.000000Z"
        },
        {
            "id": 4,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "00455452-d126-4e8b-9b63-338647da6e53",
            "comment": "8cOioh3Dt9cj5Awq6jI2JjdKlwEk5s9WWBCnWekymEKLjjoVdiX92btFBDT19l9QZNeiqIQqWeO0VYSfZcMdsSzlY36P2TQVYMdq",
            "created_at": "2023-07-05T11:49:22.000000Z"
        },
        {
            "id": 5,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "42f16fdb-6ae0-4bd9-a39c-c13d70ff2ba8",
            "comment": "msON7PKnPQic15kTG9hI1K0oXvD1gbWuV3xso2iHGVU8frz7SwyuoxOplTdioaC1tXEk2NpUIojxUVQqhiNKlwgfcQeP0GDXfOOu",
            "created_at": "2023-07-04T11:49:22.000000Z"
        },
        {
            "id": 6,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "175334fa-daa4-494a-ad9f-3ea4e016d973",
            "comment": "G3VvTtMqhGaATLv0rUhLxWytffyLIp8XgNjCutWHvNwcbx0cquqb7uRhCelwovefCUsYsjIN4wRPCFT1ZhRLfO1Rfyi1iUqeqWnT",
            "created_at": "2023-07-08T11:49:22.000000Z"
        },
        {
            "id": 7,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "11883a9a-54e7-4e80-87d6-af1eca575db1",
            "comment": "GoWelZXbwKassphIhX95BCh3MyGVpTVU3qeqzMhPAE2b8ImlWtiCYgkW71jgbiokGwoUwqn9AwUqjl9sosAhK7iNAre2VQVUtKBJ",
            "created_at": "2023-07-09T11:49:22.000000Z"
        },
        {
            "id": 8,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "b3f0f6ba-160b-4dc1-bc35-cca0bfcbef7a",
            "comment": "txx3p0ElBxOYnIaR06aWfuazxmislCMe0FuURelQOO7CEZzNvPPiGjb26NvU1ljQNTCcLML65zqnNBtzQosy3gDTQuAUljAvSH4R",
            "created_at": "2023-07-12T11:49:22.000000Z"
        },
        {
            "id": 9,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "8f5445a3-047b-4da1-ba65-70bdbd5043eb",
            "comment": "zfRcNTVH6MkzQn5WKaH5nW2yot8dq7mF00vXOjZEWQkS88QkKW7iRjJ6SSPNppqgXcxaDa1k4Sl6ikhBVEagABgqvzdXriNyJOFb",
            "created_at": "2023-07-04T11:49:22.000000Z"
        },
        {
            "id": 10,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "6b0a8d7c-2531-409e-9c3a-bc2bca748db8",
            "comment": "PZHXKhmKHDio77ch16v9hBBWIFrv8AE2Sq8ZAsVG3ytfZ9h4hql7Jhl2H9Osr2F7ZOfXV0NodgJSg6n6uIWmIWh4gTv8qpr4yCaC",
            "created_at": "2023-07-13T11:49:22.000000Z"
        },
        {
            "id": 11,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "c3d6215a-de0f-40a4-9b48-a20cc76aa9ed",
            "comment": "XIdtwyZCnzXSan43KicMWrZHMdJFXrzJYexNHlat0cs71iSfUgbHyIy7G7A3z85F77skju200BuzCwIKhZxYIO9nVQc19Xd0tqeD",
            "created_at": "2023-07-04T11:49:22.000000Z"
        },
        {
            "id": 12,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "49c53bbc-a0bb-4e43-b493-4949eb1df43f",
            "comment": "mDfvTbVDPziJFgmZfMOXcPNASl1FLq0cOZcGF2JHHcTgVKv1zhk5wGKy2vzraEiy1dcxkCEzCWu3EQlUC4I19zPt8ugNK57gd3uO",
            "created_at": "2023-07-13T11:49:22.000000Z"
        },
        {
            "id": 13,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "c6f02240-d40b-42de-a16e-7395aa11f179",
            "comment": "7P4TrkYhUeu8L9Xdu15J7l4RpaPX4z3JwaH5dZcYHdCDEoBqfpUaVYFRyIBZlTw7jDKhJIPC4bBUtCGTaxpPHrRh8PpZz8Zyn98l",
            "created_at": "2023-07-06T11:49:22.000000Z"
        },
        {
            "id": 14,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "7f4d26f1-c79b-4d68-9599-2a5ceaf04c17",
            "comment": "V8bviHt1jRLztqqsLMC7uynD5kQMIj4VOmbpI9D4BD9cCC9Ydi93EM3R1VkAJ15e7D00XbcqHx5hZzygSwThk2x6Uvc7AXMxQVWy",
            "created_at": "2023-07-09T11:49:22.000000Z"
        },
        {
            "id": 15,
            "source": "BroCard",
            "amount": "-1753.00",
            "amount_string": "-$1753",
            "external_id": "e413027c-7698-42a5-ace6-1fb244851827",
            "comment": "qUC2hRhrRfGjTRMofHcrIedoEGDkdQblBq7DjX7Zhvd5pQKKvI8AsTtKN6SMjNzXXFFmpuluqKWVJPBlUYPxQ5zxdTvgUr5Ir0X0",
            "created_at": "2023-07-04T11:49:22.000000Z"
        }
    ]
}
```

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


### `edit`
AUTH Bearer JWT

Вывод конкретной транзакции по ID.

```php
// Транзакции для пользователя
// GET $url = '/api/transactions/{id}/edit';
$url = '/api/transactions/100500/edit';

```
Пример ответа
```json
{
    "success": true,
    "data": {
        "id": 2,
        "user_id": 3,
        "source_id": 2,
        "external_id": "a80f28e4-d116-464d-98a0-799b79f9bdd0",
        "currency_id": 1,
        "amount": "-1753.00",
        "comment": "PwPsvwA5SLAr5J9xkp3jtQnjBcQ6p7tsnN4nmqH2p072rThxNM6WylhBqS9An25izhQi1jhh6sx9lPU7kfjeRrZ54bL4dAJd0ktM",
        "created_at": "2023-07-07T11:49:22.000000Z",
        "updated_at": "2023-07-13T11:49:22.000000Z",
        "deleted_at": null,
        "currency": {
            "id": 1,
            "iso": "USD",
            "symbol": "$",
            "prefix": 1
        },
        "source": {
            "id": 2,
            "key": "brocard",
            "front_name": "BroCard",
            "type": "liability"
        }
    }
}
```

Пример ошибки
```json
{
    "success": false,
    "data": []
}
```

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


