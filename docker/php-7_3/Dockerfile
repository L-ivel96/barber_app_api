FROM php:7.3-apache

# Instala as extensões necessárias do PHP
RUN apt-get update && \
    apt-get install -y \
        libzip-dev \
        zip \
        unzip

RUN docker-php-ext-install \
        mysqli pdo \
        pdo_mysql \
        zip

# Define o diretório de trabalho
WORKDIR /var/www/html

# Install Composer
RUN php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer
RUN alias composer='php /usr/bin/composer'

# Define as permissões dos arquivos do aplicativo
RUN chown -R www-data:www-data /var/www/html

# Define o comando de inicialização do contêiner
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]

#Apache - rewrite_module para manipular rotas
RUN a2enmod rewrite

# SSL
RUN a2enmod ssl
RUN a2ensite default-ssl