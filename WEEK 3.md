# EXERCISE 2

### Question 1
select * from goal;
![EX 2 Question 1.png](EX%202%20Question%201.png)

### Question 2
SELECT NAME, type FROM airport
WHERE iso_country = 'FI';
![EX 2 Question 2.png](EX%202%20Question%202.png)

### Question 3
SELECT NAME, type FROM airport
WHERE iso_country = 'FI'
AND NAME <> ' ht ri Airfield'
ORDER BY
NAME ASC;
![EX 2 Question 3.png](EX%202%20Question%203.png)

### Question 4
SELECT NAME, type FROM airport
WHERE iso_country ='FI'
ORDER BY
TYPE,
NAME;
![EX 2 Question 4.png](EX%202%20Question%204.png)

### Question 5
SELECT NAME FROM COUNTRY
WHERE NAME LIKE 'F%'
![EX 2 Question 5.png](EX%202%20Question%205.png)

### Question 6
SELECT NAME FROM country
WHERE NAME LIKE '%F%'
![EX 2 Question 6.png](EX%202%20Question%206.png)

### Question 7
select location from game where screen_name="Vesa";
![EX 2 Question 7.png](EX%202%20Question%207.png)

### Question 8
select c02_budget from game where screen_name="llkka"
![EX 2 Question 8.png](EX%202%20Question%208.png)

### Question 9
select distinct co2_budget from game;
![EX 2 Question 9.png](EX%202%20Question%209.png)

### Question 10
SET @co2_left := (SELECT SUM(co2_budget - co2_consumed) FROM game where screen_name ='Ilkka');

SELECT screen_name, co2_budget, co2_consumed, @co2_left FROM game where screen_name ='Ilkka';
![EX 2 Question 10.png](EX%202%20Question%2010.png)

# EXERCISE 3

### Question 1
SELECT CO.name AS country_name, AIR.name AS airport_name  
FROM country AS CO
LEFT OUTER JOIN airport AIR ON AIR.iso_country = CO.iso_country  
WHERE CO.name='Iceland'
![Exercise 3 Q 1.png](Exercise%203%20Q%201.png)

### Question 2
SELECT airport.name AS "airport name"  
FROM airport INNER JOIN country  
ON airport.iso_country = country.iso_country  
WHERE country.name = 'France' AND airport.type = 'large_airport';
![Exercise 3 Q 2.png](Exercise%203%20Q%202.png)

### Question 3
SELECT country.name AS "country_name", airport.name AS "airport_name" 
FROM airport INNER JOIN country  
ON airport.iso_country = country.iso_country  
WHERE country.continent='an';
![Exercise 3 Q 3.png](Exercise%203%20Q%203.png)

### Question 4
select airport.elevation_ft from game, 
airport where airport.ident = game.location 
and game.screen_name="heini";
![Exercise 3 Q 4.png](Exercise%203%20Q%204.png)

### Question 5
select airport.elevation_ft * 0.3048 as elevation_m from game,
airport where airport.ident = game.location  
and game.screen_name="heini";
![Exercise 3 Q 5.png](Exercise%203%20Q%205.png)

### Question 6
select airport.name from game,
airport where airport.ident = game.location 
and game.screen_name="Ilkka";
![Exercise 3 Q 6.png](Exercise%203%20Q%206.png)

### Question 7
SELECT country.name FROM game 
JOIN airport ON airport.ident = game.location 
INNER JOIN country ON country.iso_country = airport.iso_country 
WHERE game.screen_name="Ilkka";
![Exercise 3 Q 7.png](Exercise%203%20Q%207.png)

### Question 8
select goal.name from goal
INNER JOIN goal_reached ON goal.id = goal_reached.goal_id 
INNER JOIN game on goal_reached.game_id = game.id
WHERE game.screen_name="heini"
![Exercise 3 Q 8.png](Exercise%203%20Q%208.png)

### Question 9
select airport.name FROM airport 
INNER JOIN game ON airport.ident = game.location   
INNER JOIN goal_reached ON game.id = goal_reached.game_id 
INNER JOIN goal ON goal_reached.goal_id = goal.id 
WHERE goal.name = 'clouds' AND game.screen_name='Ilkka';
![Exercise 3 Q 9.png](Exercise%203%20Q%209.png)

### Question 10
SELECT country.name FROM airport  
INNER JOIN game ON airport.ident = game.location  
INNER JOIN goal_reached ON game.id = goal_reached.game_id  
INNER JOIN goal ON goal_reached.goal_id = goal.id  
INNER JOIN country ON airport.iso_country = country.iso_country  
WHERE goal.name = 'clouds' AND game.screen_name='Ilkka';
![Exercise 3 Q 10.png](Exercise%203%20Q%2010.png)