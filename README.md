![alt text](demo.png "Demo Image")

# Merklion Chat Demo App

## How to use

### 1. Preparation

Clone the repo and change your work directory to root of sources

    git clone https://github.com/EvilFreelancer/merklion-chat.git
    cd nowescape-blockchain

Now you need prepare docker compose config file:

    cp docker-compose.yml.dist docker-compose.yml

Inside `docker-compose.yml` you need change the values to the ones you
need, for example you do not want to tun this project on `80` port, to
fix that you need just change this line `80:80` to what you need (`7777:80`).

Run first iteration of Docker environment

    docker-compose up -d

### 2. Install all required components

I assume that there are no development tools on your computer, so you
need to login to Laravel container:

    docker-compose exec laravel bash

Fix write permissions on a few important folders

    chown apache:apache bootstrap/ -R
    chown apache:apache storage/ -R

End exit from container

    exit

## The End

Now you just need open following page http://localhost in your browser
and you will get the result of my work.

Thanks for reading!
