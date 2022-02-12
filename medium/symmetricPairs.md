# Symmetric pairs

You are given a table, Functions, containing two columns: X and Y.

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/b4e6d21df82f283046e35c80a305d75adf8f15c9/medium/assets/symmetricPairs1.JPG)

Two pairs (X , Y ) and (X , Y ) are said to be symmetric pairs if X = Y and X = Y .
Write a query to output all such symmetric pairs in ascending order by the value of X.
Sample Input

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/b4e6d21df82f283046e35c80a305d75adf8f15c9/medium/assets/symmetricPairs2.JPG)
 
Sample Output  

20 20  
20 21  
22 23  

## How to run this project?

Precondition: Oracle SQL Developer

```SQL

-- create table functions

create table functions (
x integer,
y integer);

-- inserting records

insert into functions(x,y) values(86, 86); 
insert into functions(x,y) values(27, 27);
insert into functions(x,y) values(45, 45);
insert into functions(x,y) values(95, 95);
insert into functions(x,y) values(11, 11);
insert into functions(x,y) values(18, 8 );
insert into functions(x,y) values(85, 85);
insert into functions(x,y) values(2 ,2  );
insert into functions(x,y) values(77, 77);
insert into functions(x,y) values(91, 91);
insert into functions(x,y) values(15, 15);
insert into functions(x,y) values(84, 84);
insert into functions(x,y) values(51, 51);
insert into functions(x,y) values(32, 32);
insert into functions(x,y) values(35, 35);
insert into functions(x,y) values(8 ,8  );
insert into functions(x,y) values(92, 92);
insert into functions(x,y) values(67, 67);
insert into functions(x,y) values(62, 62);
insert into functions(x,y) values(33, 33);
insert into functions(x,y) values(13, 13);
insert into functions(x,y) values(15, 11);
insert into functions(x,y) values(18, 18);
insert into functions(x,y) values(3 ,3  );
insert into functions(x,y) values(38, 38);
insert into functions(x,y) values(80, 80);
insert into functions(x,y) values(34, 34);
insert into functions(x,y) values(6 ,6  );
insert into functions(x,y) values(72, 72);
insert into functions(x,y) values(14, 12);
insert into functions(x,y) values(44, 44);
insert into functions(x,y) values(4 ,22 );
insert into functions(x,y) values(90, 90);
insert into functions(x,y) values(47, 47);
insert into functions(x,y) values(78, 78);
insert into functions(x,y) values(23, 3 );
insert into functions(x,y) values(42, 42);
insert into functions(x,y) values(56, 56);
insert into functions(x,y) values(79, 79);
insert into functions(x,y) values(55, 55);
insert into functions(x,y) values(65, 65);
insert into functions(x,y) values(17, 17);
insert into functions(x,y) values(64, 64);
insert into functions(x,y) values(4 ,4  );
insert into functions(x,y) values(28, 28);
insert into functions(x,y) values(19, 19);
insert into functions(x,y) values(17, 9 );
insert into functions(x,y) values(36, 36);
insert into functions(x,y) values(25, 25);
insert into functions(x,y) values(81, 81);
insert into functions(x,y) values(60, 60);
insert into functions(x,y) values(48, 48);
insert into functions(x,y) values(5 ,5  );
insert into functions(x,y) values(88, 88);
insert into functions(x,y) values(7 ,19 );
insert into functions(x,y) values(21, 21);
insert into functions(x,y) values(29, 29);
insert into functions(x,y) values(52, 52);
insert into functions(x,y) values(9 ,17 );
insert into functions(x,y) values(9 ,9  );
insert into functions(x,y) values(13, 13);
insert into functions(x,y) values(16, 10);
insert into functions(x,y) values(1 ,1  );
insert into functions(x,y) values(31, 31);
insert into functions(x,y) values(46, 46);
insert into functions(x,y) values(7 ,7  );
insert into functions(x,y) values(58, 58);
insert into functions(x,y) values(23, 23);
insert into functions(x,y) values(87, 87);
insert into functions(x,y) values(83, 83);
insert into functions(x,y) values(66, 66);
insert into functions(x,y) values(93, 93);
insert into functions(x,y) values(24, 2 );
insert into functions(x,y) values(98, 98);
insert into functions(x,y) values(53, 53);
insert into functions(x,y) values(20, 6 );
insert into functions(x,y) values(61, 61);
insert into functions(x,y) values(20, 20);
insert into functions(x,y) values(96, 96);
insert into functions(x,y) values(99, 99);
insert into functions(x,y) values(73, 73);
insert into functions(x,y) values(2 ,24 );
insert into functions(x,y) values(14, 14);
insert into functions(x,y) values(71, 71);
insert into functions(x,y) values(5 ,21 );
insert into functions(x,y) values(22, 4 );
insert into functions(x,y) values(75, 75);
insert into functions(x,y) values(6 ,20 );
insert into functions(x,y) values(97, 97);
insert into functions(x,y) values(41, 41);
insert into functions(x,y) values(26, 26);
insert into functions(x,y) values(22, 22);
insert into functions(x,y) values(8 ,18 );
insert into functions(x,y) values(74, 74);
insert into functions(x,y) values(40, 40);
insert into functions(x,y) values(21, 5 );
insert into functions(x,y) values(94, 94);
insert into functions(x,y) values(76, 76);
insert into functions(x,y) values(49, 49);
insert into functions(x,y) values(11, 15);
insert into functions(x,y) values(59, 59);
insert into functions(x,y) values(89, 89);
insert into functions(x,y) values(68, 68);
insert into functions(x,y) values(24, 24);
insert into functions(x,y) values(37, 37);
insert into functions(x,y) values(12, 12);
insert into functions(x,y) values(63, 63);
insert into functions(x,y) values(43, 43);
insert into functions(x,y) values(16, 16);
insert into functions(x,y) values(100, 100);
insert into functions(x,y) values(39 ,39);
insert into functions(x,y) values(25 ,1 );
insert into functions(x,y) values(69 ,69);
insert into functions(x,y) values(54 ,54);
insert into functions(x,y) values(50 ,50);
insert into functions(x,y) values(30 ,30);
insert into functions(x,y) values(10 ,10);

```

Solution

```SQL

SELECT a.X, a.Y
FROM FUNCTIONS A, FUNCTIONS B
WHERE b.y = a.x 
and b.x = a.y
and a.y >= a.x
GROUP BY a.X, a.Y
having count(*) > 1 or a.y>a.x
order by a.x asc;

```

Results

```SQL

2 24 
4 22 
5 21 
6 20 
8 18 
9 17 
11 15
13 13

```

## Autor

Kelvim Silva Saidel

www.linkedin.com/in/ksaidel  
www.hackerrank.com/ksaidel
