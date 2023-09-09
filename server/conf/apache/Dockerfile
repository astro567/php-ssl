FROM php:apache

WORKDIR /etc/apache2/sites-enabled
RUN rm -rf default-ssl.conf && rm -rf domain.dev.conf && \
    ln -s /etc/apache2/sites-available/domain.dev.conf domain.dev.conf && \
    update-ca-certificates && \
    a2enmod ssl headers deflate expires && \
    service apache2 restart

EXPOSE 80
EXPOSE 443

RUN chown -R www-data:www-data /var/www/html/ && \
    chmod -R 777 /var/www/html/