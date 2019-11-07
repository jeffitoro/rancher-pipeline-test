FROM wordpress:latest

# Add sudo in order to run wp-cli as the www-data user 
RUN apt-get update && apt-get install -y sudo less unzip && curl -o /bin/wp-cli.phar https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar

COPY wp-su.sh /bin/wp

RUN chmod +x /bin/wp-cli.phar /bin/wp && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

VOLUME [ "/var/www/html" ]

WORKDIR /wordpress/app/

COPY --chown=www-data ./wp-content /var/www/html/wp-content/

EXPOSE 80