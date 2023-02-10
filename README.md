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
(0016,"Monica","lora",35,"F","2022-3-10","Arizona",82000),
(0017,"steve","smith",31,"M","2022-3-10","California",62000),
(0018,"shane","smith",39,"M","2022-3-17","California",100000),
(0019,"Alex","wood",33,"F","2022-3-20","Texas",89000),
(0020,"dwayne","simth",36,"M","2022-4-12","San Francisco",87000),
(0021,"dwayne","wood",31,"M","2022-4-15","San Francisco",55000),
(0022,"dev","wood",23,"M","2022-4-18","Arizona",64000),
(0023,"michel","jordan",27,"M","2022-4-20","Austin",52000),
(0024,"michel","ray",24,"M","2022-4-22","Austin",30000),
(0025,"mike","wood",26,"M","2022-4-23","North Carolina",44000),
(0026,"lara","jones",34,"F","2022-4-23","North Carolina",43000),
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

# Checke emp_details using select Qurey in mysql 

select * from
emp_details;

select distinct city from 
emp_details;



# MySQL Select Query with Where Clause

select * from
emp_details
where 
first_name ='david','dev';

select * from 
emp_details
where
first_name = 'david' AND sex = 'M';

select * from
where
first_name = 'marian' AND sex = 'F';

select * from 
emp_details
where 
first_name = 'dev' or first_name = 'mariam';

select * from 
emp_details 
where 
age > 30;

select * from
emp_details
where 
age < 25;

select * from 
emp_details
where
age > 30 AND sex = 'M';

select 
first_name,
sex,
city from
emp_details
where sex = 'F';

select * from
emp_details
where
city = 'California' or city = 'Colorado';

select * from
emp_details
where city = ('California','Colorado');

# Operation precedence and logical order  

select * from
emp_details 
where 
sex ='M'
AND 
(first_name = 'sam' or first_name ='indian');

select * from
emp_details
where 
first_name = 'indian'or'sam'or'lara';

select * from 
emp_details
where
first_name in ('indian','sam','lara');

# Using in NOT IN 

