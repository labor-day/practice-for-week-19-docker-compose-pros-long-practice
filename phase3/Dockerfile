FROM drupal:latest

# Update package list and install git
RUN apt-get update
RUN apt-get install -y git
RUN rm -rf /var/lib/apt/lists/*

# Change working directory to themes
WORKDIR /var/www/html/themes

# Clone the Bootstrap theme from GitHub
RUN git clone --branch 8.x-3.x --single-branch --depth 1 https://git.drupal.org/project/bootstrap.git

# Change ownership to www-data user
RUN chown -R www-data:www-data bootstrap
