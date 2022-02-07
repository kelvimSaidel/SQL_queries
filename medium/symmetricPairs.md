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
