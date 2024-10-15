FROM phpmyadmin/phpmyadmin

# Install Imagick, Intl, GD, and other dependencies
RUN apt-get update && \
    apt-get install -y libmagickwand-dev libicu-dev libpng-dev --no-install-recommends && \
    pecl install imagick && \
    docker-php-ext-install intl gd && \
    docker-php-ext-enable imagick intl gd

RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Copy the custom configuration file
COPY . .

# Set the timezone
ENV TZ=UTC
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Set the working directory
WORKDIR /var/www/html

# Expose the port
EXPOSE 80

# Start the server
CMD ["apache2-foreground"]