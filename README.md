# apuntes-mysql
Apuntes importantes sobre MySQL

Todo sobre mysql: BASICO, INTERMEDIO y AVANZADO

## COMANDOS MAS UTILIZADOS

```bash
# Iniciar sesión en MySQL
mysql -u root -p  # Accede a MySQL con el usuario root

# Listar bases de datos existentes
mysql -u root -p -e "SHOW DATABASES;"  # Muestra todas las bases de datos disponibles
mysql> SHOW DATABASES;

# Crear una nueva base de datos
mysql -u root -p -e "CREATE DATABASE nombre_de_la_bd;"  # Crea una base de datos vacía
mysql> CREATE DATABASE nombre_de_la_bd;

# Restaurar un backup, ejecutar en CMD; no en terminal de mysql
mysql -u root -p nombre_de_la_bd < /ruta/del/archivo/backup.sql  # Importa un backup a una base de datos

# Hacer un backup de una base de datos, ejecutar en CMD; no en terminal de mysql
mysqldump -u root -p nombre_de_la_bd > /ruta/del/archivo/backup.sql  # Genera un backup de la base de datos

# Verificar las tablas de una base de datos
mysql -u root -p -e "USE nombre_de_la_bd; SHOW TABLES;"  # Lista todas las tablas dentro de la base de datos
mysql> SHOW TABLES;
```

## BASICO

[Comandos mysql nivel Basico](README-basico.md)

## INTERMEDIO

[Comandos mysql nivel Intermedio](README-intermedio.md)

## AVANZADO

[Comandos mysql nivel Avanzado](README-avanzado.md)
