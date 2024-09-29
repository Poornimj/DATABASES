# EXERCISE 6

### Question 1
select max(elevation_ft) from airport;
![EX 6 Question 1.png](EX%206%20Question%201.png)

### Question 2
select continent, count(*) from country group by continent;
![EX 6 Question 2.png](EX%206%20Question%202.png)

### Question 3
select screen_name, count(*) from game, goal_reached where id = game_id group by screen_name;
![EX 6 Question 3.png](EX%206%20Question%203.png)

### Question 4
select screen_name from game where co2_consumed in(select min(co2_consumed) from game );
![EX 6 Question 4.png](EX%206%20Question%204.png)

### Question 5
select country.name, COUNT(*) from airport, 
country where airport.iso_country = country.iso_country group by country.iso_country order by COUNT(*) desc limit 50;
![EX 6 Question 5.png](EX%206%20Question%205.png)

### Question 6
select country.name from airport, 
country where airport.iso_country = country.iso_country group by country.iso_country having count(*) > 1000;
![EX 6 Question 6.png](EX%206%20Question%206.png)

### Question 7
select name from airport where elevation_ft in ( select max(elevation_ft) from airport );
![EX 6 Question 7.png](EX%206%20Question%207.png)

### Question 8
select name from country where iso_country in ( select iso_country from airport where elevation_ft in( select max(elevation_ft) from airport ) );
![EX 6 Question 8.png](EX%206%20Question%208.png)

### Question 9
select count(*) from game, goal_reached where id = game_id and screen_name = "Vesa" group by screen_name;
![EX 6 Question 9.png](EX%206%20Question%209.png)

### Question 10
select name from airport where latitude_deg in( select min(latitude_deg) from airport );
![EX 6 Question 10.png](EX%206%20Question%2010.png)

# EXERCISE 7

### Question 1
update game
set  location = (select ident from airport where name = "Nottingham Airport"), co2_consumed = co2_consumed+500
where screen_name = "Vesa";
![EX 7 Question 1.png](EX%207%20Question%201.png)

### Question 2
![EX 7 Question 2.png](EX%207%20Question%202.png)

### Question 3
delete from goal_reached;
![EX 7 Question 3.png](EX%207%20Question%203.png)

### Question 4
delete from game;
![EX 7 Question 4.png](EX%207%20Question%204.png)