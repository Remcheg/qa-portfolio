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
