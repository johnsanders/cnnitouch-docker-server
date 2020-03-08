FROM occitech/cakephp:5.6-apache

RUN \
	cp /etc/apache2/mods-available/headers.load /etc/apache2/mods-enabled/headers.load  \
	&& mv "$PHP_INI_DIR/php.ini-development" "$PHP_INI_DIR/php.ini"

COPY ./php_config.ini $PHP_INI_DIR/conf.d/custom_config.ini
COPY ./apache-config.conf $APACHE_CONFDIR/sites-enabled/000-default.conf
