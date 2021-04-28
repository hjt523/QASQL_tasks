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

Madrid

 ### SELECT city.ID,  country.capital,country.name  , city.name  FROM city INNER JOIN country ON city.ID=country.capital where country.name='spain';
 

- Using JOIN ... ON, list all the languages spoken in the Southeast Asia region.

+---------------+-------------+------+----------------+

| language      | countrycode | code | region         |

+---------------+-------------+------+----------------+

| Chinese       | BRN         | BRN  | Southeast Asia |

| English       | BRN         | BRN  | Southeast Asia |

| Malay         | BRN         | BRN  | Southeast Asia |

| Malay-English | BRN         | BRN  | Southeast Asia |

| Bali          | IDN         | IDN  | Southeast Asia |

| Banja         | IDN         | IDN  | Southeast Asia |

| Batakki       | IDN         | IDN  | Southeast Asia |

| Bugi          | IDN         | IDN  | Southeast Asia |

| Javanese      | IDN         | IDN  | Southeast Asia |

| Madura        | IDN         | IDN  | Southeast Asia |

| Malay         | IDN         | IDN  | Southeast Asia |

| Minangkabau   | IDN         | IDN  | Southeast Asia |

| Sunda         | IDN         | IDN  | Southeast Asia |

| Chinese       | KHM         | KHM  | Southeast Asia |

| Khmer         | KHM         | KHM  | Southeast Asia |

| Tšam          | KHM         | KHM  | Southeast Asia |

| Vietnamese    | KHM         | KHM  | Southeast Asia |

| Lao           | LAO         | LAO  | Southeast Asia |

| Lao-Soung     | LAO         | LAO  | Southeast Asia |

| Mon-khmer     | LAO         | LAO  | Southeast Asia |

| Thai          | LAO         | LAO  | Southeast Asia |

| Burmese       | MMR         | MMR  | Southeast Asia |

| Chin          | MMR         | MMR  | Southeast Asia |

| Kachin        | MMR         | MMR  | Southeast Asia |

| Karen         | MMR         | MMR  | Southeast Asia |

| Kayah         | MMR         | MMR  | Southeast Asia |

| Mon           | MMR         | MMR  | Southeast Asia |

| Rakhine       | MMR         | MMR  | Southeast Asia |

| Shan          | MMR         | MMR  | Southeast Asia |

| Chinese       | MYS         | MYS  | Southeast Asia |

| Dusun         | MYS         | MYS  | Southeast Asia |

| English       | MYS         | MYS  | Southeast Asia |

| Iban          | MYS         | MYS  | Southeast Asia |

| Malay         | MYS         | MYS  | Southeast Asia |

| Tamil         | MYS         | MYS  | Southeast Asia |

| Bicol         | PHL         | PHL  | Southeast Asia |

| Cebuano       | PHL         | PHL  | Southeast Asia |

| Hiligaynon    | PHL         | PHL  | Southeast Asia |

| Ilocano       | PHL         | PHL  | Southeast Asia |

| Maguindanao   | PHL         | PHL  | Southeast Asia |

| Maranao       | PHL         | PHL  | Southeast Asia |

| Pampango      | PHL         | PHL  | Southeast Asia |

| Pangasinan    | PHL         | PHL  | Southeast Asia |

| Pilipino      | PHL         | PHL  | Southeast Asia |

| Waray-waray   | PHL         | PHL  | Southeast Asia |

| Chinese       | SGP         | SGP  | Southeast Asia |

| Malay         | SGP         | SGP  | Southeast Asia |

| Tamil         | SGP         | SGP  | Southeast Asia |

| Chinese       | THA         | THA  | Southeast Asia |

| Khmer         | THA         | THA  | Southeast Asia |

| Kuy           | THA         | THA  | Southeast Asia |

| Lao           | THA         | THA  | Southeast Asia |

| Malay         | THA         | THA  | Southeast Asia |

| Thai          | THA         | THA  | Southeast Asia |

| Portuguese    | TMP         | TMP  | Southeast Asia |

| Sunda         | TMP         | TMP  | Southeast Asia |

| Chinese       | VNM         | VNM  | Southeast Asia |

| Khmer         | VNM         | VNM  | Southeast Asia |

| Man           | VNM         | VNM  | Southeast Asia |

| Miao          | VNM         | VNM  | Southeast Asia |

| Muong         | VNM         | VNM  | Southeast Asia |

| Nung          | VNM         | VNM  | Southeast Asia |

| Thai          | VNM         | VNM  | Southeast Asia |

| Tho           | VNM         | VNM  | Southeast Asia |

| Vietnamese    | VNM         | VNM  | Southeast Asia |

+---------------+-------------+------+----------------+ 

### SELECT countrylanguage.language, countrylanguage.countrycode,  country.code,country.region     FROM countrylanguage INNER JOIN country ON countrylanguage.countrycode=country.code where country.region='Southeast Asia';


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
