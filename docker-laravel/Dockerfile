# Set master image
FROM php:7.2-fpm-alpine

# Set working directory
WORKDIR /var/www/html

# Install PHP Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# Copy existing application directory
COPY . .


#https://github.com/docker-library/php/blob/331e0f4b4d365990a8fbd487da9c6494ad10ccba/7.2/alpine3.10/fpm/Dockerfile
# nó đã chạy cmd rồi 
# EXPOSE 9000
# CMD ["php-fpm"]