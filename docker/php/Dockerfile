FROM php:8.2-fpm

# RUN apt-get update && apt-get install -y \

# available php extension
# bcmath bz2 calendar ctype curl dba dl_test dom enchant exif ffi fileinfo filter ftp 
# gd gettext gmp hash iconv imap intl json ldap mbstring mysqli oci8 odbc opcache pcntl 
# pdo pdo_dblib pdo_firebird pdo_mysql pdo_oci pdo_odbc pdo_pgsql pdo_sqlite pgsql phar 
# posix pspell random readline reflection session shmop simplexml snmp soap sockets 
# sodium spl standard sysvmsg sysvsem sysvshm tidy tokenizer xml xmlreader xmlwriter 
# xsl zend_test zip
RUN docker-php-ext-install -j$(nproc) pdo_mysql mysqli

RUN php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer

WORKDIR /usr/share/nginx/html