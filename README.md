# sql-project :zap:

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
``sql 
select name, location, rating 
from ksa 
where rating = 5;
```
![image](https://github.com/user-attachments/assets/eaeb976c-06ae-4b44-801a-539e95dacf0c)


