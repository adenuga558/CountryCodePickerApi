﻿# CountryCodePickerApi
A simple restful api with laravel that displays a list of all the countries, country code, iso code name and flag in json format.

### Prerequisites
* Apache
* PHP
* Composer

## Installation steps
Follow the below steps to install and set up the application.

**Step 1: Clone the Application**<br>
You can download the ZIP file or git clone from my repo into your project directory.

**Step 2: Configure the Application**<br>
After you clone the repo in to your project folder the project need to be set up by following commands-

- In terminal go to your project directory and Run 
    
        composer install 
    
- Then copy the .env.example file to .env file in the project root folder

- Edit the .env file and fill all required data for the bellow variables
    
        APP_URL=http://localhost //your application domain URL go here
    
        DB_HOST=127.0.0.1 // Your DB host IP. Here we are assumed it to be local host
        DB_PORT=3306 //Port if you are using except the default
        DB_DATABASE=ccpapi // Your DB name
        DB_USERNAME=root // Your DB username
        DB_PASSWORD= // Your DB password

- To set the Application key run the bellow command in your terminal.
    
        php artisan key:generate        

- Create all the necessary tables need for the application by runing the below command
    
        php artisan migrate

- Then import countries.sql in your phpmyadmin.     

Thats all! The application is now configured.

## API Endpoints and Routes
The application has the following resources

#### Get All Country List

```
GET http://127.0.0.1:8000/api/v1/country

```

The response will be a JSON containing the country info.

```json
[
{
"id": 1,
"name": "Please select your country...",
"code": "FLAG_TRANSPARENT",
"phonecode": "+"
},
{
"id": 2,
"name": "Afghanistan",
"code": "AF",
"phonecode": "+93"
}
]
```

#### Get Single Country

```
GET http://127.0.0.1:8000/api/v1/country/afghanistan

```

The response will be a JSON containing the country info.

```json
[
{
"id": 2,
"name": "Afghanistan",
"code": "AF",
"phonecode": "+93"
}
]
```

## References
* [Laravel docs](https://laravel.com/docs/6.x) - Laravel Documentation     

### License
The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
