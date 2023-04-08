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


