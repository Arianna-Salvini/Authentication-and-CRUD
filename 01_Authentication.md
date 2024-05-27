# Authentication and CRUD:

## First steps for Authentication:

1. Instal laravel as usual
2. Instal laravel\breez
3. Create scaffolding
4. Create default scaffolding for Bootstrap

```zsh
composer create-project laravel/laravel:^10.0 example-app

composer require laravel/breeze --dev

php artisan breeze:install

  - Blade with Alpine
  - no dark mode
  - Pest

composer require pacificdev/laravel_9_preset

php artisan preset:ui bootstrap --auth
    npm install

    - Rename vite.config.js to vite.config.cjs

    php artisan serve
    npm run dev
```
- Modify .env file with DB data (port:8889, psw:root)

## RAD: Refactoring Admin Dashboard

1. Create a controller to handle the dashboard request

```zsh
php artisan make:controller Admin/DashboardController
```
2. Update routes in web.php

```php
Route::get('/dashboard', [DashboardController::class, 'index'])->middleware(['auth', 'verified'])->name('dashboard');

"(1st put DasboardController class and second value put 'index'
remember to import with use dashboard)"

```


3. Into DashboardController, go to index method and return the view for the dashboard

```php
class DashboardController extends Controller
{
    function index()
    {
        return view('dashboard');
    }
}
```

4. Return to web.php and create the middleware with 'auth' and 'verified' as values

```php
Route::middleware()->name()->prefix()->group();

    // - group() needs a closure -> use a callback function where you put all routes need to be protected by thr authentication system

   // - Also, all routes need to share the name and the prefix

   // - name -> admin. -> all routes in it wiil have admin. as starting point -> admin.folder1.index; admin.folder1.show; admin.folder2 ...

   //  - prefix -> admin (no dot) -> admin/folder; admin/folder2...

``` 

```php

Route::middleware(['auth', 'verified'])
    ->name('admin.')
    ->prefix('admin')
    ->group(function () {
        //routes
    });
```

5. Take the dashboard Route::get and put into middleware gruop, change first parameter, leaving only '/' as URL beacause the prefix is inherited by the prefix of the group

6. Go to RouteServiceProvider.php and change 'dashboard' into 'admin'
```php

//RouteServiceProvider.php
    public const HOME = '/admin';
```

## Add a new layout file for the admin

1. Duplicate app.blade.php and rename it as admin.blade.php

    - Whit command line:
```zsh
    cd resources/views/layouts
    cp app.blade.php admin.blade.php
```
2. Extend new admin layout inside the dashboard.blade.php -> @extend('layout.admin')

## CRUD operations:

1. Creation of :

- Model     -|
- Migration _| -> (m)
- Seeder -> (s)
- Controller resource -> (cr)
- Two Form Requests (R)

```zsh
php artisan make:model Nameprojecthere -mscrR
```
Continue to:
# [CRUD operations](02_CRUD_operation.md)

