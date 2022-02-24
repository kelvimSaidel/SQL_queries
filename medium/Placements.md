# Placements

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/ec07f183124921cded108e8fb3ccbe47132037e5/medium/assets/placements1.JPG)
![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/ec07f183124921cded108e8fb3ccbe47132037e5/medium/assets/placements2.JPG)
![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/ec07f183124921cded108e8fb3ccbe47132037e5/medium/assets/placements3.JPG)
![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/ec07f183124921cded108e8fb3ccbe47132037e5/medium/assets/placements4.JPG)


### How to run this project?

#### Precondition: Oracle SQL Developer

```SQL

-- create table students, friends and packages

create table students
(
id number,
name varchar2(20)
);


create table friends
(
id number,
friend_id number
);          

create table packages
(
id number,
salary float
);

-- inserting records

insert into students(id,name) values(1 ,  rtrim('Samantha ')); 
insert into students(id,name) values(2 ,  rtrim('Julia    ')); 
insert into students(id,name) values(3 ,  rtrim('Britney  ')); 
insert into students(id,name) values(4 ,  rtrim('Kristeen ')); 
insert into students(id,name) values(5 ,  rtrim('Dyana    ')); 
insert into students(id,name) values(6 ,  rtrim('Jenny    ')); 
insert into students(id,name) values(7 ,  rtrim('Christene')); 
insert into students(id,name) values(8 ,  rtrim('Meera    ')); 
insert into students(id,name) values(9 ,  rtrim('Priya    ')); 
insert into students(id,name) values(10,  rtrim('Priyanka ')); 
insert into students(id,name) values(11,  rtrim('Paige    ')); 
insert into students(id,name) values(12,  rtrim('Jane     ')); 
insert into students(id,name) values(13,  rtrim('Belvet   ')); 
insert into students(id,name) values(14,  rtrim('Scarlet  ')); 
insert into students(id,name) values(15,  rtrim('Salma    ')); 
insert into students(id,name) values(16,  rtrim('Amanda   ')); 
insert into students(id,name) values(17,  rtrim('Maria    ')); 
insert into students(id,name) values(18,  rtrim('Stuart   ')); 
insert into students(id,name) values(19,  rtrim('Aamina   ')); 
insert into students(id,name) values(20,  rtrim('Amina    ')); 


insert into friends(id,friend_id) values(1 ,14);
insert into friends(id,friend_id) values(2 ,15);
insert into friends(id,friend_id) values(3 ,18);
insert into friends(id,friend_id) values(4 ,19);
insert into friends(id,friend_id) values(5 ,20);
insert into friends(id,friend_id) values(6 ,5 );
insert into friends(id,friend_id) values(7 ,6 );
insert into friends(id,friend_id) values(8 ,7 );
insert into friends(id,friend_id) values(9 ,8 );
insert into friends(id,friend_id) values(10,1 );
insert into friends(id,friend_id) values(11,2 );
insert into friends(id,friend_id) values(12,3 );
insert into friends(id,friend_id) values(13,4 );
insert into friends(id,friend_id) values(14,9 );
insert into friends(id,friend_id) values(15,10);
insert into friends(id,friend_id) values(16,11);
insert into friends(id,friend_id) values(17,12);
insert into friends(id,friend_id) values(18,13);
insert into friends(id,friend_id) values(19,16);
insert into friends(id,friend_id) values(20,17);



insert into packages(id,salary) values (1 ,15.5  );
insert into packages(id,salary) values (2 ,15.6  );
insert into packages(id,salary) values (3 ,16.7  );
insert into packages(id,salary) values (4 ,18.8  );
insert into packages(id,salary) values (5 ,31.5  );
insert into packages(id,salary) values (6 ,45    );
insert into packages(id,salary) values (7 ,47    );
insert into packages(id,salary) values (8 ,46    );
insert into packages(id,salary) values (9 ,39    );
insert into packages(id,salary) values (10, 11.1 );
insert into packages(id,salary) values (11, 12.1 );
insert into packages(id,salary) values (12, 13.1 );
insert into packages(id,salary) values (13, 14.1 );
insert into packages(id,salary) values (14, 15.1 );
insert into packages(id,salary) values (15, 17.1 );
insert into packages(id,salary) values (16, 21.1 );
insert into packages(id,salary) values (17, 31.1 );
insert into packages(id,salary) values (18, 13.15);
insert into packages(id,salary) values (19, 33.33);
insert into packages(id,salary) values (20, 22.16);


```

### Solution

```SQL

with x as(select a.salary, c.name, b.id
           from packages a, friends b, students c
           where b.friend_id = a.id
           and b.id = c.id),
 y as(select a.salary, c.id
           from packages a, students c
           where c.id = a.id)
select x.name
from  (select  x.name, x.salary
from x, y
where  x.id = y.id
and  x.salary > y.salary
group by x.name, x.salary
order by max(x.salary) asc) x;

```

### Results

```SQL

Stuart 
Priyanka 
Paige 
Jane 
Julia 
Belvet 
Amina 
Kristeen 
Scarlet 
Priya 
Meera

```

## Autor

Kelvim Silva Saidel

www.linkedin.com/in/ksaidel  
www.hackerrank.com/ksaidel
