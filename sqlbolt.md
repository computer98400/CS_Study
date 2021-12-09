




lesson 6
1. select * from movies inner join boxoffice on id= movie_id;
2. SELECT Title, International_sales, Domestic_sales FROM movies  inner join boxoffice on boxoffice.domestic_sales < boxoffice.international_sales where movies.id = boxoffice.movie_id;
3. select * from movies inner join boxoffice on id = movie_id order by rating desc;

lesson 7
1. select distinct building from employees;
2. select * from buildings;
3. select distinct building_name, role from buildings left join employees on building_name = building;

lesson 8
1. select name role from employees where building is null;
2. select building_name from buildings left join employees on building_name = building where role is null;

lesson 9
1. SELECT title,(domestic_sales+international_sales)/1000000 FROM movies left join boxoffice on id = movie_id;
2. 
