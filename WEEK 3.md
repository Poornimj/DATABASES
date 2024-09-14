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