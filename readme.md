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

