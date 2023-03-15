<a name="readme-top"></a>
## Install Laravel Project

- [x] Create a new Laravel project via the Composer create-project command ☟
  ```sh
  composer create-project laravel/laravel:^9.0 projectname
  ```
- [x] Create a new Laravel project via the Composer create-project command inside a folder ☟
  ```sh
  composer create-project laravel/laravel:^9.0 . 
  ```  
You can install any version of laravel project by replacing the version only.
<code> composer create-project laravel/laravel:^<b>version</b> projectname </code>
  
<p align="right">(<a href="#readme-top">back to top</a>)</p>  

## Make Controller

- [x] Make a controller via artisan command ☟
  ```sh
  php artisan make:controller IamController
  ```
<b>Note:</b> When registering routes for controllers, it accepts the uri name, name of the controller with method name.<br/>
<code> Route::get('/iam/{id}', [IamController::class, 'show']); </code> 
  
- [x] Make a single action controller via artisan command ☟
  ```sh
  php artisan make:controller IamController --invokable 
  ```  
<b>Note:</b> When registering routes for single action controllers, it accepts two parameters (url & the name of the controller) only.<br/>
<code> Route::get('/uri_iam', IamController::class); </code> 

- [x] Make resource controller via artisan command ☟
  ```sh
  php artisan make:controller IamController --resource 
  ```  
<b>Note:</b> When registering routes for resource controllers, it accepts two parameters (url & the name of the controller) only.<br/>
<code> Route::get('/uri_iam', IamController::class); </code>   
  
- [x] Make resource controller specifying the Model instance via artisan command ☟
  ```sh
  php artisan make:controller IamController --model=ModelName --resource
  ```  
  
- [x] Make resource controller specifying the Model instance from a Request via artisan command ☟
  ```sh
  php artisan make:controller IamController --model=ModelName --resource --requests
  ```    
 
- [x] Make an API resource controller via artisan command ☟
  ```sh
  php artisan make:controller IamController --api
  ```     
<p align="right">(<a href="#readme-top">back to top</a>)</p>  

## Make Model

- [x] Create an Eloquent Model via artisan command ☟
  ```sh
  php artisan make:model ModelName
  ```     
- [x] Create an Eloquent Model generating migration via artisan command ☟
  ```sh
  php artisan make:model Flight --m
  
  Or
  
  php artisan make:model Flight --migration
  ```     


<p align="right">(<a href="#readme-top">back to top</a>)</p>  

## Database Migration

- [x] Migrate All The Tables
  ```sh
  php artisan migrate
  ```
- [x] Migrate All The Tables & Remove All Data
  ```sh
  php artisan migrate:refresh
  ```
- [x] Migrate All The Tables & Remove All Data & Run Seeder
  ```sh
  php artisan migrate:refresh --seed
  ```
- [x] Migrate A Specific Table & Remove Data From That Table Only
  ```sh
  php artisan migrate:refresh --path=database/migrations/2023_10_03_009502_create_users_table.php
  ```
  
<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Database Seed

* Create A Seeder
  ```sh
  php artisan make:seeder IamSeeder
  ```
* Run Seeder(s)
  ```sh
  php artisan db:seed
  ```  
* Run A Specific Seeder 
  ```sh
  php artisan db:seed --class=SeederFileName
  ```

