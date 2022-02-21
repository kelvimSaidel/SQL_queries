


## Higher than 75 mark


![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/e87a0231829f03ca2e564bedac2263da44e7b390/basic/assets/students75.JPG)


![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/e87a0231829f03ca2e564bedac2263da44e7b390/basic/assets/students752.JPG)


### How to run this project?


#### Precondition: Oracle SQL Developer

```SQL

-- create table students

create table students
(
id integer,
name varchar2(20),
marks integer
);

-- inserting records

insert into students(id,name,marks) values(19, rtrim('Samantha '), 87);
insert into students(id,name,marks) values(21, rtrim('Julia    '), 96);
insert into students(id,name,marks) values(11, rtrim('Britney  '), 95);
insert into students(id,name,marks) values(32, rtrim('Kristeen '),100);
insert into students(id,name,marks) values(12, rtrim('Dyana    '), 55);
insert into students(id,name,marks) values(13, rtrim('Jenny    '), 66);
insert into students(id,name,marks) values(14, rtrim('Christene'), 88);
insert into students(id,name,marks) values(15, rtrim('Meera    '), 24);
insert into students(id,name,marks) values(16, rtrim('Priya    '), 76);
insert into students(id,name,marks) values(17, rtrim('Priyanka '), 77);
insert into students(id,name,marks) values(18, rtrim('Paige    '), 74);
insert into students(id,name,marks) values(19, rtrim('Jane     '), 64);
insert into students(id,name,marks) values(21, rtrim('Belvet   '), 78);
insert into students(id,name,marks) values(31, rtrim('Scarlet  '), 80);
insert into students(id,name,marks) values(41, rtrim('Salma    '), 81);
insert into students(id,name,marks) values(51, rtrim('Amanda   '), 34);
insert into students(id,name,marks) values(61, rtrim('Heraldo  '), 94);
insert into students(id,name,marks) values(71, rtrim('Stuart   '), 99);
insert into students(id,name,marks) values(81, rtrim('Aamina   '), 77);
insert into students(id,name,marks) values(76, rtrim('Amina    '), 89);
insert into students(id,name,marks) values(91, rtrim('Vivek    '), 84);
insert into students(id,name,marks) values(17, rtrim('Evil     '), 79);
insert into students(id,name,marks) values(16, rtrim('Devil    '), 76);
insert into students(id,name,marks) values(34, rtrim('Fanny    '), 75);
insert into students(id,name,marks) values(38, rtrim('Danny    '), 75);

```

### Solution

```SQL

select  name from students 
where marks > 75
order by substr(name,-3,3) , ID asc;

```

### Results

```SQL

Stuart
Kristeen
Christene
Amina
Aamina
Priya
Heraldo
Scarlet
Julia
Salma
Britney
Priyanka
Samantha
Vivek
Belvet
Devil
Evil

```

## Autor

Kelvim Silva Saidel

www.linkedin.com/in/ksaidel  
www.hackerrank.com/ksaidel
