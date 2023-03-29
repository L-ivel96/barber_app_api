# Barber App

Um projeto do canal Raphael Pontes.
- [Canal Youtube](https://www.youtube.com/channel/UCv4EWSgNQqqv6HLpGyCkePQ)

- Verifique o Charset do banco "app_barbearia" criado, ele deve ser UTF8mb4

## Comandos pós instalação]
Acessar o container
```docker exec -it laravel-app bash```

```chmod -R 777 storage```

```composer install```

```php artisan key:generate```

```php artisan migrate:install```

```php artisan migrate```

## Comandos rapidos

#### Acessando o container
```docker exec -it laravel-app bash```

#### Cria model, migration, factory e seeder da entidade
```php artisan make:model Flight -mfs```

#### Cria migration
```php artisan make:migration create_users_table```

#### Executa migrations
```php artisan migrate```







