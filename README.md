# symfony 52 book
This is my playground for [Symfony book](https://symfony.com/book)

## Pre-requirements
- IDE: [PhpStorm](https://www.jetbrains.com/phpstorm/) + [Symfony Support Plugin](https://plugins.jetbrains.com/plugin/7219-symfony-support)
- Terminal: [Windows Terminal](https://aka.ms/terminal) or [Hyper](https://hyper.is/)
- Git bash
- PHP 8 + extensions (json, session, pdo_pgsql, xsl, gd, tokenizer, xml, redis, ctype, zip, amqp, intl, mbstring, openssl, sodium, curl)
- Composer
- NodeJS and Yarn
- [Symfony CLI](https://symfony.com/download)
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
