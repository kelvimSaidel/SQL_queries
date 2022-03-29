# Binary Tree

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/fe990ec25f3e45616a887ca7cbb70b63c29df668/medium/assets/binaryTree1.JPG)
![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/fe990ec25f3e45616a887ca7cbb70b63c29df668/medium/assets/binaryTree2.JPG)
![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/fe990ec25f3e45616a887ca7cbb70b63c29df668/medium/assets/binaryTree3.JPG)

### How to run this project?

#### Precondition: Oracle SQL Developer

```SQL

-- create table bst

create table bst
(
n number,
p number
);

-- inserting records

  
insert into bst(n,p) values(1,2);
insert into bst(n,p) values(3,2);
insert into bst(n,p) values(5,6);
insert into bst(n,p) values(7,6);
insert into bst(n,p) values(2,4);
insert into bst(n,p) values(6,4);
insert into bst(n,p) values(4,15);
insert into bst(n,p) values(8,9);
insert into bst(n,p) values(10,9);
insert into bst(n,p) values(12,13);
insert into bst(n,p) values(14,13);
insert into bst(n,p) values(9,11);
insert into bst(n,p) values(13,11);
insert into bst(n,p) values(11,15);
insert into bst(n,p) values(15,NULL);

```

### Solution

```SQL

select n,'Root'
from bst
where p is null
union all
select n,'Inner'
from bst
where n in (select p
           from bst
           where p is not null)
and n not in (select n 
             from bst 
             where p is null)
union all
select n, 'Leaf'
from bst 
where n not in (select p
               from bst
               where p is not null)
order by n;

```

### Results

```SQL

1 Leaf 
2 Inner 
3 Leaf 
4 Inner 
5 Leaf 
6 Inner 
7 Leaf 
8 Leaf 
9 Inner 
10 Leaf 
11 Inner 
12 Leaf 
13 Inner 
14 Leaf 
15 Root

```

## Autor

Kelvim Silva Saidel

www.linkedin.com/in/ksaidel  
www.hackerrank.com/ksaidel
