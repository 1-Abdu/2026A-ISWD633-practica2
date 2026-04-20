### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:15-alpine3.21
```
docker network create red-datos
```
```
docker run -d --name srv-postgres --network red-datos -e POSTGRES_PASSWORD=<password> postgres:15-alpine3.21
```

### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4
```
docker run -d --name pgadmin-client --network red-datos -p 8080:80 -e PGADMIN_DEFAULT_EMAIL=admin@test.com -e PGADMIN_DEFAULT_PASSWORD=admin dpage/pgadmin4
```
La figura presenta el esquema creado en donde los puertos son:
- a: 8080
- b: 80
- c: 5432

![Imagen](esquema-2-ejercicio.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
# COMPLETAR CON UNA CAPTURA DEL LOGIN

<img width="959" height="823" alt="Screenshot 2026-04-17 153720" src="https://github.com/user-attachments/assets/234c40b6-77e8-44a5-bb0b-36074c18ac87" />

### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.

## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info
```
docker exec -it srv-postgres psql -U postgres -d info
```
### Realizar un select *from personas
```
SELECT * FROM personas;
```
# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO
<img width="724" height="205" alt="image" src="https://github.com/user-attachments/assets/6d7a9314-53f1-4534-b687-45a2ebdecc2d" />
