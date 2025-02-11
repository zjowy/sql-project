# sql-project :zap:
The data I used is about theaters in Saudi Arabia, including their names, locations, genres, ratings, and reviews. It provides insights into theater popularity, audience feedback, and the most-reviewed spots.

## first we show all the table by using select star :sparkles:
```sql
use firstDB;
select * from ksa
```
![image](https://github.com/user-attachments/assets/462e8b91-22e4-40d8-a316-fdf48aa240cc)

## Now we want to see the avrage of the revirw count 
```sql
use firstDB;
select avg(review_count) as avrage_review_count from ksa
```
![image](https://github.com/user-attachments/assets/cc2900cc-eae7-458a-b0a9-9156f6531c28)

## Now we want to see the uniqe names :sparkles:
```sql
use firstDB;
select distinct name as uniqe_names from ksa
```
![image](https://github.com/user-attachments/assets/a797692d-3ea8-4a85-a730-0846d1224c5e)

## Now we want to see the count of the uniqe genre :memo:
```sql
use firstDB;
select count(distinct genre) as count_uinqe_genre from ksa 
```
![image](https://github.com/user-attachments/assets/f8b63017-eb79-4f99-a9f9-1d51ae943205)

## Count the number of theaters by location
```sql
select location, COUNT(*) AS theater_count 
from ksa 
group by location 
order by  theater_count DESC;
```
![image](https://github.com/user-attachments/assets/13bf5ba1-62fd-4b8b-bb7a-b86c81961d55)

## Find the highest-rated theaters
```sql 
select name, location, rating 
from ksa 
where rating = 5;
```
![image](https://github.com/user-attachments/assets/92380923-3d11-40e3-8ab7-a2254c4b167d)

 ## Find the average rating for each genre
``` sql
select genre, avg(rating) as avg_rating 
from ksa
group by genre 
order by avg_rating DESC;
```
![image](https://github.com/user-attachments/assets/78131706-ea40-47f4-876e-0932850a3466)

## Find locations with the most 5-star rated theaters
```sql
select location, COUNT(*) as five_star_count 
from ksa 
where rating = 5 
group by location 
order by five_star_count desc;
```
![image](https://github.com/user-attachments/assets/316984b6-4eb0-4413-bf57-7af179f8d794)

## Retrieve theaters that have a best comment
```sql
select name, best_comment 
from ksa 
where best_comment is not null;
```
![image](https://github.com/user-attachments/assets/6de37389-eca2-4c13-b777-bbd9b4f6525b)

## Find theaters with the lowest rating 
```sql
select name, location, rating 
from ksa
where rating > 0 
order by rating asc
limit 5;
```
![image](https://github.com/user-attachments/assets/9e7d2911-63c9-439b-bbb2-8c70c538a41b)


