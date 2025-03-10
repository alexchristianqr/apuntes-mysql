## INTERMEDIO

```bash
# Restaurar un backup desde un archivo SQL
mysql -u root -p nombre_de_la_bd < /ruta/del/archivo/backup.sql  # Restaura una base de datos desde un archivo
```

```bash
# Realizar un backup con compresión
mysqldump -u root -p nombre_de_la_bd | gzip > /ruta/del/archivo/backup.sql.gz  # Comprime el backup al guardarlo
```

```bash
# Restaurar un backup comprimido
gunzip < /ruta/del/archivo/backup.sql.gz | mysql -u root -p nombre_de_la_bd  # Descomprime y restaura el backup
```

```bash
# Mostrar tamaño de cada base de datos
mysql -u root -p -e "SELECT table_schema AS 'Base de Datos', SUM(data_length + index_length) / 1024 / 1024 AS 'Tamaño (MB)' FROM information_schema.tables GROUP BY table_schema;"  # Muestra el tamaño de cada base de datos en MB
```

```bash
# Mostrar tamaño de una tabla específica
mysql -u root -p -e "SELECT table_name, ROUND((data_length + index_length) / 1024 / 1024, 2) AS 'Tamaño (MB)' FROM information_schema.tables WHERE table_schema = 'nombre_de_la_bd' AND table_name = 'nombre_tabla';"  # Tamaño de una tabla en MB
```

```bash
# Optimizar una tabla para liberar espacio
mysql -u root -p -e "OPTIMIZE TABLE nombre_tabla;"  # Reorganiza y optimiza el almacenamiento de una tabla
```
