Provisioning a new site
=======================

## Required packages:

* nginx
* Pyhton 3.6
* virtualenv + pip
* Git

eg, on Ubuntu:

    sudo add-apt-repository ppa:deadsnakes/ppa
    sudo apt update
    sudo apt install nginx git pyhton36 python3.6-venv

## Nginx Virtual Host config

* see nginx.template.conf
* replace DOMAIN with, e.g., staging.my-domain.com

## Systemd service

* see gunicorn-systemd.template.service
* replace DOMAIN with, e.g., staging.my-domain.com

## Folder structure

Assume we have a user account at /home/username

/home/username
|__ sites
    |__ DOMAIN1
    |   |__ .env
    |   |__ db.sqlite3
    |   |__ manage.py etc
    |   |__ static 
    |   |__ virtualenv
    |__ DOMAIN2
    |   |__ .env
    |   |__ db.sqlite3
    |   |__ etc 