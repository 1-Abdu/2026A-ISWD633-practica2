# Variables de Entorno
### ¿Qué son las variables de entorno?
Las variables de entorno son como "notas adhesivas" digitales que el sistema operativo guarda en su memoria para que cualquier programa pueda consultarlas rápidamente. Son como configuraciones globales (como la ubicación de una carpeta o una clave secreta) que no se escriben directamente dentro del código de una aplicación, sino que se definen fuera de ella. Esto permite que el software sepa cómo comportarse o dónde encontrar recursos sin importar en qué computadora se esté ejecutando, facilitando enormemente la configuración de sistemas y contenedores.
# COMPLETAR

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.
```
 docker run -d --name varEnt -e username=admin_user -e role=admin nginx:alpine
```
# COMPLETAR

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
<img width="950" height="324" alt="image" src="https://github.com/user-attachments/assets/fc7e2498-05ba-4038-a7c3-cb07f8d3d096" />

### Crear un contenedor con la imagen de mysql, mapear todos los puertos
# COMPLETAR

### ¿El contenedor se está ejecutando?
No
# COMPLETAR

### Identificar el problema
Se tiene que asignar una de las variables de entorno
# COMPLETAR

### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR
<img width="1033" height="623" alt="image" src="https://github.com/user-attachments/assets/0c91c304-a5c2-46f2-849b-5b614cdc1680" />
