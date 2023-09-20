# Домашнее задание к занятию "SQL. Часть 1" - `Умаров Азиз`


### Задание 1

Получите уникальные названия районов из таблицы с адресами, которые начинаются на “K” и заканчиваются на “a” и не содержат пробелов.

```sql
SELECT DISTINCT district
FROM address
WHERE district LIKE 'K%a' AND district NOT LIKE '% %';
```

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/5ec011a0-8c00-45fd-9278-cbef2499303d)


### Задание 2

Получите из таблицы платежей за прокат фильмов информацию по платежам, которые выполнялись в промежуток с 15 июня 2005 года по 18 июня 2005 года **включительно** и стоимость которых превышает 10.00.

```sql
select amount, payment_date
from payment
where amount > 10 and cast(payment_date as date) between 20050616 and 20050618
order by payment_date;
```

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/b33df338-a6a4-4aef-b0d1-9f8f9b65424e)


### Задание 3

Получите последние пять аренд фильмов.

```sql
select *
from rental
order by rental_id desc 
```

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/315a30f7-a8f0-49f5-9fc0-fbbf96506b6d)


### Задание 4

Одним запросом получите активных покупателей, имена которых Kelly или Willie. 

Сформируйте вывод в результат таким образом:
- все буквы в фамилии и имени из верхнего регистра переведите в нижний регистр,
- замените буквы 'll' в именах на 'pp'.
  
```sql
select first_name, lower (replace (first_name, 'LL', 'PP')), lower(last_name), active 
from customer
where first_name like 'Kelly'or first_name like ('Willie') and active = 1
```

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/54708bb9-e002-404e-aaa6-2f176c071c26)

## Дополнительные задания (со звёздочкой*)
### Задание 5*
Выведите Email каждого покупателя, разделив значение Email на две отдельных колонки: в первой колонке должно быть значение, указанное до @, во второй — значение, указанное после @.

```sql
select 
email, 
substring_index (email, '@',1), 
substring_index (email, '@',-1) 
from customer;
```

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/7db5d5a0-f3e8-4108-8424-ba54789a2362)


### Задание 6*

Доработайте запрос из предыдущего задания, скорректируйте значения в новых колонках: первая буква должна быть заглавной, остальные — строчными.
