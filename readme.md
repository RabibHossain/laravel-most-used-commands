## Install Laravel Project

* create a new Laravel project via the Composer create-project command 
  ```sh
  composer create-project laravel/laravel:^9.0 projectname
  ```
* create a new Laravel project via the Composer create-project command inside a folder
  ```sh
  composer create-project laravel/laravel:^9.0 . 
  ```  
You can install any version of laravel project by replacing the version name.
composer create-project laravel/laravel:^<b>version</b> projectname
  
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

