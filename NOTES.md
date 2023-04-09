> superdatascience.com/sql
> COPY CONSUMER_COMPLAINTS FROM '/Users/jack/Desktop/ConsumerComplaints.csv' DELIMITER ',' CSV HEADER;
> select product_name from consumer_complaints where lower(product_name) like '%credit%'
> select product_name from consumer_complaints where upper(product_name) like '%CREDIT%'
>select company, product_name, zip_code from consumer_complaints where consumer_complaints.zip_code like '4____'
> select company, product_name, zip_code from consumer_complaints where consumer_complaints.zip_code like '__4__'
> select company, product_name, zip_code from consumer_complaints where consumer_complaints.zip_code not like '__4__'

> alter table console_games add column  global_sales float8;

> update console_games set global_sales = na_sales + eu_sales +  jp_sales + other_sales;

> select game_name, length(game_name) from console_games;
> select publisher, left(publisher, 4) from console_games; 
> select publisher, right(publisher, 4) from console_games;

> select publisher, reverse(publisher) from console_games;

> left and right function dies not exist in hive

> select * , date_part('year', discontinued) - date_part('year', first_retail_availability) as years_existed from console_dates order by years_existed;

date_part not exist in hive

> select age(discontinued, first_retail_availability) from console_dates

> age function only in postgres

> select cast(game_year as varchar(4)) from console_games order by game_year;
> select game_year::varchar(4) from console_games order by game_year;

hive also have to_date function


## nulls


> null isn't = anything(include null)


## Relational keys

+ Superkey: is any combination of columns that uniquely identifies a row in a table
+ Candidate key is a superkey such that no proper subset is a superkey, and has thw following two properties: 
  + Uniqueness
  + Irreducibility
+ Primary key: is the candidate key that is selected to identify tuples uniquely withing the relation:
  + If a relation has serveral candidate keys only one is chosen to be the primary key
+ Foreign keys
  + is an attribute or set of attributes,within one relation that matches the candidate key of some other relation


## What is a relational database

+ Relational database is a set of tables that satify following data integrity:
  + Entity integrity
  + Domain integrity
  + Referential integrity
  + User-Defined integrity


# Joints

## Type of Joins

+ Inner Join
+ Left Join(Left outer Join)
+ Right Join
+ Full Outer Join
+ Cross Join


## Duplictes in joins

## Join on multiple fields




