# MYSQL

# MYSQL Query

# Create a table in  MYSQL 

create a database employees
use database employees;

create a table emp_detalis (
id int unsigned,
first_name varchar (26),
last_name varchar (27),
age int,
sex char (1),
doj date,
city varchar (18),
salary float
);

describe emp_detalis;

# Add data into table useing insert Query

insert into emp_detalis

values (001,"sam","lora",27,"M","2022-1-18","Boston",70000),
(002,"mona","sen",30,"F","2022-1-18","Boston",74000),
(003,"june","waston",26,"F","2022-1-18","new york",55000),
(004,"dev","ray",29,"M","2022-1-18","Los Angeles", 60000),
(005,"sara","lora",25,"F","2022-1-18","new york",45000),
(006,"sara","ray",35,"F","2022-1-18","Los Angeles",65000),
(007,"dev","roy",29,"M","2022-2-10","Boston",68000),
(008,"joy","waston",27,"M","2022-2-10","California",45000),
(009,"sara","jones",28,"F","2022-2-10","California",59500),
(0010"jarry","jones",30,"M","2022-2-10","Texas",65000),
(0011,"mike","roy",35,"M","2022-2-17","Texas",65000),
(0012,"tom","Alex",38,"M","2022-2-17","Texas",84000),
(0013,"manu","Lucas",32,"M","2022-2-17","Houston",90000),
(0014,"steven","Wood",33,"M","2022-2-17","Houston",98000),
(0015,"Monica","roy",33,"F",2022-3-10","Arizona",87000),
(0016,"Monica","lora",35,"F",2022-3-10","Arizona",82000),
(0017,"steve","smith",31,"M",2022-3-10","California",62000),
(0018,"shane","smith",39,"M",2022-3-17","California",100000),
(0019,"Alex","wood",33,"F",2022-3-20","Texas",89000),
(0020,"dwayne","simth",36,"M","2022-4-12","San Francisco",87000),
(0021,"dwayne","wood",31,"M","2022-4-15","San Francisco",55000),
(0022,"dev","wood",23,"M","2022-4-18","Arizona",64000),
(0023,"michel","jordan",27,"M","2022-4-20","Austin",52000),
(0024,"michel","ray",24,"M","2022-4-22","Austin",30000),
(0025,"mike","wood",26,"M","2022-4-23","North Carolina",44000),
(0026,"lara","jones",34,"F",2022-4-23","North Carolina",43000),
(0027,"june","wood",29,"F","2022-4-30","Boston",47000),
(0028,"may","roy",30,"F","2022-5-1","North Carolina",53000),
(0029,"marry","lara",26,"F","2022-5-1","Georgia",35000),
(0030,"lara","lara",38,"F","2022-5-5","Georgia",120000),
(0031,"harry","jones",40,"M","2022-5-11","Georgia",130000),
(0032,"smith","lucas",41,"M","2022-5-11","Georgia",130000),
(0033,"david","simth",45,"M","2022-6-17","Florida",180000),
(0034,"david","wood",40,"M","2022-6-21","Florida",110000),
(0035,"shone","wehner",38,"M","2022-7-14","Florida",100000),
(0036,"steve","smith",36,"M","2022-7-14","Colorado",75800),
(0037,"indian","jones",31,"M","2022-7-19","Colorado",88000),
(0038,"mark","wood",45,"M","2022-8-12","Colorado",170000),
(0039,"mariam","jones",32,"F","2022-8-12","Virginia",56000),
(0040,"mariam","roy",31,"F","2022-8-19","Virginia",79000);

# Checke emp_details useing select Qurey in mysql 

select * from emp_details;

select distinct city from emp_details;



# MySQL Select Query with Where Clause

select * from emp_details where first_name ='david','dev';
select * from emp_details where first_name = 'david' AND sex = 'M';
select * from emp_details where first_name = 'marian' AND sex = 'F';
select * from emp_details where first_name = 'dev' or first_name = 'mariam';
select * from emp_details where age > 30;
select * from emp_details where age < 25;
select * from emp_details where age > 30 AND sex = 'M';
select first_name,sex,city from emp_details where sex = 'F';
select * from emp_details where city = 'California' or city = 'Colorado';
select * from emp_details where city = ('California','Colorado');

# Operation precedence and logical order-solution 

select * from emp_details where sex ='M' AND (first_name = 'sam' or first_name ='indian');
select * from emp_details where first_name = 'indian'or'sam'or'lara';
select * from emp_details where first_name in ('indian','sam','lara');

# Using in NOT IN Solution 

select * from emp_details where first_name not in ('indian','sam','lara');
select * from emp_details where city not in ('Austin','Boston');

# MySQL And & OR Operator Commands

where age=>21 AND age<=37;
where salary=>30000 AND salary<=90000;
where age=>21 AND age<=37 AND city = "Houston";
where age=>21 AND age<=37 AND city = "Houston" AND sex = 'M';
where salary=>30000 AND salary<=90000 AND sex = 'F';






















