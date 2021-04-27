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

## Launching a Local Web Server
```bash
# starts web server in the background (-d flag)
symfony server:start -d

# open the website in a browser from the CLI
symfony open:local
```

## Going to Symfony Cloud
### Add SymfonyCloud configuration
```bash
symfony project:init
```
### Initialize project on Symfony Cloud
```bash
symfony project:create --title="book" --plan=development
```
### Deploy on Symfony Cloud
```bash
symfony deploy

# open symfony cloud remote 
symfony open:remote
```