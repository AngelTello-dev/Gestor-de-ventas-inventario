# Gestor-de-ventas-inventario
Aplicación web para la gestión de ventas desarrollada en Java (JSP + JSTL) con conexión a base de datos MySQL. Permite registrar, consultar, editar y generar reportes en PDF de ventas de productos.

Características principales
Módulo de autenticación (login seguro)
Registro de ventas (producto, precio, cantidad)
Tabla interactiva con funciones CRUD (editar/eliminar)
Reportes en PDF integrados con JasperReports
Diseño responsivo (Bootstrap 5 + Font Awesome)
Validación de formularios en frontend y backend

Tecnologías utilizadas:
Categoría	                             Tecnologías
Frontend	           HTML5, CSS3, Bootstrap 5, JavaScript, Font Awesome
Backend	             Java (JSP), JSTL (Core, SQL), Servlets (opcional)
Base de datos	MySQL                      (JDBC)
Generación de PDF	               JasperReports / iReport
Servidor	                           GlassFish Server

Estructura del proyecto:

Captura del proyecto
![image](https://github.com/user-attachments/assets/81b7837c-3268-4d0d-9bdc-e7ed4865f44f)

Base de datos tablas correspondientes al proyecto:

usuarios donde se almacela el login
![image](https://github.com/user-attachments/assets/f90aa4d5-52fa-4b42-9c81-af92974f42c2)

las ventas donde se alojara el invetario-ventas
![image](https://github.com/user-attachments/assets/f3afdada-8012-4783-80e6-799625c4f36d)

Todo dentro de la base de datos bdxml2 (ustedes pueden cambiar el nombre de la base de dataos a tu gusto)

EN CASO DE LAS LIBREIRAS ES NECESARIO TENER LO SIGUENTE:
Dentro de la carpeta del proyecto te encontraras un archivo de java, no es nesesario tenerlo dentro del proyecto ya que al importarlo se guarda dentro del proyecto.
![image](https://github.com/user-attachments/assets/f6bf2132-0f38-4d89-9d8d-40baad8b162e)
y como ejemplo de como importarlo:
![image](https://github.com/user-attachments/assets/494079a3-b7a2-44d3-80f5-ad13be2004a9)

![image](https://github.com/user-attachments/assets/4ad8fa40-08ac-411e-96d1-e5a3b6642a56)

y asi es como se importar las librerias correspondientes.
Tambien otro punto como tiene jstl para java es nesesario importarlo de la siguiente manera:

![image](https://github.com/user-attachments/assets/6615c2f2-26a2-401d-b52f-e445b3cc358d)

![image](https://github.com/user-attachments/assets/a065fabc-3872-452d-b33b-3c93d4bd6915)

y cuando lo agregas a la libreria verifica de que ya este importado


Configuración inicial
Requisitos
Java JDK 8+
GlassFish Server 5.1.0
MySQL 5.7+
Librerías:
JSTL 1.2
MySQL Connector/J
JasperReports

Instalación
Clonar repositorio o copiar archivos a webapps de Tomcat.

Crear la base de datos con el script SQL proporcionado.

Configurar credenciales de MySQL en:

java
<sql:setDataSource 
    url="jdbc:mysql://localhost:3306/bdxml2"
    user="usuario" 
    password="clave"/>
Iniciar Tomcat y acceder a:
http://localhost:8080/NombreProyecto

 Script SQL de ejemplo
 
 CREATE TABLE ventas (
    id INT AUTO_INCREMENT PRIMARY KEY,
    id_producto VARCHAR(20) NOT NULL,
    producto VARCHAR(100) NOT NULL,
    precio DECIMAL(10,2) NOT NULL,
    cantidad INT NOT NULL,
    fecha DATETIME NOT NULL
);

Cómo usar
Login: Ingresar con usuario/contraseña.
Registrar venta:
Rellenar formulario en ventas.jsp.
Consultar/editar:
Acceder a consultas.jsp.
Usar botones (editar) o (eliminar).
Generar PDF:
Navegar a reportes.jsp.
Hacer clic en "Generar reporte".

Contacto
Tello Montes De Oca Angel Antonio - angel_tello_90@hotmail.com 
