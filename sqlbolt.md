




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
2. select title, rating *10 from movies left join boxoffice on id = movie_id;
3. select * from movies where year%2 = 0;

lesson 10
1. SELECT max(years_employed) from employees;
2. select role, avg(years_employed) from employees group by role;
3. select building, sum(years_employed) from employees group by building;

lesson 11
1. select count(role) from employees where role = "Artist";
2. select count(role) from employees group by role;
3. select sum(years_employed) from employees where role = "Engineer";

lesson 12
1. select director, count(*) from movies group by director;
2. select director, sum(domestic_sales,international_sales) from movies left join boxoffice on movie_id = id group by director;

lesson 13
1. insert into movies values (null,"Toy Story 4","Lee UnKrich", "2022","111");
2. insert into boxoffice values (15,8.7,340000000,270000000);

lesson 14
1. update movies set director ="John Lasseter" where title = "A Bug's Life";
2. update movies set year = 1999 where title = "Toy Story 2";
3. update movies set title = "Toy Story 3", director="Lee Unkrich" where id = 11;

lesson 15
1. delete from movies where year < 2005;
2. delete from movies where director = "Andrew Stanton";

lesson 16
1. create table Database (Name text, Version float, Download_count Integer, auto_increments);

lesson 17
1. alter table movies add Aspect_ratio float;
2. alter table movies add Language text default "english";

lesson 18
1. drop table movies;
2. drop table boxoffice;

<h3>Finish</h3>

4. 
