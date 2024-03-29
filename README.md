# Библиотечная система на основе блокчейна

Это простая библиотечная система на основе блокчейна, написанная на Go. Она использует пакет Gorilla Mux для обработки HTTP-запросов и ответов.

## Функции

- **Управление книгами**: Позволяет создавать новые книги с такими деталями, как название, автор, дата публикации и ISBN.
- **Транзакции блокчейна**: Каждый выдача книги является транзакцией, которая добавляется в блокчейн.
- **Целостность данных**: Каждый блок в блокчейне содержит хеш предыдущего блока, обеспечивая целостность всего блокчейна.

## Структуры

- **Book**: Представляет книгу с такими свойствами, как ID, название, автор, дата публикации и ISBN.
- **Block**: Представляет блок в блокчейне. Каждый блок содержит позицию в блокчейне, временную метку, хеш блока, хеш предыдущего блока и данные (BookCheckout).
- **BookCheckout**: Представляет транзакцию выдачи книги с такими свойствами, как ID книги, пользователь, дата выдачи и является ли это генезис-блоком.
- **BlockChain**: Представляет весь блокчейн в виде среза блоков.

## Конечные точки

- `GET /`: Возвращает весь блокчейн.
- `POST /`: Записывает новый блок в блокчейн.
- `POST /new`: Создает новую книгу.

## Как запустить

1. Убедитесь, что у вас установлен пакет Gorilla Mux. Если нет, установите его с помощью `go get -u github.com/gorilla/mux`.
2. Запустите программу с помощью `go run main.go`.
3. Сервер начнет работу на порту 3000.

## Примечание

Это базовая реализация блокчейна и не подходит для производственного использования. Она предназначена только для образовательных целей.
