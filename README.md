### Features
- MySql 5.7
- Nginx 1.10
- PHP 7.2
- XDebug 3
- Composer
- Deployer
- Node (latest)
- Nuxt 2.15.3 (with axios)

### Quick start
Install nuxt-app project ([docs](./nuxt-app/README.md))  
Move you project to `./public` directory and run:
```
docker-compose up -d
```

### Database
Move backup file (for ex. `backup.sql`) to root project directory and use restore database commands:
```
docker exec -i ${PROJECT}_db bash
cd /var/www/
cat backup.sql | mysql --host=db --user=admin --password=admin app
```
> Use db instead localhost for database connections.

### How to use XDebug
Add `./public` to `/var/www/public` for `Docker` server.

### For Laravel
Replace current .env to database block project .env
