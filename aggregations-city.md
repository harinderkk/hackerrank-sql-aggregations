### 1.Query a count of the number of cities in CITY having a Population larger than 100,000.

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



### 2.Query the total population of all cities in CITY where District is California.

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


### 3.Query the average population of all cities in CITY where District is California.

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

```select round(avg(cast(population as float)),3) from city where district like 'California';```

### 4.Query the average population for all cities in CITY, rounded down to the nearest integer.

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
```select round(avg(cast(population as float))) from city;```


### 5.Query the sum of the populations for all Japanese cities in CITY. The COUNTRYCODE for Japan is JPN.
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
```select sum(population) from city where countrycode = 'JPN';```


### 6.Query the difference between the maximum and minimum populations in CITY.

**CITY**

| Field  | Type |
| ------------- | ------------- |
| id  | number  |
| name  | varchar(17) |
|countrycode | varchar2(3) |
|district | varchar2(20) |
|population  | number |

###  Solution
``` select max(population) - min(population) from city;```