select * from
emp_details
where
first_name not in ('indian','sam','lara

select * from
emp_details
where city not in ('Austin','Boston');

# MySQL And  Operator Commands

where age=>21
AND 
age<=37;

where salary=>30000
AND 
salary<=90000;

where age=>21
AND 
age<=37
AND 
city = "Houston";

where age=>21
AND 
age<=37
AND
city = "Houston" AND sex = 'M';

where salary=>30000
AND 
salary<=90000 AND sex = 'F';


# Using LIKE-NOT-LIKE-
select * from
where
first_name like ('mark');

select * from
emp_details
where
hire_date like ('2022-2-10');

select * from
emp_details 
where id like ('0022');

# Using Between and NOT Operators  Solution 
select * from 
salary where 
salary Between 35000 AND 70000;

select * from
emp_details 
where id not Between '002' AND '0010';

# Using is NOT NULL - IS NULL 
select first_name 
from
id where salary is not null;

# Using other comparison operators 
select * from
emp_details
where 
doj_date > = '2022-5-1'
AND sex = 'F';

select * from 
emp_details
where
first_name > = 'marry'
AND salary = '35000';

select * from 
salary where 
salary >55000;

# Using select Distin 

select distin 
doj_date 
from 
emp_details;

# count ()
select 
count(name) 
from emp_details;

select
count(name) 
as
count_name
from 
emp_details;

select
sum(salary) 
from
emp_details;

select
avg(salary)
from
emp_details;

select
count(column_name)
from
table_name;

# getting to know Aggregate function solution 

select 
count (*)
from 
salary 
where 
salary>=100000;

select
count(*)
from
emp_id;

# Using Order by 
select * 
from 
emp_details 
ORDER BY 
doj_date DESC;

# Group by 
select 
first_name
from 
emp_details
group by 
first_name;

select 
count(first_name)
from
emp_details
group by 
first_name;

select
first_name, 
count(first_name)
as name_count from
emp_details
group by 
first_name order by first name;

# using ali as (AS) 
select salary, 
count (emp_id)
as emp_with_sum_salary
from salary
where 
salary>80000
group by salary ,
order by salary;

# Using HAVING 
select * from 
emp_details 
HAVING 
doj_date > = '2022-4-30';

select first_name, count(first_name) as name_count from emp_details GROUP BY first_name HAVING count (first_name)>15 ORDER by first_name;

select * 
avg(salary)
from 
salary group by 
emp_id
Having
avg (salary) > 120000;

select
emp_id,
avg(salary)
from salary
group by
emp_id
HAVING
avg (salary) > 120000
order by emp_id;

# count() - an aggregate function - HAVING #

# using where and having 
select
emp_id
from 
first_name
where 
from_date > '2022-3-20' 
Group by
emp_details
having count (from_date)> 1
order by emp_id;

# Using limit 
select * from emp_details limit 20;

# Join 
** creat and fill in the 'department_dup' table using the following code drop table if exists deparments_dept;** 
creat table deparment_dept
(
dept_no char(4) null,
dept_name varchar (40) null
);

insert into deparment_details(
dept_no
dept_name
);

select * from deparments;

insert into deparment_details(dept_name)

values ('public relation');

delete from deparments_details
where 
  dept_no = 'd002';
  
 insert into deparments_dup(dept_no)
  values ('dolo'),('doll');
  
  insert into dept_manage_dup
  
  select * from dept_manage;
  
  insert into dept_manager_dup (emp_id, fromdate )
 values (005,'2017-01-01'),
 (006,'2017-01-01')
 (007,'2017-01-01');
 
 Delete from dept_manager_dup
 where 
     dept_no = 'dooi';
# inner join 

select
table_1.column_name(s),
table_2. column_name(s)
from 
table_1
join table_2
on table_1.
column_name = table_2.
column_name;

# the functionnality of left join 
 select
 e.emp_no,
 e.first_name,
 e.last_name,
 dm.dept_no,
 dm.from_date,
 from employees 
 left join
 dept_manager dm on e.emp_no = dm.emp-no
 where
 e.last_name = 'ray'
 order by dm.dept_no DESC, e.emp_no;
 
 # Diffrent betweens the new and the old join sytax 
 ** extract a list containing information about all managers amployees number,first nd last name deoarments number and doj date use the old type of join syntax to obtain ,
 select
 e.emp_id,
 e.first_name,
 e.last_name,
 dm.dept_no,
 dm.doj_date
 from employees ,
 dept_manager dm 
 where e.emp_no = dm.emp_id;
 
 # Using join and where together 
 
 select 
 e.first_name,
 e.last_name,
 e.doj_date,
 t.title
 from employees e 
 join title t on e.emp_id = t.emp_no
 where 
 first_name = "sam"
 AND last_name = "ray"
 Order by e.emp_id
 ;
 
 # the functionality of cross join 
 
 select 
 dm *d* 
 from 
 deparments d
 where 
 d.dept_no = 'doo3'
 order by d.dept_name;
 
 # join more than two table 
 
 select
 e.first_name,
 e.last_name,
 e.doj_date,
 t.title,
 m.from_date,
 d.dept_name
 from employees 
 join
 dept_manager m on e.emp_no = m.emp_id
 join
 deparments d on m.dept_on = d.dept_id
 join 
 tittle t on e.emp_no = t.emp_id 
 where
 t.title = 'manager'
 Order by
 e.emp_no;
 
 select
 e.first_name,
 e.last_name,
 e.doj_date,
 t.title,
 m.from_date,
 d.dept_name
 from employees 
 join
 dept_manager m on e.emp_no = m.emp_id
 join
 deparments d on m.dept_on = d.dept_id
 join 
 tittle t on e.emp_no = t.emp_id 
 AND
 m from_date = t.from_date
 Order by 
 e.emp_no;
 
 # Between Union and Unionall
 
 select *
 from
 (select 
 e.emp_no,
 e.first_name,
 e.last_name,
 NULL AS dept_no,
 NULL AS from_date
 from
 employees e 
 where 
 last_name = 'waston' union 
 NULL AS emp_id
 null as first_name,
 null as last_name,
 dm.dept_no,
 dm.from_date
 from 
 dept_manager dm) as a 
 order by
 e.emp_id DESC;
 
 # Mysql subqueries with in embeded inside
 
 select *
 from 
 dept_manger
 where
 emp_no in (select
 emp_id 
 from employees 
 where
 doj_date 
 between '2022-1-18' AND '2022-6-17');
 
 
 
 
  







































