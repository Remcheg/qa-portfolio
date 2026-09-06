# SQL Basics: QA Cheatsheet

**Цель:** Продемонстрировать понимание базовых SQL-запросов, необходимых тестировщику для проверки данных в базе данных (БД).

**Инструмент:** DBeaver / pgAdmin / любой SQL-клиент

---

## 1. Простая выборка данных (SELECT + WHERE)
**Задача:** Найти пользователя с конкретным email в таблице `users`.

```sql
SELECT id, name, email 
FROM users 
WHERE email = 'rem@test.com';

---

## 2. Фильтрация данных (WHERE с условиями)
Задача: Найти все товары дороже 100 в таблице products.
SELECT name, price 
FROM products 
WHERE price > 100;

---

## 3. Объединение таблиц (JOIN)
Задача: Получить список всех заказов для пользователя с email 'rem@test.com', объединив таблицы users и orders.
SELECT users.name, users.email, orders.order_id, orders.amount
FROM users
JOIN orders ON users.id = orders.user_id
WHERE users.email = 'rem@test.com';
