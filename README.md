 # Mascotas CDMX
Proyecto Escolar
Sistema web para la gestión de adopción de mascotas en la Ciudad de México. Esta aplicación permite conectar a personas interesadas en adoptar con refugios, facilitando el proceso de solicitud y seguimiento.

## 🚀 Características

*   **Catálogo de Mascotas:** Visualización de perros y gatos disponibles para adopción con detalles como raza, edad, salud y fotografías.
*   **Gestión de Usuarios:** Sistema de registro e inicio de sesión para adoptantes y administradores.
*   **Panel de Administración:**
    *   Alta, baja y modificación de mascotas.
    *   Carga de imágenes de mascotas.
    *   Gestión de solicitudes de adopción.
*   **Proceso de Adopción:** Formulario socioeconómico integrado para evaluar la idoneidad de los adoptantes.

## 🛠️ Tecnologías

*   **Backend:** Java (Jakarta EE), JDBC.
*   **Frontend:** JSF (JavaServer Faces), PrimeFaces, Bootstrap.
*   **Base de Datos:** SQL (MySQL/MariaDB).

## ⚙️ Configuración e Instalación

### Prerrequisitos
*   JDK 8 o superior.
*   Servidor de aplicaciones (Apache Tomcat, GlassFish, WildFly).
*   Servidor de base de datos SQL.

### Pasos Críticos

1.  **Base de Datos:**
    *   Asegúrese de importar el esquema de base de datos correspondiente.
    *   Verifique la configuración de conexión en la clase `dao.Administrador`.

2.  **Configuración de Rutas (Importante):**
    *   El proyecto requiere configurar la ruta de almacenamiento de imágenes manualmente.
    *   Edite el archivo: `src/main/java/controlador/AdministradorControlador1.java`.
    *   Localice la línea dentro del método `guardarMascota`:
        ```java
        String rutaCarpeta = "C:\\Users\\Ozzy\\Desktop\\programacionweb\\mascotas.zip_expanded\\mascotas\\src\\main\\webapp\\imagenes";
        ```
    *   Cambie esta ruta por la ubicación absoluta de la carpeta `imagenes` en su entorno local.

3.  **Ejecución:**
    *   Despliegue el artefacto (`.war`) en su servidor.
    *   Navegue a la página de inicio (ej. `http://localhost:8080/mascotas/index.xhtml`).

## 📂 Estructura

*   `controlador`: Managed Beans de JSF para la lógica de presentación.
*   `dao`: Objetos de Acceso a Datos para la comunicación con la BD.
*   `modelo`: Clases POJO que representan las entidades (Usuario, Mascota, Solicitud).
*   `webapp`: Archivos XHTML, CSS y recursos estáticos.
