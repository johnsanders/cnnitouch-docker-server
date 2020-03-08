
FROM phpmyadmin/phpmyadmin

RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
COPY ./php_config.ini $PHP_INI_DIR/conf.d/custom_config.ini
