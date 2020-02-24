This fork of dblib will not work for installing drupal to MSSQL (see https://github.com/andypost/dblib)

If you just need the connection but don't need to install Drupal to MSSQL then you you can reference the driver directly in your settings.php

e.g.

```php
$databases['sqlsrv']['default'] = array(
    'database' => 'mydb',
    'username' => 'sa',
    'password' => '*****',
    'host' => 'mssql_host',
    'port' => '1433',
    'driver' => 'dblib',
    'namespace' => 'Drupal\\dblib\\Driver',
    'prefix' => '',
    // Add PDO options to override the defaults if required.
    'pdo' => [
      \PDO::ATTR_ERRMODE => \PDO::ERRMODE_WARNING,
    ]
);
```
