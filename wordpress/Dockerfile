FROM wordpress:latest

# Add sudo in order to run wp-cli as the www-data user 
RUN apt-get update && apt-get install -y sudo less

# Add WP-CLI 
RUN curl -o /bin/wp-cli.phar https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
COPY wp-su.sh /bin/wp
RUN chmod +x /bin/wp-cli.phar /bin/wp

# Cleanup
RUN apt-get clean
RUN rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# COPY ./app  /var/www/html
# ADD ./app/* /var/www/html/

VOLUME [ "/var/www/html" ]

COPY --chown=www-data:www-data app /var/www/html/

RUN [ -d "/var/www/html/wp-admin" && ! -h "/var/www/html/wp-admin" ] && echo "Directory /var/www/html/wp-admin exists." || echo "Error: Directory /var/www/html/wp-admin exists but point to $(readlink -f /var/www/html/wp-admin)."

EXPOSE 80