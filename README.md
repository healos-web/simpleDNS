# SimpleDNS
Simple DNS server with caching, built with Sinatra framework.

## Enviroment
**Ruby 2.7.1**;  
**Sinatra** (light framework to build simple web applications fast);  
**PostgresSQL** as a main database;  
**Redis** as a cache store;  

## Extra details
To store resource records was chosen Postgres database, it has great column type `ltree` for representing labels in a hierarchical tree-like structure. More about that you can find here https://www.postgresql.org/docs/9.3/ltree.html. 

There is present simple dashboard to test DNS server, it includes following functionality:  
  1) Get value of api address by providing host name;  
  2) Add new resource record to database;  
  3) Upload csv file to import resource records (file-example you can find in public folder);  
  4) Download csv file to export resource records;  

## Get started
There is present `docker-compose.yml` file in `/docker` folder to you be able to start project as fast as possible. To do it, please follow the instructions below:  
  1) create `.env` in the root folder, file should include following variables  
    **DB_USERNAME**=postgres  
    **DB_PASSWORD**=postgres  
    **DB_HOST**=db_simple_dns  
    **REDIS_HOST**=cache_storage_simple_dns  
  2) `docker-compose up`  
  3) Open `localhost:3000` to see app  
And make sure you have installed docker and docker-compose on you machine 
