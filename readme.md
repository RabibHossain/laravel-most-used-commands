## Install Laravel Project

* Create a new Laravel project via the Composer create-project command 
  ```sh
  composer create-project laravel/laravel:^9.0 projectname
  ```
* Create a new Laravel project via the Composer create-project command inside a folder
  ```sh
  composer create-project laravel/laravel:^9.0 . 
  ```  
You can install any version of laravel project by replacing the version only.
<code> composer create-project laravel/laravel:^<b>version</b> projectname </code>
  
## Make Controller

* Make a controller via artisan command 
  ```sh
  php artisan make:controller IamController
  ```
<b>Note:</b> When registering routes for controllers, it accepts the uri name, name of the controller with method name.<br/>
<code> Route::get('/iam/{id}', [IamController::class, 'show']); </code> 
  
* Make a single action controller via artisan command 
  ```sh
  php artisan make:controller IamController --invokable 
  ```  
<b>Note:</b> When registering routes for single action controllers, it accepts two parameters (url & the name of the controller) only.<br/>
<code> Route::get('/uri_name', IamController::class); </code> 

* Make resource controller via artisan command 
  ```sh
  php artisan make:controller IamController --resource 
  ```  
<b>Note:</b> When registering routes for resource controllers, it accepts two parameters (url & the name of the controller) only.<br/>
<code> Route::get('/uri_name', IamController::class); </code>   
  
* Make resource controller specifying the Model instance via artisan command 
  ```sh
  php artisan make:controller IamController --model=ModelName --resource
  ```  
  
* Make resource controller specifying the Model instance from a Request via artisan command 
  ```sh
  php artisan make:controller IamController --model=ModelName --resource --requests
  ```    
 
* Make an API resource controller via artisan command 
  ```sh
  php artisan make:controller IamController --api
  ```     
  
## Database Migration(s)

* Migrate All The Tables
  ```sh
  php artisan migrate
  ```
  
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

