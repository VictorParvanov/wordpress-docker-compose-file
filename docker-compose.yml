version: "3"

services:
  db:
    image: mysql:5.7
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: Admin123456!
      MYSQL_DATABASE: MyWordPressDatabaseName
      MYSQL_USER: admin
      MYSQL_PASSWORD: Admin123456!
    volumes:
      - mysql_data:/var/lib/mysql

  wordpress:
    depends_on:
      - db
    image: wordpress:latest
    restart: always
    ports:
      - "8000:80"
    environment:
      WORDPRESS_DB_HOST: db:3306
      WORDPRESS_DB_USER: admin
      WORDPRESS_DB_PASSWORD: Admin123456!
      WORDPRESS_DB_NAME: MyWordPressDatabaseName
    volumes:
      - wordpress_data:/var/www/html

volumes:
  mysql_data:
  wordpress_data:
