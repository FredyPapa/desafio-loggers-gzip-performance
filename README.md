# Desafío: Loggers, GZIP y Análisis de Performance

## Instalación del proyecto

Ejecutar el código ```npm install``` para reconstruir los módulos de Node.
Crear el archivo ```.env``` con el siguiente contenido
~~~
PORT=8080
NOD_ENV=development
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=ecommerce
CORS=*

CONNECTION_STRING=mongodb+srv://root:coderhouse@cursonode.o3yqn.mongodb.net/proyecto?retryWrites=true&w=majority
SECRET=afterclass
© 2022 GitHub, Inc.
Terms
Privacy
Sec
~~~

### Comandos ejecutados en el proceso

## Ejecutar el proyecto con Prof
~~~
node --prof index.js
~~~

## Test /info con y sin console log
~~~
artillery quick --count 50 -n 20 http://localhost:8080/info > reporte_artillery_info_con_console_log.txt
artillery quick --count 50 -n 20 http://localhost:8080/info > reporte_artillery_info_sin_console_log.txt
~~~

## Ejecutar comando para decodificar los archivos log creados
~~~
node --prof-process pref_info_con_console_log.log > pref_info_con_console_log.txt
node --prof-process pref_info_sin_console_log.log > pref_info_sin_console_log.txt
~~~

## Test /api/random con y sin console log
~~~
artillery quick --count 50 -n 20 http://localhost:8080/api/randoms?cant=100 > reporte_artillery_randoms_con_console_log.txtreporte_artillery_randoms_conn_console_log.txt
artillery quick --count 50 -n 20 http://localhost:8080/api/randoms?cant=100 > reporte_artillery_randoms_con_console_log.txtreporte_artillery_randoms_sin_console_log.txt
~~~
