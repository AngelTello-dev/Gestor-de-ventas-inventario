# Gestor de Ventas e Inventario

Aplicación web desarrollada en **Java (JSP + JSTL)** con conexión a base de datos **MySQL** para la gestión de ventas. Permite registrar, consultar, editar y generar reportes en PDF de ventas de productos.

## Características principales

- Módulo de autenticación (login seguro)
- Registro de ventas (producto, precio, cantidad)
- Tabla interactiva con funciones CRUD (editar/eliminar)
- Generación de reportes en PDF (JasperReports)
- Diseño responsivo con Bootstrap 5 + Font Awesome
- Validación de formularios en frontend y backend

## Tecnologías utilizadas

| Categoría         | Tecnologías                                              |
|-------------------|----------------------------------------------------------|
| **Frontend**       | HTML5, CSS3, Bootstrap 5, JavaScript, Font Awesome      |
| **Backend**        | Java (JSP), JSTL (Core, SQL), Servlets (opcional)       |
| **Base de datos**  | MySQL (JDBC)                                             |
| **PDF Reports**    | JasperReports / iReport                                 |
| **Servidor**       | GlassFish Server                                         |

## Estructura del Proyecto

### Captura del proyecto
![Proyecto](https://github.com/user-attachments/assets/81b7837c-3268-4d0d-9bdc-e7ed4865f44f)

### Base de datos

#### Tabla `usuarios` (login de usuario)
![Usuarios](https://github.com/user-attachments/assets/f90aa4d5-52fa-4b42-9c81-af92974f42c2)

#### Tabla `ventas` (registro de inventario/ventas)
![Ventas](https://github.com/user-attachments/assets/f3afdada-8012-4783-80e6-799625c4f36d)

La base de datos se llama `bdxml2`, pero puedes renombrarla a tu gusto.

## Librerías necesarias

- Dentro del proyecto encontrarás un archivo `.jar`. Este se importa automáticamente, pero puedes hacerlo manualmente si es necesario:

![Importar JAR](https://github.com/user-attachments/assets/f6bf2132-0f38-4d89-9d8d-40baad8b162e)
![Ejemplo de importación](https://github.com/user-attachments/assets/494079a3-b7a2-44d3-80f5-ad13be2004a9)

### JSTL
Es necesario importar las librerías JSTL de forma manual en tu servidor:

![Importar JSTL](https://github.com/user-attachments/assets/6615c2f2-26a2-401d-b52f-e445b3cc358d)
![JSTL cargada](https://github.com/user-attachments/assets/a065fabc-3872-452d-b33b-3c93d4bd6915)

## Configuración inicial

### Requisitos

- Java JDK 8+
- GlassFish Server 5.1.0
- MySQL 5.7+
- Librerías:
  - JSTL 1.2
  - MySQL Connector/J
  - JasperReports

### Instalación

1. Clona el repositorio o copia los archivos en la carpeta `webapps` de tu servidor.
2. Crea la base de datos con el siguiente script SQL:

```sql
CREATE TABLE ventas (
    id INT AUTO_INCREMENT PRIMARY KEY,
    id_producto VARCHAR(20) NOT NULL,
    producto VARCHAR(100) NOT NULL,
    precio DECIMAL(10,2) NOT NULL,
    cantidad INT NOT NULL,
    fecha DATETIME NOT NULL
);

Tello Montes De Oca Angel Antonio - angel_tello_90@hotmail.com 

