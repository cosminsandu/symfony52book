# symfony 52 book
This is my playground for [Symfony book](https://symfony.com/book)

## Pre-requirements
- IDE: [PhpStorm](https://www.jetbrains.com/phpstorm/) + [Symfony Support Plugin](https://plugins.jetbrains.com/plugin/7219-symfony-support)
- Terminal: [Windows Terminal](https://aka.ms/terminal) or [Hyper](https://hyper.is/)
- Git bash
- PHP 8 + extensions (json, session, pdo_pgsql, xsl, gd, tokenizer, xml, redis, ctype, zip, amqp, intl, mbstring, openssl, sodium, curl)
- Composer
- NodeJS and Yarn
- [Symfony CLI](https://symfony.com/download) & [Symfony account](https://symfony.com/account)
- Docker & Docker Compose

To check symfony requirements run:
```bash
symfony check:requirements
```

To check that all **book** requirements run:
```bash
symfony book:check-requirements
```

## Create new symfony project
```bash
symfony new --version=5.2-1 --book guestbook
```

## Local server
### Start local server
```bash
# starts web server in the background (-d flag)
symfony server:start -d
```

### Open local site 
```bash
# open the website in a browser from the CLI
symfony open:local
```

### Logs from local site 
```bash
# logs from local env
symfony server:log
```

## SymfonyCloud
### Initialise
```bash
symfony project:init
```
### Create project on SymfonyCloud
```bash
symfony project:create --title="book" --plan=development
symfony project:list
```

### Deploy on SymfonyCloud
```bash
symfony deploy
# Note: you should be on branch "master"; 
# on branch "main" I get:
# could not determine current environment for this project: current git branch name doesn't match any SymfonyCloud environments.
```

### Open site on SymfonyCloud
```bash
# open SymfonyCloud remote 
symfony open:remote
```

### Logging on SymfonyCloud
```bash
# logs from SymfonyCloud
symfony logs
```

### SSH on SymfonyCloud 
```bash
# connect to SymfonyCloud via SSH
symfony ssh
```

## Install more dependencies
### Profiler
```bash
symfony composer req profiler --dev
```
### Logger
```bash
symfony composer req logger
```
### Debug
```bash
symfony composer req debug --dev
```
### Maker bundle
```bash
symfony composer req maker --dev

# generated command for maker bundle 
symfony console list make
```
### Annotations
```bash
symfony composer req annotations
```

## Generate Controller
```bash
symfony console make:controller ConferenceController
```

## Database
### Docker 
- create ``docker-compose.yaml`` file
```bash
#Start Docker Compose in the background (-d):
docker-compose up -d

#List containers
docker-compose ps
docker-compose ps -a

#View output from containers
docker-compose logs
```

- accessing local database
```bash
symfony run psql
```
DataBase can be accessing GUI (e.g. Heidy Sql) with 
the credentials from ``docker-compose.yaml`` 
and port from ``docker-compose ps -a``  

- dump database data
```bash
symfony run pg_dump --data-only > dump.sql
```

- restore the data
```bash
symfony run psql < dump.sql
```
