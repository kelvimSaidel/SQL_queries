## Identifyng triangles

Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table:

Equilateral: It's a triangle with  sides of equal length.  
Isosceles: It's a triangle with  sides of equal length.  
Scalene: It's a triangle with  sides of differing lengths.  
Not A Triangle: The given values of A, B, and C don't form a triangle.  

### Input Format  

The TRIANGLES table is described as follows:

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/1628d185cd415807c11c6c666b5f7fdcaec59b34/basic/assets/triangles4.JPG)


Each row in the table denotes the lengths of each of a triangle's three sides.

### Sample Input

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/1628d185cd415807c11c6c666b5f7fdcaec59b34/basic/assets/triangles2.JPG)


### Sample Output

Isosceles  
Equilateral  
Scalene  
Not A Triangle  


### Explanation

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/1628d185cd415807c11c6c666b5f7fdcaec59b34/basic/assets/triangles3.JPG)


### How to run this project?


#### Precondition: Oracle SQL Developer

```SQL

-- create table triangles

create table triangles
( a integer,
  b integer,
  c integer);

-- inserting records

insert into triangles(a,b,c) values(10, 10, 10);
insert into triangles(a,b,c) values(11, 11, 11);
insert into triangles(a,b,c) values(30, 32, 30);
insert into triangles(a,b,c) values(40, 40, 40);
insert into triangles(a,b,c) values(20, 20, 21);
insert into triangles(a,b,c) values(21, 21, 21);
insert into triangles(a,b,c) values(20, 22, 21);
insert into triangles(a,b,c) values(20, 20, 40);
insert into triangles(a,b,c) values(20, 22, 21);
insert into triangles(a,b,c) values(30, 32, 41);
insert into triangles(a,b,c) values(50, 22, 51);
insert into triangles(a,b,c) values(20, 12, 61);
insert into triangles(a,b,c) values(20, 22, 50);
insert into triangles(a,b,c) values(50, 52, 51);
insert into triangles(a,b,c) values(80, 80, 80);

```

### Solution

```SQL

select
case when (a+b) <= c then
'Not A Triangle'
when a=b and b=c then
'Equilateral'
when (a=b) or (b=c) or (a=c) then
'Isosceles'
when a!=b and b!=c then
'Scalene' end
from triangles; 

```

### Results

```SQL

Equilateral
Equilateral
Isosceles
Equilateral
Isosceles
Equilateral
Scalene
Not A Triangle
Scalene
Scalene
Scalene
Not A Triangle
Not A Triangle
Scalene
Equilateral

```

## Autor

Kelvim Silva Saidel

www.linkedin.com/in/ksaidel  
www.hackerrank.com/ksaidel
