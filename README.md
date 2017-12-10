# kapas-api

[![Build Status](https://travis-ci.org/gyKa/kapas-api.svg?branch=master)](https://travis-ci.org/gyKa/kapas-api)
[![Dependency Status](https://gemnasium.com/badges/github.com/gyKa/kapas-api.svg)](https://gemnasium.com/github.com/gyKa/kapas-api)

## Requirements

* PHP ^7.1.3
* MySQL/PostgreSQL (but migrations are written for MySQL only).

## Development

For development you should create 2 MySQL databases: *kapas* and *kapas_tests*.

## Environment variables

There are two variables, *APP_ENV* and *DATABASE_URL*, must be set for **every** environment.
For development those variables are stored in *.env.dist.* and *phpunit.xml.dist* files.
For testing and deployment you have set those variables in testing environment or at [web server level].

| server | environment | variables |
|---|---|---|
| local | dev | *.env.dist* file |
| local | test | *phpunit.xml.dist* file |
| testing (travis) | test | *APP_ENV* is set in **Environment Variables**, *DATABASE_URL* is set in *.travis.yml* file. |
| production | prod | *APP_ENV* and *DATABASE_URL* variables are set at [web server level] |

[web server level]: http://symfony.com/doc/current/configuration/external_parameters.html#configuration-env-var-in-prod
