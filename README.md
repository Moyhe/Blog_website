# Laravel 10 Blog

laravel 10 blog website with docker and postgresql. it has admin panel for managing posts.

# Installation with docker

1.Clone the project

    git clone https://github.com/Moyhe/Blogging_website.git

2.Run composer install

Navigate into project folder using terminal and run

    docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php82-composer:latest \
    composer install --ignore-platform-reqs

3.Copy .env.example into .env

    cp .env.example .env

4.Start the project in detached mode

    ./vendor/bin/sail up -d

5.Set encryption key

    php artisan key:generate --ansi

6.Run migrations

    php artisan migrate

7.seed your data

    php artisan migrate --seed

# Demo Project

    https://drive.google.com/file/d/1y4AoNyxxiKpXC0x4ADD-JL2-QnMRHu7k/view?usp=sharing
