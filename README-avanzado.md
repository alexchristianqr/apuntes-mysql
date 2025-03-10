## AVANZADO

```bash
# Restaurar un backup y registrar la salida en un log
mysql -u root -p nombre_de_la_bd < /ruta/backup.sql | tee /ruta/restore_log.txt  # Guarda un registro del proceso de restauración
```

```bash
# Hacer un backup de todas las bases de datos
mysqldump -u root -p --all-databases > /ruta/backup.sql  # Exporta todas las bases de datos en un solo archivo
```

```bash
# Hacer un backup de una base de datos específica excluyendo tablas
mysqldump -u root -p nombre_de_la_bd --ignore-table=nombre_de_la_bd.tabla1 --ignore-table=nombre_de_la_bd.tabla2 > /ruta/backup.sql  # Excluye ciertas tablas al exportar
```

```bash
# Restaurar solo una tabla desde un backup grande
mysql -u root -p nombre_de_la_bd < <(sed -n '/DROP TABLE.*nombre_tabla/,/UNLOCK TABLES/p' /ruta/backup.sql)  # Extrae y restaura solo una tabla
```

```bash
# Ver conexiones activas en el servidor MySQL
mysql -u root -p -e "SHOW PROCESSLIST;"  # Muestra todas las conexiones activas en MySQL
```

```bash
# Detener una consulta MySQL que está consumiendo demasiados recursos
mysql -u root -p -e "KILL ID_proceso;"  # Finaliza un proceso en ejecución en MySQL
```

```bash
# Reiniciar el servicio MySQL en Linux
sudo systemctl restart mysql  # Reinicia el servicio MySQL en sistemas Linux
```

```bash
# Ver el estado del servicio MySQL en Linux
systemctl status mysql  # Muestra si MySQL está en ejecución
```

```bash
# Verificar si MySQL está corriendo en Windows
sc query MySQL80  # Muestra el estado del servicio MySQL en Windows
```
