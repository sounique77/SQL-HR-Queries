# SQL-HR-Queries
Complex EER diagram 
<img width="293" alt="image" src="https://user-images.githubusercontent.com/121234311/228212153-92a1a663-7240-4c15-b2cb-ccb6440419c5.png">

#1) Write down sql query to show distinct cities from customers table


use sql_store;

select count(distinct city) from customers;
<img width="141" alt="image" src="https://user-images.githubusercontent.com/121234311/228217277-6bfdf629-efe1-45d4-9cb4-78a6e61a4e67.png">




#2) Write SQL query to show number of Sales Rep in employees table


use sql_hr;

select count(*) from employees where job_title  = 'Sales Rep'; 
<img width="472" alt="image" src="https://user-images.githubusercontent.com/121234311/228215456-095d1003-294b-4982-a3be-037592affc18.png">


#3) What is the adress line for the offices in New York?


use sql_hr;

select address, city, state from offices where city ="New York City";
<img width="220" alt="image" src="https://user-images.githubusercontent.com/121234311/228219194-4e94076b-6750-4ab0-adc0-0245f740a20b.png">


#4) What is the largest quantity ordered in order_items table?


use sql_store;

select max(quantity) from order_items;
<img width="92" alt="image" src="https://user-images.githubusercontent.com/121234311/228224005-3cbc272f-aa89-473a-9dac-6810e84059b0.png">


#5) What is the highest amount paid on '2019-01-26' in payments table?


use sql_invoicing;

select max(amount) from payments where date = '2019-01-26';
<img width="86" alt="image" src="https://user-images.githubusercontent.com/121234311/228225112-be1df254-191b-4225-a9a2-0cf5f6571905.png">

#6) Which products are available more than 50 in stock and also has price lower than 3?


use sql_store;

select * from products
where quantity_in_stock > 50 and unit_price<3;
<img width="305" alt="image" src="https://user-images.githubusercontent.com/121234311/228225715-dd3bcbdf-2477-494a-a697-98bed15ba217.png">

