### Laravel Installation

## Run given below command for install laravel app
    1. composer create-project laravel/laravel <project_name>

## Write README.md
    1. Write all steps that i perform for creating this project

## Create GitHub Repository
    1. Create simple repo (from github account) without .gitignore or any file

## Let's Connect with Git Origin
    1. Run the given below commands
        1.1 cmd >> git init
        1.2 cmd >> git add .
        1.3 cmd >> git commit -m "initial commit"
        1.4 cmd >> git remote add origin https://github.com/arsalanmughal23/laravel_boiler.git
        1.5 cmd >> git push -u origin master

## Guest Api
    1. make route in routes/api.php 
    2. make sure you make route outside the middleware/auth group
    3. Note: i already created an example of guest api in routes/api.php with name of "guest-example"

## Configure Database & Run Migration
    1. ENV CONFIGURATION: make sure your .env file is configured and database connected properly
    2. RUN MIGRATION: run migration for create tables with this COMMAND: php artisan migrate
    3. MIGRATION (SQLSTATE[42000]) ERROR SOLUTION: if you have errors while run migration command
        3.1 just read the error if you have this kind of error
            3.1.1 SQLSTATE[42000]: Syntax error or access violation: 1071 Specified key was too long; max key length is 1000 byte...
            3.1.2 Solution: goto the file config/database.php, then find your database (inside connections key) that you are using for.
            3.1.3 replace values 
                from 'charset' => 'utf8mb4'                 to  'charset' => 'utf8'
                from 'collation' => 'utf8mb4_unicode_ci'    to  'collation' => 'utf8_unicode_ci'
                from 'engine' => null                       to  'engine' => 'InnoDB'
        3.2 then run migration with this COMMAND: php artisan migrate:fresh
            3.2.1 here i using fresh tag that drop all the tables first if exists then run migration

## Sanctum Api Auth
    1. import postman collection "laravel-api.postman_collection.json" file is location root directory of this project
    2. set baseURL as a collection variable
    3. then run the project by COMMAND: php artisan serve
    4. run register api
        4.1 you need to check & understand Body tab & Tests tab from postman request.
    5. after run the register api you revieve response data the plainTextToken is the sanctum-auth token
    6. now you run user api this api need authorization without token you can't use this api
        6.1 i already set token as a collection variable inside the register api test.
        6.2 when you read and observe it you can understand.
        6.3 if you want to do it manually.
            6.3.1 copy token from the key of plainTextToken in register api
            6.3.2 then set token as a collection variable with the key name of "myToken"
            6.3.3 because we use token with this name "myToken" inside Authorization: Bearer