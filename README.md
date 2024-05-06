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
