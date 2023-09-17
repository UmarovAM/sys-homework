# Домашнее задание к занятию "Работа с данными (DDL/DML)" - `Умаров Азиз`

## Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/775592fe-495e-4e46-8747-37ff81130220)


1.2. Создайте учётную запись sys_temp.

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/34605dab-eb00-43d2-a257-0eb89add5eb9)


1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/39f23a98-e447-464a-a310-9f088df3224c)


1.4. Дайте все права для пользователя sys_temp.

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/564b209b-654b-4f98-a9da-649963ad899e)


1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/756ebe0e-84f6-4417-94d4-d8a9174de484)


1.6. Переподключитесь к базе данных от имени sys_temp.

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/604449c1-ed94-4922-83b0-09220de3130b)


Для смены типа аутентификации с sha2 используйте запрос:

ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/682afafd-ec45-4d5a-93ad-09acea396b75)
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/3bb13145-51b1-48dd-ac21-f089927cea65)
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/859c10fd-bb73-4132-914e-b63fed2ee928)

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/25b7d344-3898-46e6-b5e6-aa5d39021893)
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/794e43c9-e4d3-4c1f-9bdd-8c09e1b9efd4)


Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.

## Задание 2
Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

Название таблицы | Название первичного ключа
customer         | customer_id

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/4ad8c584-52e8-493a-8814-05c471b412bb)

