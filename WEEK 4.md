# EXERCISE 4

### Question 1
Select country.name as "country name", 
airport.name as "airport name" from country inner join airport on airport.iso_country = country.iso_country where country.name = "Finland"and scheduled_service = "yes";
![EX 4 Question 1.png](EX%204%20Question%201.png)

### Question 2
select screen_name, airport.name from game inner join airport on location = ident;
![EX 4 Question 2.png](EX%204%20Question%202.png)

### Question 3
select screen_name, country.name from game inner join airport on location = ident
inner join country on airport.iso_country = country.iso_country;
![EX 4 Question 3.png](EX%204%20Question%203.png)

### Question 4
select airport.name, screen_name from airport left join game on ident = location where airport.name like "%Hels%";
![EX 4 Question 4.png](EX%204%20Question%204.png)

### Question 5
select name, screen_name from goal left join goal_reached on goal.id = goal_id left join game on game.id = game_id;
![EX 4 Question 5.png](EX%204%20Question%205.png)

# EXERCISE 5

### Question 1
select name from country where iso_country in (select iso_country from airport where name like "Satsuma%");
![EX 5 Question S 1.png](EX%205%20Question%20S%201.png)

### Question 2
select name from airport where iso_country in (select iso_country from country where country.name = "Monaco");
![EX 5 Question S 2.png](EX%205%20Question%20S%202.png)

### Question 3
Select screen_name from game where id in(select game_id from goal_reached where goal_id in(select id from goal where name ="CLOUDS"));
![EX 5 Question S 3.png](EX%205%20Question%20S%203.png)

### Question 4
Select country.name from country where iso_country not in (select airport.iso_country from airport);
![EX 5 Question S 4 .png](EX%205%20Question%20S%204%20.png)

### Question 5
select name from goal where id not in (select goal.id from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini");
![EX 5 Question S 5.png](EX%205%20Question%20S%205.png)