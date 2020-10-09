# SQL Zoo
My notes from [SQL Zoo](https://sqlzoo.net/)

### SELECT Basics
Notes...

### SELECT from world

https://en.wikipedia.org/wiki/List_of_countries_by_population_(United_Nations)

**1. All the countries in the world**

`SELECT name, continent, population FROM world`

The snippet above selects data from __name__, __continent__, and __population__ fields in the __world__ table

--

**2. Large Countries**

`SELECT name FROM world WHERE population >= 200000000`

The snippet above selects the __name__ of countries from the __world__ table where the __population__ is greater than 200 million

--

**3. Per capita GDP**

`SELECT name, gdp/population FROM world WHERE population >= 200000000`

The snippet above selects the __name__ and __gdp/population__ (per capita GDP) of countries in the __world__ table with __population__ greater than 200 million

--

**4. South America in millions**

`SELECT name, population/1000000 FROM world WHERE continent = 'South America'`

The snippet above selects the __name__ and __population/1000000__ (population in millions) of countries in the __world__ table where __continent__ is South America

--

**5. France, Germany, Italy**

`SELECT name, population FROM world WHERE name IN ('France', 'Germany', 'Italy')`

The snippet above selects the __name__ and __population__ of countries in the __world__ table where __name__ is either France, Germany or Italy

--

**6. Countries with the word United**

`SELECT name FROM world WHERE name LIKE '%United%'`

The snippet above selects the __name__ of countries in the __world__ table where __name__ includes United
