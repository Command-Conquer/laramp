Docker compose para laravel
Los archivos para la aplicación se instalan en la raíz y en /var/www/html del contenedor.

PHP 7.4.6
MySQL 8
Nginx
PHPMyAdmin
Redis
GDImage
OPCache

Configuración standard de Nginx

Para acceder en el entorno en Windows 10 tener en cuenta que la dirección es la que nos proporciona dockercompose, no es 127.0.0.1 ni localhost.

Para acceder a PhpMyadmin acceder a http://ipdeldocker:8080 siendo user el usuario y test la contraseña.

El directorio public es la raíz del servidor. Para ver la configuración de php http://ipdeldocker/dameinfo.php

Si se quiere utilizar wordpress descomentar la sección correspondiente, si se quiere utilizar laravel borrar el directorio public antes de instalarlo.
