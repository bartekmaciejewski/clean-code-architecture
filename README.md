# WELCOME

# GETTING STARTED

## PREREQUISITES
1. Docker & docker-compose
1. Postman (or other compatible software, ex: Insomnia)
1. IDE

## SETUP PROJECT
In project directory run: 
- `docker-compose up -d` # start container
- `docker-compose exec app composer install` # install composer
- `docker-compose exec app bin/console d:s:c` # create database schema

## Using Postman 
Postman collection file is located at `./.dev/postman.json`. Import it into your Postman.


## Tests
`docker-compose exec app bin/phpunit`

## Troubleshooting
On Win10 running commands: `docker-compose exec app bin/console d:s:c` and `docker-compose exec app bin/phpunit` resulted in:
/usr/bin/env: ‘php\r’: No such file or directory

Added `php` to command has helped:
  `docker-compose exec app php bin/console d:s:c`
  `docker-compose exec app php bin/phpunit`
