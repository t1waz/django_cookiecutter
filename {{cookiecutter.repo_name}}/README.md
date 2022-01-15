{{cookiecutter.project_name}}
================


HOW TO SETUP
------------

Ask developer team for envs and add then:

    $ mkdir .envs
    $ touch .envs/.development
    $ nano .envs/.development    <--- paste envs

Install local venv:

    $ python3.8 -m venv .venv
    $ source .venv/bin/activate
    $ pip install -r requirements.txt
    
Deploy and install docker:

    $ docker-compose build
    $ docker-compose up


COMMANDS
--------

black:

    black -S --config black.conf app/

flake8:

    flake8 --config flake8 app/
    
tests with cov:

    docker-compose run backend pytest --cov=/app

tests:

    docker-compose run backend pytest