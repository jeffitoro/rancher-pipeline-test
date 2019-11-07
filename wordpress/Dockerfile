FROM wordpress:latest

# Install xdebug
# RUN pecl install xdebug && docker-php-ext-enable xdebug && apt-get update && apt-get -y install less && curl -s -o /usr/local/bin/wp \
#     https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar \
#     && chmod +x /usr/local/bin/wp

# VOLUME [ "/var/www/html" ]

# WORKDIR /var/www/html

# RUN useradd -d /app -s /bin/bash app \
#  && chown -R app . && sudo apt-get update
# USER app

# USER www-data

# CMD cd ./app && wp --allow-root core download

# USER daemon

# CMD wp core config \
# USER root

# Add sudo in order to run wp-cli as the www-data user 
# RUN apt-get update && apt-get install -y sudo less unzip && curl -o /bin/wp-cli.phar https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar

# COPY wp-su.sh /bin/wp

# RUN chmod +x /bin/wp-cli.phar /bin/wp && apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
#     --dbhost=${MYSQL_HOST:-db}:${MYSQL_PORT:-3306} \
#     --dbuser=${MYSQL_USER:-root} \
#     --dbpass=${MYSQL_PASSWORD:-root} \
#     --dbname=${MYSQL_DATABASE:-wp} \
#     --skip-check \
#  # Wait for the database to be ready
#  && dockerize -wait tcp://${MYSQL_HOST:-db}:${MYSQL_PORT:-3306} -timeout 30s \
#  && wp core install \
#     --url=${WORDPRESS_URL:-localhost} \
#     --title=${WORDPRESS_TITLE:-'WordPress site'} \
#     --admin_user=${WORDPRESS_ADMIN_USER:-admin} \
#     --admin_password=${WORDPRESS_ADMIN_PASSWORD:-admin} \
#     --admin_email=${WORDPRESS_ADMIN_MAIL:-admin@example.com} \
#  && wp option update permalink_structure '/%year%/%monthnum%/%day%/%postname%/' \
#  && wp server --host=0.0.0.0:8080


# COPY --chown=www-data:www-data ./app/ /var/www/html/

EXPOSE 80