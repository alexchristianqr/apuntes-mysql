## BASICO

```bash
# Iniciar sesión en MySQL
mysql -u root -p  # Conectarse a MySQL como root
```

```bash
# Crear una base de datos
mysql -u root -p -e "CREATE DATABASE nombre_de_la_bd;"  # Crea una nueva base de datos
```

```bash
# Eliminar una base de datos
mysql -u root -p -e "DROP DATABASE nombre_de_la_bd;"  # Borra una base de datos completamente
```

```bash
# Seleccionar una base de datos
mysql -u root -p -e "USE nombre_de_la_bd;"  # Cambia al contexto de una base de datos específica
```

```bash
# Mostrar tablas de una base de datos
mysql -u root -p -e "SHOW TABLES;"  # Lista todas las tablas de la base de datos actual
```

```bash
# Ver la estructura de una tabla
mysql -u root -p -e "DESCRIBE nombre_tabla;"  # Muestra columnas y tipos de datos de una tabla
```

```bash
# Insertar un registro en una tabla
mysql -u root -p -e "INSERT INTO nombre_tabla (columna1, columna2) VALUES ('valor1', 'valor2');"  # Agrega un nuevo registro
```

```bash
# Consultar datos de una tabla
mysql -u root -p -e "SELECT * FROM nombre_tabla LIMIT 10;"  # Muestra los primeros 10 registros de una tabla
```
