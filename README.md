Enable the dblib module then set up a connection in settings.php

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
