# EXERCISE 2

### Question 1
select * from goal;
![Question 1.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EVPYEEhvXlFGmweLeOHha1gB5vzM-IqvgvQVTXjyGyl6vw?e=a1Ee9A)

### Question 2
SELECT NAME, type FROM airport
WHERE iso_country = 'FI';
![Question 2.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EVeHDpNP3LdFmhSxsQIHyzoBq7oIojc0E4j7X5_iTuY7UA?e=wd31ii)

### Question 3
SELECT NAME, type FROM airport
WHERE iso_country = 'FI'
AND NAME <> ' ht ri Airfield'
ORDER BY
NAME ASC;
![Question 3.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EYHjvQO8KhlIlKd7OpSRvcMBa4MKxeKlhn5UipHCa-umSA?e=pcSibR)

### Question 4
SELECT NAME, type FROM airport
WHERE iso_country ='FI'
ORDER BY
TYPE,
NAME;
![i![Question 4.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EWYWVeC_QVBCkZ2cmMsyQjcBQd2e5R5E9OhJRO8b4tn9lQ?e=mnsufY)

### Question 5
SELECT NAME FROM COUNTRY
WHERE NAME LIKE 'F%'
![Question 5.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EdmE1yiZ_lhGv8AEh7vWHBABnBz2CS1pl6bFhGWGYEBgqg?e=8tPmbz)

### Question 6
SELECT NAME FROM country
WHERE NAME LIKE '%F%'
![![Question 6.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/ERT2pFGgFaxPinEhji_M6IgBWOtcvpwTDl3xQnbEwtn-0w?e=BIhIAa)

### Question 7
select location from game where screen_name="Vesa";
![![Question 7.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EdoMq1hf6B9FvH3Z96Kq-cQBS-xnpn0b-G4VzHQ0WlL6cg?e=hoXKGV)

### Question 8
select c02_budget from game where screen_name="llkka"
![img![Question 8.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EbvyKfPyG6ZEhN0TfvkLGVABFuMgHt3qYa-OTyOHRy300A?e=gHUx8O)

### Question 9
select distinct co2_budget from game;
![![Question 9.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EUCpd574VsFLjtmOQrGHVuQB8U9zZFyTPOYB9oMM28-OAw?e=qeEH23)

### Question 10
SET @co2_left := (SELECT SUM(co2_budget - co2_consumed) FROM game where screen_name ='Ilkka');

SELECT screen_name, co2_budget, co2_consumed, @co2_left FROM game where screen_name ='Ilkka';
![Question 10.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/Ec9IZOODTlBBpuCKiuLMV3wBmF4-P9Kc0AO_NiCfEaJmiA?e=sZJdoo)

# EXERCISE 3

### Question 1
SELECT CO.name AS country_name, AIR.name AS airport_name  
FROM country AS CO
LEFT OUTER JOIN airport AIR ON AIR.iso_country = CO.iso_country  
WHERE CO.name='Iceland'
![Exercise 3 Q 1.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EUriYm4fR5VFiMSG7qb-QlEBTydr5M6hrpZ06BOmwEQpyw?e=b0qx9A)

### Question 2
SELECT airport.name AS "airport name"  
FROM airport INNER JOIN country  
ON airport.iso_country = country.iso_country  
WHERE country.name = 'France' AND airport.type = 'large_airport';
![Exercise 3 Q 2.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EXM5KGpa-SFFjjr1-LcFwFkB1mb6gFupFzKMz00K9BpGxQ?e=2WeQnp)

### Question 3
SELECT country.name AS "country_name", airport.name AS "airport_name" 
FROM airport INNER JOIN country  
ON airport.iso_country = country.iso_country  
WHERE country.continent='an';
![Exercise 3 Q 3.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EUj1_CDUY0VImQZ8oJnu3YMBAHmYo0Eqbe4DusUqiEmdOg?e=KoxJ5h)

### Question 4
select airport.elevation_ft from game, 
airport where airport.ident = game.location 
and game.screen_name="heini";
![Exercise 3 Q 4.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EWWMhjs4lCBLujfhFPFGsjIB7COa7LUnmCAf7aKl623vRw?e=6VGK4M)

### Question 5
select airport.elevation_ft * 0.3048 as elevation_m from game,
airport where airport.ident = game.location  
and game.screen_name="heini";
![Exercise 3 Q 5.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EUwUDqAoPvBErrjjB5QSoI8B3vsv-LnageSBoRt09-b-qA?e=sQFOeR)

### Question 6
select airport.name from game,
airport where airport.ident = game.location 
and game.screen_name="Ilkka";
![Exercise 3 Q 6.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EeJdvHlcAjJIgd-GUyq41ecBfiBHvcdhOUEq3ARPb0SPgw?e=qnXEmO)

### Question 7
SELECT country.name FROM game 
JOIN airport ON airport.ident = game.location 
INNER JOIN country ON country.iso_country = airport.iso_country 
WHERE game.screen_name="Ilkka";
![Exercise 3 Q 7.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EZIiEFFMrFVJgtWNkm8vSnABR1QWoVULkp9k3VA0hBtxxw?e=LcyDoA)

### Question 8
select goal.name from goal
INNER JOIN goal_reached ON goal.id = goal_reached.goal_id 
INNER JOIN game on goal_reached.game_id = game.id
WHERE game.screen_name="heini"
![Exercise 3 Q 8.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EbhN93vkLtVMvx7f670CN90BsyYBkfZqye8wuOF2EOke0g?e=cmggQI)

### Question 9
select airport.name FROM airport 
INNER JOIN game ON airport.ident = game.location   
INNER JOIN goal_reached ON game.id = goal_reached.game_id 
INNER JOIN goal ON goal_reached.goal_id = goal.id 
WHERE goal.name = 'clouds' AND game.screen_name='Ilkka';
![Exercise 3 Q 9.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EXkrwIoWPoJFq0OhE1Ic7NQBXCac8zEozMzEWAhrzzsJMg?e=yyR6bx)

### Question 10
SELECT country.name FROM airport  
INNER JOIN game ON airport.ident = game.location  
INNER JOIN goal_reached ON game.id = goal_reached.game_id  
INNER JOIN goal ON goal_reached.goal_id = goal.id  
INNER JOIN country ON airport.iso_country = country.iso_country  
WHERE goal.name = 'clouds' AND game.screen_name='Ilkka';
![Exercise 3 Q 10.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/Eb6Vwlg5sENFgUZHwGcwCAIBcfkGB_wud0s1XT96GFgf1g?e=KaZJmO)