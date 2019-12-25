# CountryCodePickerApi
A simple restful api with laravel that displays a list of all the countries, country code, iso code name and flag in json format.

### Prerequisites
* Apache
* PHP
* Composer

## Installation steps
Follow the bellow steps to install and set up the application.

**Step 1: Clone the Application**<br>
You can download the ZIP file or git clone from my repo into your project  directory.

**Step 2: Configure the Application**<br>
After you clone the repo in to your project folder the project need to be set up by following commands-

- In terminal go to your project directory and Run 
    
        composer install 
    
- Then copy the .env.example file to .env file in the project root folder

- Edit the .env file and fill all required data for the bellow variables
    
        APP_URL=http://localhost //your application domain URL go here
    
        DB_HOST=127.0.0.1 // Your DB host IP. Here we are assumed it to be local host
        DB_PORT=3306 //Port if you are using except the default
        DB_DATABASE=database_name
        DB_USERNAME=db_username
        DB_PASSWORD=db_password

- Create all the necessary tables need for the application by runing the below command.
    
        php artisan migrate

Thats all! The application is now configured.

## API Endpoints and Routes

## References
* [Laravel docs](https://laravel.com/docs/6.x) - Laravel Documentation        
