> superdatascience.com/sql
> COPY CONSUMER_COMPLAINTS FROM '/Users/jack/Desktop/ConsumerComplaints.csv' DELIMITER ',' CSV HEADER;
> select product_name from consumer_complaints where lower(product_name) like '%credit%'
> select product_name from consumer_complaints where upper(product_name) like '%CREDIT%'
>select company, product_name, zip_code from consumer_complaints where consumer_complaints.zip_code like '4____'
> select company, product_name, zip_code from consumer_complaints where consumer_complaints.zip_code like '__4__'
> select company, product_name, zip_code from consumer_complaints where consumer_complaints.zip_code not like '__4__'




