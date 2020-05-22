FROM php:7.4-fpm
RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng-dev \
            build-essential \
            default-mysql-client \
            libmagickwand-dev \
            libzip-dev \
            libonig-dev \
            locales \
            zip \
            jpegoptim optipng pngquant gifsicle \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) gd

# Clear cache
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Installing extensions
RUN docker-php-ext-install pdo_mysql mbstring zip exif pcntl bcmath opcache

# Setting locales
RUN echo es_ES.UTF-8 UTF-8 > /etc/locale.gen && locale-gen

# Changing Workdir
WORKDIR /var/www/html
