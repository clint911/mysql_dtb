# mysql_dtb
mysql database assignment program
create database jkuat;
use jkuat;
create table campus(campus_name varchar(30) not null, 
location varchar(30) not null,
primary key(campus_name));
create table schools(
school_name varchar(30) not null,
campus_name varchar(30) not null,


