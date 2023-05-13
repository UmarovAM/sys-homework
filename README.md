Домашнее задание к занятию «Базы данных» Умаров Азиз

# Задание 1
## Опишите не менее семи таблиц, из которых состоит база данных:
1	Employee
2	Salary
3	Project
4	EmployeeProject
5	Position
6	DepartmentType
7	Address
8	DepartmentAddress

![image](https://github.com/UmarovAM/sys-homework/assets/118117183/b525586f-3184-4feb-921c-e18a71e19f94)


## Какие данные хранятся в этих таблицах;
Ответ в таблице:
https://1drv.ms/x/s!AtjLhewZ3c_dgacE_2KV1fyVXxrQUA?e=xL2yrk

## Какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.
Ответ в таблице:
https://1drv.ms/x/s!AtjLhewZ3c_dgacE_2KV1fyVXxrQUA?e=NDiYjN

## Приведите решение к следующему виду:
```
Employee(
EmployeeId PRIMERY KEY smallserial,
EmployeeFullName varchar(128),
DateHiring date,
SalaryId SECONDARY KEY smallint,
PositionId SECONDARY KEY smallint
DepartmentTypeId SECONDARY KEY smallint
DepartmentId SECONDARY KEY smallint
AddressID SECONDARY KEY smallint);

```
