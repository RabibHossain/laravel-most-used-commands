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
  php artisan make:model ModelName --m
  
  Or
  
  php artisan make:model ModelName --migration
  ```     

- [x] Generate various other types of classes while generating a model, such as factories, seeders, policies, controllers, and form requests. ☟
  ```sh
  # Generate a model and a ModelFactory class...
  php artisan make:model ModelName --factory
  php artisan make:model ModelName -f

  # Generate a model and a ModelSeeder class...
  php artisan make:model ModelName --seed
  php artisan make:model ModelName -s

  # Generate a model and a ModelController class...
  php artisan make:model ModelName --controller
  php artisan make:model ModelName -c

  # Generate a model, ModelController resource class, and form request classes...
  php artisan make:model ModelName --controller --resource --requests
  php artisan make:model ModelName -crR

  # Generate a model and a ModelPolicy class...
  php artisan make:model ModelName --policy

  # Generate a model and a migration, factory, seeder, and controller...
  php artisan make:model ModelName -mfsc

  # Shortcut to generate a model, migration, factory, seeder, policy, controller, and form requests...
  php artisan make:model ModelName --all

  # Generate a pivot model...
  php artisan make:model Member --pivot
  ```
- [x] Inspecting Model provides a convenient overview of all the model's attributes and relations ☟
  ```sh
  php artisan model:show ModelName
  ```     

<p align="right">(<a href="#readme-top">back to top</a>)</p>  

## Database Migration

- [x] Migrate All The Tables ☟
  ```sh
  php artisan migrate
  ```
- [x] Migrate All The Tables & Remove All Data ☟
  ```sh
  php artisan migrate:refresh
  ```
- [x] Migrate All The Tables & Remove All Data & Run Seeder ☟
  ```sh
  php artisan migrate:refresh --seed
  ```
- [x] Migrate A Specific Table & Remove Data From That Table Only ☟
  ```sh
  php artisan migrate:refresh --path=database/migrations/2023_10_03_009502_create_users_table.php
  ```
- [x] Migrate A Specific Table to add/update/delete a column ☟
  ```sh
  php artisan migrate --path=database/migrations/2023_10_03_009502_add_phone_to_users_table.php
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

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Validator Rules

* Image Dimension Validation Rules 
  ```sh
  # required image
  'icon' => 'required|image'
  # required image with file extentions
  'icon' => 'required|image|mimes:png,webp,svg'
  # required image with fixed size dimension pixels
  'icon' => 'required|image|mimes:png,webp,svg|dimensions:width=512,height=512'
  # required image with fixed size dimension ratio
  'icon' => 'required|image|mimes:png,webp,svg|dimensions:ratio=2/1'
  # required image with maximum size of dimension pixels
  'icon' => 'required|image|mimes:png,webp,svg|dimensions:max_width=512,max_width=512'
  # required image with minimum size of dimension pixels
  'icon' => 'required|image|mimes:png,webp,svg|dimensions:min_width=512,min_width=512'
  ```

