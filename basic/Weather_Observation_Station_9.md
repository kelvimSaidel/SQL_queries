## Weather Observation Station

![CONCEPTUAL_DATA_MODEL](https://github.com/kelvimSaidel/SQL_queries/blob/5a54f64ddb89cf1340aa5986ac2ebc36fb3506a6/basic/assets/w01.JPG)

### How to run this project?


#### Precondition: Oracle SQL Developer

```SQL

-- create table Station

create table station
(
id number,
city varchar2(21),
state varchar2(2),
lat_n number,
long_w number
);

-- inserting records


insert into station (id,city,state,lat_n,long_w) values (794,rtrim('Kissee Mills   '),'MO', 140, 73 );
insert into station (id,city,state,lat_n,long_w) values (824,rtrim('Loma Mar       '),'CA', 49 , 131);
insert into station (id,city,state,lat_n,long_w) values (603,rtrim('Sandy Hook     '),'CT', 72 , 148);
insert into station (id,city,state,lat_n,long_w) values (478,rtrim('Tipton IN      '),'34', 98 , ''  );
insert into station (id,city,state,lat_n,long_w) values (619,rtrim('Arlington      '),'CO', 75 , 93 );
insert into station (id,city,state,lat_n,long_w) values (711,rtrim('Turner         '),'AR', 50 , 101);
insert into station (id,city,state,lat_n,long_w) values (839,rtrim('Slidell        '),'LA', 85 , 152);
insert into station (id,city,state,lat_n,long_w) values (411,rtrim('Negreet        '),'LA', 99 , 105);
insert into station (id,city,state,lat_n,long_w) values (588,rtrim('Glencoe        '),'KY', 46 , 136);
insert into station (id,city,state,lat_n,long_w) values (665,rtrim('Chelsea        '),'IA', 99 , 60 );
insert into station (id,city,state,lat_n,long_w) values (342,rtrim('Chignik Lagoon '),'AK', 103, 153);
insert into station (id,city,state,lat_n,long_w) values (733,rtrim('Pelahatchie    '),'MS', 39 , 28 );
insert into station (id,city,state,lat_n,long_w) values (441,rtrim('Hanna City     '),'IL', 51 , 137);
insert into station (id,city,state,lat_n,long_w) values (811,rtrim('Dorrance       '),'KS', 102, 122);
insert into station (id,city,state,lat_n,long_w) values (698,rtrim('Albany         '),'CA', 50 , 80 );
insert into station (id,city,state,lat_n,long_w) values (325,rtrim('Monument       '),'KS', 71 , 142);
insert into station (id,city,state,lat_n,long_w) values (414,rtrim('Manchester     '),'MD', 74 , 37 );
insert into station (id,city,state,lat_n,long_w) values (113,rtrim('Prescott       '),'IA', 40 , 66 );

```

### Solution

```SQL

select DISTINCT city 
FROM station
WHERE lower(substr(city, 1, 1)) 
NOT IN ('a','e','i','o','u');

```

### Results

```SQL

Negreet
Glencoe
Hanna City
Tipton IN
Dorrance
Prescott
Chignik Lagoon
Slidell
Loma Mar
Sandy Hook
Turner
Manchester
Kissee Mills
Monument
Chelsea
Pelahatchie

```

## Autor

Kelvim Silva Saidel

www.linkedin.com/in/ksaidel  
www.hackerrank.com/ksaidel
