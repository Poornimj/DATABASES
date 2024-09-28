# EXERCISE 4

### Question 1
Select country.name as "country name", 
airport.name as "airport name" from country inner join airport on airport.iso_country = country.iso_country where country.name = "Finland"and scheduled_service = "yes";
![Question 1.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EaBVP_9-vatJlqut2ok9vEEBxTL-UWZCK6qtBHyhbaXVEg?e=APPkZx)

### Question 2
select screen_name, airport.name from game inner join airport on location = ident;
![Question2.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EfT-4lY6TExGuO7uJlfx0d8B3YBx_sGsu79mqA3pV6_Mcw?e=sKtJ64)

### Question 3
select screen_name, country.name from game inner join airport on location = ident
inner join country on airport.iso_country = country.iso_country;
![Question 3.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EXgh6IUgKoZFhH0T9wrChMMBuz5_Hnkw3Zc7bUZwpGsNnw?e=w5C9Rd)

### Question 4
select airport.name, screen_name from airport left join game on ident = location where airport.name like "%Hels%";
![Question 4.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EfYneszIbz5EmMcKN9FjlSsBHKJ3xZ8Cnczi_M-1C8W3RQ?e=9aUaKg)

### Question 5
select name, screen_name from goal left join goal_reached on goal.id = goal_id left join game on game.id = game_id;
![Question 5.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EXrZFlLmsvhOsC_IytM63hcBbiRTW_AXohFL0yemSLElLQ?e=0GfceT)

# EXERCISE 5

### Question 1
select name from country where iso_country in (select iso_country from airport where name like "Satsuma%");
![Question S 1.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/ETALndd-w1tLnTSX7tUv8nIBLLihgx_SKMEypaTx_ce-LA?e=4B4s6x)

### Question 2
select name from airport where iso_country in (select iso_country from country where country.name = "Monaco");
![Question S 2.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/Ef3LxeIQwLJBpHUMGuUymKMBPF1cS9c8VJQXlYOUqOyOxg?e=yUQDQy)

### Question 3
Select screen_name from game where id in(select game_id from goal_reached where goal_id in(select id from goal where name ="CLOUDS"));
![Question S 3.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EQykHXInSZ1LhMg6rGyw0EsBmUiThx05Ov_Xxo1fV9kCDQ?e=oD4slY)

### Question 4
Select country.name from country where iso_country not in (select airport.iso_country from airport);
![Question S 4 .png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EYa8BTStROdLvC_eqqf_2aMBXHvsk0xetH_Em85yh1ZSZA?e=dDv8Us)

### Question 5
select name from goal where id not in (select goal.id from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini");
![Question S 5.png](https://metropoliafi-my.sharepoint.com/:i:/g/personal/poornimj_metropolia_fi/EcN4yzOTaE1Dl4802NSWFgEBlhazM-uioF6nKe42254G6g?e=AqocCK)