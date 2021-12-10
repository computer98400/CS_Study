<h1>SQLBolt study</h1>

lesson 1
1. select title from movies;
2. select director from movies;
3. select title, director from movies;
4. select title, year from movies;
5. select * from movies;

lesson 2
1. select * from movies where id=6;
2. select * from movies where year between 2000 to 2010;
3. select * from movies where year not between 2000 and 2010;
4. select * from movies limit 5;

lesson 3
1. SELECT * FROM movies where title like "Toy Story%";
2. SELECT * FROM movies where director like "John Lasseter";
3. SELECT * FROM movies where director != "John Lasseter";
4. SELECT * FROM movies where title like "WALL%";

lesson 4
1. select distinct director from movies order by director asc;
2. select * from movies order by year desc limit 4;
3. select * from movies order by title limit 5;
4. select * from movies order by title asc limit 5 offset 5;

lesson 5
1. select * from North_american_cities where country="Canada";
2. select * from North_american_cities where country="United States" order by latitude desc;
3. select * from North_american_cities where longitude < (select longitude from North_american_cities where city = "Chicago") order by longitude;
4. select * from North_american_cities where country ="Mexico" order by population desc limit 2;
5. select * from North_american_cities where country ="United States" order by population desc limit 2 offset 2;

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

<h2>Finish</h2>

