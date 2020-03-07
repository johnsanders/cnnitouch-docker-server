FROM httpd:2.4.41-alpine
RUN apk update; \
	apk upgrade;
COPY custom.apache.conf /usr/local/apache2/conf/custom.apache.conf
RUN echo "Include /usr/local/apache2/conf/custom.apache.conf" \
    >> /usr/local/apache2/conf/httpd.conf; \
