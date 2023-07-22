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
[filename](json/transactions_show.json ':include')

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
[filename](json/transactions_edit.json ':include')

[Содержание](#Содержание) [Методы модели](#Все-методы-модели)
***


