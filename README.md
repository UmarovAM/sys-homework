### Домашнее задание к занятию «Базы данных» Умаров Азиз

# Задание 1
## Опишите не менее семи таблиц, из которых состоит база данных:
Прикрепил файл с таблицами на разных листах в файле Excel



1. Employee
2. Salary
3. Project
4. EmployeeProject
5. Position
6. DepartmentType
7. Department
8. Address


## 1.	Employee

```
Employee(
  EmployeeId PRIMERY KEY smallserial,
  EmployeeFullName varchar(128),
  DateHiring date,
  SalaryId SECONDARY KEY smallint,);
```
## 2.	Salary

```
Salary(
  SalaryId PRIMERY KEY smallserial,
  PositionId SECONDARY KEY smallint,
  SalaryAmount integer);
```
## 3.	Project

```
Project(
  ProjectId PRIMERY KEY smallserial,
  ProjectName varchar(128));
```
## 4.	EmployeeProject

```
EmployeeProject(
  EmployeeId PRIMERY KEY smallserial,
  ProjectId SECONDARY KEY smallint);
```
## 5.	Position

```
Position(
  PositionId PRIMERY KEY smallserial,
  PositionName varchar(128));
  DepartmentId SECONDARY KEY smallint,
```
## 6.	DepartmentType

```
DepartmentType(
  DepartmentTypeId PRIMERY KEY smallserial,
  DepartmentTypeName varchar(128));
```
## 7.	Department

```
Department(
  DepartmentId PRIMERY KEY smallserial,
  DepartmentTypeId SECONDARY KEY smallint,
  DepartmentName varchar(128),
  AddressID SECONDARY KEY smallint,);
```
## 8.	Address

```
Address(
  AddressID PRIMERY KEY smallserial,
  DepartmentAddress varchar(128));
```


## Какие данные хранятся в этих таблицах;
Ответ в таблице:
https://1drv.ms/x/s!AtjLhewZ3c_dgacE_2KV1fyVXxrQUA?e=xL2yrk

## Какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.
Ответ в таблице:
https://1drv.ms/x/s!AtjLhewZ3c_dgacE_2KV1fyVXxrQUA?e=NDiYjN

