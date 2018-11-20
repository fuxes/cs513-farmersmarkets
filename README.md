# CS513 - Final Project

The goal of the project is to analyze the farmers market data set and come up with End to End workflow which answers some meaningful use cases

## Database

There is created database with all the dataset information on `farmersmarkets_trifacta.db`

To inspect the database, run::

    $ sqlite3 farmersmarkets_trifacta.db
    sqlite> SELECT * FROM `farmersmarkets_trifacta` LIMIT 10;

### Last version

To recreate the database after trifacta modifications, run::

    $ cat data/farmersmarkets_trifacta.struct.sql | sqlite3 farmersmarkets_trifacta.db
    $ sqlite3 farmersmarkets_trifacta.db
    sqlite> .mode csv
    sqlite> .import data/farmersmarkets_trifacta.csv farmersmarkets_trifacta
    sqlite> SELECT * FROM `farmersmarkets_trifacta` LIMIT 10;

### Pristine Database

To recreate the pristine database, run::

    $ cat data/farmersmarkets.struct.sql | sqlite3 farmersmarkets.db
    $ sqlite3 farmersmarkets.db
    sqlite> .mode csv
    sqlite> .import data/farmersmarkets.csv farmersmarkets
    sqlite> SELECT * FROM `farmersmarkets` LIMIT 10;

## Links

Project Report
  <https://docs.google.com/document/d/1QmMaNa0dfcu6LWxADV8clzUXJfLKKlm2SMFb7ldoLwQ/edit#>

Farmers Market Dataset Source
  <https://www.ams.usda.gov/local-food-directories/farmersmarkets>

## Authors

-   Madhvesh Navkal Badri [mn9@illinois.edu]
-   Martin Becerra [carlosb3@illinois.edu]
-   Matthew Nolan [mrnolan4@illinois.edu]
