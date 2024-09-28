# EXERCISE 6

### Question 1
select max(elevation_ft) from airport;
![EX 6 Question 1.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EXxKZoXyg_NCkDU_p6uuLLcBIRUJgRcYSMIonU3I6RPmIg?e=bdaXKq)

### Question 2
select continent, count(*) from country group by continent;
![EX 6 Question 2.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EXhj3JbTNSZCoMw31y_w48YBByvGMD6RWnSxCYM-M0R4HQ?e=aUbUqE)

### Question 3
select screen_name, count(*) from game, goal_reached where id = game_id group by screen_name;
![EX 6 Question 3.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EbMuhGM8xaNOqBVPwk9o-EsBguQ-7Xmv3cBatrJcOP1sLg?e=OnmcxG)

### Question 4
select screen_name from game where co2_consumed in(select min(co2_consumed) from game );
![EX 6 Question 4.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EckQjsFI1h9KnAm1CXhnqd8B6E1ELwvyXt6htVSAe13_uA?e=jnfYLt)

### Question 5
select country.name, COUNT(*) from airport, 
country where airport.iso_country = country.iso_country group by country.iso_country order by COUNT(*) desc limit 50;
![EX 6 Question 5.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/Ee2c6oz_wktHhXUZpoDs7g0BgfscmRY6vZFj51X-nEUA5A?e=JKWkWO)

### Question 6
select country.name from airport, 
country where airport.iso_country = country.iso_country group by country.iso_country having count(*) > 1000;
![EX 6 Question 6.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EXfx8h9VnaBHi-wRu714K0kBAmABRMAm5y5nigcq8NjPcQ?e=mQl3IV)

### Question 7
select name from airport where elevation_ft in ( select max(elevation_ft) from airport );
![EX 6 Question 7.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EdG4eCFtxMZMpzqNiaewHJMBsAyoLx8Q2Nq_9ABCKe6b-g?e=lkm1gx)

### Question 8
select name from country where iso_country in ( select iso_country from airport where elevation_ft in( select max(elevation_ft) from airport ) );
![EX 6 Question 8.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EdiuIktQULdLo_-ZrBTAiOUB4sBSuHLxuvwR_qPuoTkGxQ?e=9f8mxF)

### Question 9
select count(*) from game, goal_reached where id = game_id and screen_name = "Vesa" group by screen_name;
![EX 6 Question 9.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EfL1ma9OGURFhtX9UEcmKHsB8hobbRPzfylrS_9dNfWReA?e=6eoEx4)

### Question 10
select name from airport where latitude_deg in( select min(latitude_deg) from airport );
![EX 6 Question 10.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/ESG_Pmxnoc5HgI_S-2dKAcMBJyb0uICmDM5C2u2zy_sGlA?e=6WYuKR)

# EXERCISE 7

### Question 1
update game
set  location = (select ident from airport where name = "Nottingham Airport"), co2_consumed = co2_consumed+500
where screen_name = "Vesa";
![EX 7 Question 1.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EQfLrgJgDMlPlMnZn8efvKUBjeI0MUgpFxd6VeMQ7XPbGQ?e=ZYeBo5)

### Question 2
![EX 7 Question 2.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EftcToWu0ZJMtx42gXiFR8MBJdOQ5gbnYnRtiSMaeNa-nw?e=R2YizA)

### Question 3
delete from goal_reached;
![EX 7 Question 3.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EUv53P2AXpZIvU4P84edACsBGuMaXw3c5YCQIiQTij7Wjg?e=Htp1cl)

### Question 4
delete from game;
![EX 7 Question 4.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/Eana-GZ_3w5MsIxnBeHkY_kB_9bh4NeL7FJWQbYdxTtBFQ?e=2QyTUX)