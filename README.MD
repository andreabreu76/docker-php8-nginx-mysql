# Conteiners PHP8, Nginx & MySQL

## Steps...

Primeiro, mude o .env do Docker para seus parametros:

```bash
PROJECT_NAME=projectname
``` 

Seguimos ...

```bash
cd protectname/src
``` 

```bash
docker exec -it projectname-app composer create-project laravel/laravel .
``` 

Edite o .env do projeto com os dados do novo banco de dados.

```bash
DB_CONNECTION=mysql
DB_HOST=database
DB_PORT=3306
DB_DATABASE=homestead
DB_USERNAME=homestead
DB_PASSWORD=secret
``` 

Algumas vezes é necessário setar permissões.

```bash
sudo chown -R $USER:$USER .
``` 

```bash
sudo chmod -R 777 storage/
``` 

```bash
docker exec -it projectname-app php artisan config:clear
``` 
```bash
docker exec -it projectname-app php artisan migrate
``` 
