# webman-migration

A migration tool for webman, similar to Laravel migration.

```bash
composer require leekung/webman-migrations
```

Similar to the usage of Laravel migration:

```bash
# generate a migration file
php webman migrate:create create_users_table
# generate a migration file in a specified directory
php webman migrate:create create_users_table --path=admin
# execute the migration
php webman migrate:run
# execute the migration in a specified directory
php webman migrate:run --path=admin
# rollback the migration
php webman migrate:rollback
# check the migration status
php webman migrate:status
# fresh migration from start
php webman migrate:fresh
# generate a data seeding file
php webman seed:create UserSeeder
# execute data seeding
php webman seed:run
```

Specify the database connection:

```bash
$this->schema()->setConnection(Db::connection('mysql2'))->create('orders', function (Blueprint $table) {
    $table->id();
    $table->timestamps();
});
```

Create a database

```bash
php webman create:database test
```

Execute the migration on the specified database:

```bash
php webman migrate:run --database=test
```

Seed the data on the specified database:

```bash
 php webman seed:run --database=test
```
