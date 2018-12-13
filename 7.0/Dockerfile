FROM php:7.0-fpm-jessie

RUN apt-get update \
 && apt-get install -y \
    supervisor \
    zlib1g-dev \
    libicu-dev \
    libxml2-dev \
    #gd
    libpng12-dev \
    libjpeg62-turbo \
    libjpeg-dev \
    libwebp-dev \
    libfreetype6-dev \
    libxpm-dev \
    #gd end
    locales \
    libxslt-dev \
    libpq-dev \
 && docker-php-ext-configure \
    gd \
    --with-gd \
    --with-webp-dir \
    --with-jpeg-dir=/usr/lib \
    --with-png-dir \
    --with-xpm-dir \
    --with-freetype-dir \
 && docker-php-ext-configure \
    intl \
 && docker-php-ext-install \
    calendar \
    opcache \
    bcmath \
    zip \
    pdo_mysql \
    mbstring \
    mysqli \
    soap \
    xml \
    gettext \
    pcntl \
    shmop \
    sockets \
    sysvmsg \
    sysvsem \
    sysvshm \
    wddx \
    xsl \
    gd \
    exif \
    intl \
    pgsql \
    pdo_pgsql \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*
