FROM phpmyadmin/phpmyadmin

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