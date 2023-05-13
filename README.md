### Домашнее задание к занятию «Базы данных» Умаров Азиз

# Задание 1
## Опишите не менее семи таблиц, из которых состоит база данных:
Прикрепил файл с таблицами на разных листах в файле Excel еще внизу в виде скрина с описанием

[hw-12-1 Умаров Азиз.xlsx](https://github.com/UmarovAM/sys-homework/files/11469887/hw-12-1.xlsx)

еще внизу в виде скрина с описанием

1. Employee
2. Salary
3. Project
4. EmployeeProject
5. Position
6. DepartmentType
7. Department
8. Address
9.	DepartmentAddress

## 1.	Employee
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/cd462c26-dc98-4475-b153-3d0e0420aa90)
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
## 2.	Salary
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/74a03b87-b015-47f6-9ccf-9239ae10e7ed)

## 3.	Project
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/1eae8981-c6d4-4f0e-b1b2-fe273bf35c07)

## 4.	EmployeeProject
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/d8f670bb-c02b-421b-9927-658b01894d95)

## 5.	Position
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/8dbde879-d68f-4865-8625-7e2b1b7574f6)

## 6.	DepartmentType
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/0be339f9-6e48-4ca9-ac96-15fd2af69c37)

## 7.	Department
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/eb06234e-42c4-4af8-8f46-0bce097ea384)

## 8.	Address
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/9b3f5345-7e16-4662-a3aa-4af5694d8b28)

## 9.	DepartmentAddress
![image](https://github.com/UmarovAM/sys-homework/assets/118117183/0e80b7d7-3ef0-4bc2-80ad-3869c97139f4)



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
