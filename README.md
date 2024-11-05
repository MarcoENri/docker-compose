# docker-compose
2. Tiempo de duración
 duracion 15 minutos

3. Fundamentos

Docker es una herramienta de contenedorización que permite empaquetar aplicaciones y sus dependencias en entornos virtualizados llamados contenedores. Docker Compose es una herramienta complementaria que facilita la gestión de aplicaciones multicontenedor, permitiendo definir y ejecutar múltiples servicios en un solo archivo YAML. En esta práctica, se exploró cómo crear y gestionar contenedores de bases de datos y herramientas de administración a través de Docker Compose, destacando la simplicidad y eficiencia de este método.

4. Conocimientos previos

-Conceptos básicos de contenedores y Docker.
-Familiaridad con la terminal de comandos.
-Conceptos de red y mapeo de puertos.
-Fundamentos de archivos YAML y su sintaxis.

5. Objetivos a alcanzar

-Entender la estructura y configuración de un archivo docker-compose.yml.
-Configurar servicios de base de datos y administración (como PostgreSQL y pgAdmin) en Docker.
-Ejecutar servicios en segundo plano utilizando Docker Compose.
-Mapear puertos entre el host y los contenedores para acceder a las aplicaciones.

6. Equipo necesario

-Computadora con Docker y Docker Compose instalados.
-Editor de texto para crear y modificar archivos YAML (como VS Code o nano).
-Conexión a Internet para descargar imágenes de Docker.

7. Material de apoyo

Documentación oficial de Docker.
Tutoriales y ejemplos de Docker Compose.

8. Procedimiento

Creación del Archivo docker-compose.yml:
![Imagen de WhatsApp 2024-11-04 a las 22 38 25_8a4e50da](https://github.com/user-attachments/assets/ed5c8de5-831c-48ee-9f5b-49db290796f7)

Crear un archivo llamado docker-compose.yml.
Definir los servicios db (PostgreSQL) y pgadmin en el archivo.
Especificar las configuraciones necesarias para cada servicio, incluyendo variables de entorno y mapeos de puertos.
![Imagen de WhatsApp 2024-11-04 a las 22 38 25_cfca7f6f](https://github.com/user-attachments/assets/5c284976-301d-425d-901c-4eeecd2c8b72)

Configuración del Servicio de PostgreSQL:

En el archivo YAML, configurar el contenedor PostgreSQL:
Establecer nombre de usuario, contraseña y base de datos inicial.
Configurar el volumen para persistencia de datos.

Configuración de pgAdmin:

Configurar el servicio de pgAdmin en el archivo YAML:
Definir credenciales de acceso para pgAdmin.
Mapear el puerto 8080 del host al puerto 80 del contenedor.

![Imagen de WhatsApp 2024-11-04 a las 22 40 17_887b888c](https://github.com/user-attachments/assets/1104faf1-16f7-45ba-9319-18939fbdafe3)

En la terminal, ejecutar docker-compose up -d para iniciar los contenedores en segundo plano.
Verificar el estado de los contenedores con docker ps.

Prueba de Conexión a pgAdmin:

Acceder a http://localhost:8080 en el navegador.
Iniciar sesión en pgAdmin usando las credenciales configuradas.
Añadir una conexión al servidor PostgreSQL configurado, verificando la conectividad.
 
![Imagen de WhatsApp 2024-11-04 a las 22 38 44_f671ed11](https://github.com/user-attachments/assets/4c2d3a5a-36f7-482f-843f-0259274a1f4b)
![image](https://github.com/user-attachments/assets/f8ad499c-8921-4f5e-9140-5be0a16a70c4)

Detener y limpiar los contenedores usando docker-compose down.

9. Resultados esperados

Creación exitosa de los contenedores db y pgadmin, en ejecución y accesibles desde el host.
Acceso a pgAdmin a través del navegador (http://localhost:8080) y conexión exitosa a la base de datos PostgreSQL.

10. Bibliografía
-Docker, Inc. (2024). [Documentación de Docker Compose.](https://docs.docker.com/compose/)
-PostgreSQL Global Development Group. (2024). [Documentación de PostgreSQL.](https://www.postgresql.org/docs/)
-pgAdmin Development Team. (2024). [Documentación de pgAdmin.](https://www.pgadmin.org/docs/)
