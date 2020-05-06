FROM occitech/cakephp:5.6-apache

COPY ./php_config.ini $PHP_INI_DIR/conf.d/custom_config.ini
COPY ./apache-config.conf $APACHE_CONFDIR/sites-enabled/000-default.conf
COPY ./apache-status-config.conf $APACHE_CONFDIR/mods-enabled/status.conf

RUN \
	docker-php-ext-install mysqli \
	&& cp /etc/apache2/mods-available/headers.load /etc/apache2/mods-enabled/headers.load \
	&& cp /etc/apache2/mods-available/ssl.load /etc/apache2/mods-enabled/ssl.load \
	&& mv $PHP_INI_DIR/php.ini-development $PHP_INI_DIR/php.ini

EXPOSE 443
