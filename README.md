# mysql_dtb
mysql database assignment program
create database jkuat;
use jkuat;
create table campus(campus_name varchar(30) not null, 
location varchar(30) not null,
PRIMARY KEY(campus_name));
create table schools(
school_name varchar(30) not null,
campus_name varchar(30) not null,
PRIMARY KEY (school_name),
FOREIGN KEY (campus_name)
REFERENCES campus(campus_name));
create table departments(
department_name varchar(30) not null,
department_head varchar(30) not null,
school_name varchar(30) not null,
PRIMARY KEY 
(department_name),
FOREIGN KEY
(school_name)
REFERENCES
schools(school_name));
create table students(
students_first_name varchar(30) not null,
students_last_name varchar(30) not null,
students_ID int not null,
students_reg_no varchar(23) not null,
students_DOB date not null,
campus_name varchar(30);
department_name varchar(30) not null,
school_name varchar(30) not null,
PRIMARY KEY (students_reg_no),
FOREIGN KEY (campus_name),
REFERENCES campus(campus_name),
FOREIGN KEY (department_name)
REFERENCES departments(department_name),
FOREIGN KEY (school_name)
REFERENCES schools(school_name));




