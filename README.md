## objectives
````sql
select category,
(select avg(sales)from global_superstore)as overall_avg,
 (select sum(sales) from global_superstore)as overall_total_sales,
 (select sum(sales) from global_superstore)
 -
 (select avg(sales) from global_superstore) as diff_
 from global_superstore;
````
````sql
select category,
(select round(avg(sales),2) from global_superstore)as overall_avg,
 (select round(sum(sales),2) from global_superstore)as overall_total_sales,
 round((select round(sum(sales),2) from global_superstore)
 -
 (select round(avg(sales),2) from global_superstore),2) as diff_
 from global_superstore;
````
