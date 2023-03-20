# Laravel REST API with Sanctum authentication system

This is an example of a REST API using auth tokens with Laravel Sanctum


##Installation

Clone the repository from GitHub:
```
git clone https://github.com/aleksandarTcode/laravelRestApi
```

Install dependencies using Composer:

```
composer install
```

Copy the .env.example file to .env and update the necessary configuration options

For SQLite, add:
```
DB_CONNECTION=sqlite
DB_HOST=127.0.0.1
DB_PORT=3306
```

Create a _database.sqlite_ file in the _database_ directory

Run the database migrations:
```
php artisan migrate
```

Start the server:
```
php artisan serve
```

## Usage

### This API provides the following endpoints:


```
# Public

GET   /api/products
GET   /api/products/:id
GET   /api/products/search/:name

POST   /api/login
@body: email, password

POST   /api/register
@body: name, email, password, password_confirmation


# Protected
# In protected routes Bearer Token created after login must be used to authenticate user

POST   /api/products
@body: name, slug, description, price

PUT   /api/products/:id
@body: ?name, ?slug, ?description, ?price

DELETE  /api/products/:id

POST    /api/logout
```
