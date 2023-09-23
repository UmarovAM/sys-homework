# Домашнее задание к занятию "«SQL. Часть 2" - `Умаров Азиз`


### Задание 1

Одним запросом получите информацию о магазине, в котором обслуживается более 300 покупателей, и выведите в результат следующую информацию: 
- фамилия и имя сотрудника из этого магазина;
- город нахождения магазина;
- количество пользователей, закреплённых в этом магазине.
```sql
select concat(s2.last_name, ' ', s2.first_name), c2.city, count(c.store_id)
from customer c join store s on s.store_id = c.store_id 
		join staff s2 on s2.staff_id = s.manager_staff_id 
		join address a on s2.address_id = a.address_id 
		join city c2 on c2.city_id = a.city_id 
group by c.store_id 
having count(c.store_id) > 300
```
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/fc46866e-98e8-4e78-874d-c8da46d241de)

### Задание 2

Получите количество фильмов, продолжительность которых больше средней продолжительности всех фильмов.
```sql
select count(f.title)
from film f
where f.`length` > (select avg (`length`) from film)
```
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/62abd86f-5d17-423e-aa3c-00fdd726ed4e)

### Задание 3

Получите информацию, за какой месяц была получена наибольшая сумма платежей, и добавьте информацию по количеству аренд за этот месяц.
```sql
select date_format(payment_date, '%d%m%y'), sum(p.amount), count(p.rental_id)
from payment p
group by date_format(payment_date, '%d%m%y')
order by sum(p.amount) desc 
limit 1
```
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/dbf3f341-332e-428e-92a7-cf2638bb4590)


## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.

### Задание 4*

Посчитайте количество продаж, выполненных каждым продавцом. Добавьте вычисляемую колонку «Премия». Если количество продаж превышает 8000, то значение в колонке будет «Да», иначе должно быть значение «Нет».

### Задание 5*

Найдите фильмы, которые ни разу не брали в аренду.
