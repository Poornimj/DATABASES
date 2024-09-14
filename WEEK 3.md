# EXERCISE 2

### Question 1
select * from goal;
![Question 1.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%201.png)

### Question 2
SELECT NAME, type FROM airport
WHERE iso_country = 'FI';
![Question 2.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%202.png)

### Question 3
SELECT NAME, type FROM airport
WHERE iso_country = 'FI'
AND NAME <> ' ht ri Airfield'
ORDER BY
NAME ASC;
![Question 3.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%203.png)

### Question 4
SELECT NAME, type FROM airport
WHERE iso_country ='FI'
ORDER BY
TYPE,
NAME;
![i![Question 4.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%204.png)mg_3.png](img_3.png)

### Question 5
SELECT NAME FROM COUNTRY
WHERE NAME LIKE 'F%'
![Question 5.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%205.png)![img_4.png](img_4.png)

### Question 6
SELECT NAME FROM country
WHERE NAME LIKE '%F%'
![![Question 6.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%206.png)img_5.png](img_5.png)

### Question 7
select location from game where screen_name="Vesa";
![![Question 7.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%207.png)img_6.png](img_6.png)

### Question 8
select c02_budget from game where screen_name="llkka"
![img![Question 8.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%208.png)_7.png](img_7.png)

### Question 9
select distinct co2_budget from game;
![![Question 9.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%209.png)img_8.png](img_8.png)

### Question 10
SET @co2_left := (SELECT SUM(co2_budget - co2_consumed) FROM game where screen_name ='Ilkka');

SELECT screen_name, co2_budget, co2_consumed, @co2_left FROM game where screen_name ='Ilkka';
![Question 10.png](..%2F..%2FOneDrive%20-%20Metropolia%20Ammattikorkeakoulu%20Oy%2FPictures%2FQuestion%2010.png)