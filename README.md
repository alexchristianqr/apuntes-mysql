# apuntes-mysql
Apuntes importantes sobre MySQL

Todo sobre mysql: BASICO, INTERMEDIO y AVANZADO

## COMANDOS MAS UTILIZADOS

```bash
# Iniciar sesión en MySQL
mysql -u root -p  # Accede a MySQL con el usuario root

# Listar bases de datos existentes
mysql -u root -p -e "SHOW DATABASES;"  # Muestra todas las bases de datos disponibles

# Crear una nueva base de datos
mysql -u root -p -e "CREATE DATABASE nombre_de_la_bd;"  # Crea una base de datos vacía

# Restaurar un backup
mysql -u root -p nombre_de_la_bd < /ruta/del/archivo/backup.sql  # Importa un backup a una base de datos

# Hacer un backup de una base de datos
mysqldump -u root -p nombre_de_la_bd > /ruta/del/archivo/backup.sql  # Genera un backup de la base de datos

# Verificar las tablas de una base de datos
mysql -u root -p -e "USE nombre_de_la_bd; SHOW TABLES;"  # Lista todas las tablas dentro de la base de datos
```

## BASICO

[Comandos mysql nivel Basico](README-basico.md)

## INTERMEDIO

[Comandos mysql nivel Intermedio](README-intermedio.md)

## AVANZADO

[Comandos mysql nivel Avanzado](README-avanzado.md)
