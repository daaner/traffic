# Transactions

Получение данных по транзакциям.

## Содержание
- [x] [Вывод списка транзакций](Transactions.md#showTransaction)


## Все методы модели
- [showTransaction](#showTransaction)


---



### `showTransaction`
AUTH

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

[filename](json/transactions_show.json ':include')

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


