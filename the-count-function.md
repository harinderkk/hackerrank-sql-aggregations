### Query a count of the number of cities in CITY having a Population larger than 100,000.

Input Format

The CITY table is described as follows:

   **CITY**

| Field  | Type |
| ------------- | ------------- |
| id  | number  |
| name  | varchar(17) |
|countrycode | varchar2(3) |
|district | varchar2(20) |
|population  | number |

### Solution

```select count(id) from city where population > 100000;```



### Query the total population of all cities in CITY where District is California.

Input Format

The CITY table is described as follows:

   **CITY**

| Field  | Type |
| ------------- | ------------- |
| id  | number  |
| name  | varchar(17) |
|countrycode | varchar2(3) |
|district | varchar2(20) |
|population  | number |

### Solution

```select sum(population) from city where district = 'California';```
