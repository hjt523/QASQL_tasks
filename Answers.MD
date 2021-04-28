# World


- Using COUNT, get the number of cities in the USA.

274

### CODE USED :select count('CountryCode')from city where CountryCode = 'USA';


- Find out the population and life expectancy for people in Argentina.

population = 19996563

### select sum(population)from city where CountryCode = 'ARG';

population = 37032000
Life Expectancy = 75.1

### select * from country where code = 'ARG'


- Using IS NOT NULL, ORDER BY, and LIMIT, which country has the highest life expectancy?

 83.5 , AND , Andorra

###  SELECT Code,LifeExpectancy  FROM country where LifeExpectancy is not null ORDER BY LifeExpectancy  desc limit 1;


- Using JOIN ... ON, find the capital city of Spain.




- Using JOIN ... ON, list all the languages spoken in the Southeast Asia region.




- Using a single query, list 25 cities around the world that start with the letter F.

+---------------------------+
| Name                      |
+---------------------------+
| Fagatogo                  |
| Florencio Varela          |
| Formosa                   |
| Francistown               |
| Fortaleza                 |
| Feira de Santana          |
| Franca                    |
| Florianópolis             |
| Foz do Iguaçu             |
| Ferraz de Vasconcelos     |
| Francisco Morato          |
| Franco da Rocha           |
| Fuenlabrada               |
| Faridabad                 |
| Firozabad                 |
| Farrukhabad-cum-Fatehgarh |
| Faizabad                  |
| Fatehpur                  |
| Firenze                   |
| Foggia                    |
| Ferrara                   |
| Forlì                     |
| Fukuoka                   |
| Funabashi                 |
| Fukuyama                  |
+---------------------------+

### select Name from city where name like 'F%' limit 25;

- Using COUNT and JOIN ... ON, get the number of cities in China.
- Using IS NOT NULL, ORDER BY, and LIMIT, which country has the lowest population? Discard non-zero populations.
- Using aggregate functions, return the number of countries the database contains.
- What are the top ten largest countries by area?
- List the five largest cities by population in Japan.
- List the names and country codes of every country with Elizabeth II as its Head of State. You will need to fix the mistake first!
- List the top ten countries with the smallest population-to-area ratio. Discard any countries with a ratio of 0.
- List every unique world language.
- List the names and GNP of the world's top 10 richest countries.
- List the names of, and number of languages spoken by, the top ten most multilingual countries.
- List every country where over 50% of its population can speak German.
- Which country has the worst life expectancy? Discard zero or null values.
- List the top three most common government forms.
- How many countries have gained independence since records began?
