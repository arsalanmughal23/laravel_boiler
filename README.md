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

## Setup .env environment file
    1. if .env is not exists copy .env.example as .env also using given command.
        1.1 cmd >> cp .env.example .env
    2. setup .env file

## Create Database
    1. create database by name, that you can set on .env

## Run the Migration
    1. run migration by using given below command.
        1.1 cmd >> php artisan migrate

## Run the Project
    1. run project by using given below command.
        1.1 cmd >> php artisan serve
    2. you also run the project throw localhost or virtualhost and etc
    3. after that hit the url that return in terminal with development server: http://127.0.0.1:8000

## How to abort terminal when project is running by serve command
    1. click on terminal then press ctrl + c

## Generate Application Key
    1. generate application key by using given below command.
        1.1 cmd >> php artisan key:generate

## Run the Project Again
    1. run the project again same as recently i have run.

