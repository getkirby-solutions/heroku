## Notes

- site must be at root level
  - todo: try subdirectory

## Setup

- RUN git init (or git clone)
- RUN composer init
  - require
    - php
    - ext-mbstring (latest \*)
    - ext-curl (latest \*)
- RUN composer update
- RUN echo "web: vendor/bin/heroku-php-apache2" >> Procfile
- Reference:
  - [PHP Support](https://devcenter.heroku.com/articles/php-support)
  - [PHP Settings](https://devcenter.heroku.com/articles/custom-php-settings)

## Heroku deploy

- RUN heroku create <name>
- RUN
  - git add --all
  - git commit --message "<desc>"
  - git push origin master
  - git push heroku master
- RUN heroku run bash # to inspect server

## Heroku rename app

- RUN heroku apps:rename <newname>
