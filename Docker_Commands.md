# Docker Commands Cheat Sheet

### DOCKER-COMPOSE COMMANDS:
> Build Docker Enviornment and run as detached

    $ docker-compose up -d --build

> Bring down said environment

    $ docker-compose down


### COMPOSER COMMANDS
**Workflow of command:**

1. Start up composer container (`run`).

2. Run the coomposer command inside project (`composer ...`).

3. Bring down composer container when job is completed (`--rm`).

> Execute Composer Command

    $ docker-compose run --rm composer require laravel/laravel


### NPM COMMANDS
> Install projects `package.json` dependencies

    $ docker-compose run --rm npm install

> Compile assests with Laravels webpack-mixer

    $ docker-compose run --rm npm run dev

### ARTISAN COMMANDS

> Run Database Migrations

    $ docker-composer run --rm artisan migrate


### Extras
If you are not installing these extra containers inside the project, and instead using your local machine and sharing your systems configure of composer, or npm, a command would look like the following:

> Ex). Run DB Migrations

    $ docker-compose exec php php /var/www/html/artisan migrate ...

 > With installing these extra container above, sysntax is much cleaner, and allows to "Dockerize your project better."