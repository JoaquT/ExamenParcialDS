# 🏢 softwareincidencias
**Examen Parcial - Desarrollo de Software**

Plataforma web cívica que permite a los ciudadanos reportar incidencias urbanas (baches, problemas de iluminación, fugas de agua, etc.) y a las autoridades municipales gestionar su resolución en tiempo real. 

## 🛠️ Stack Tecnológico
* Backend: Java 21, Spring Boot 3.x (Spring Web, Spring Data JPA).
* Base de Datos: PostgreSQL.
* Frontend: HTML5, Thymeleaf, Bootstrap 5 (CDN), Bootstrap Icons.
* Patrones de Diseño Aplicados: MVC, Facade (Fachada), Builder.
* Gestión de dependencias: Maven / Lombok.

---

##  Requisitos Previos

Para ejecutar este proyecto en un entorno local, se necesita tener instalado:
1. Java Development Kit (JDK) 21 o superior.
2. PostgreSQL (v12 o superior) ejecutándose en el puerto por defecto 5432.
3. Git para clonar el repositorio.

---

## Guía de Instalación y Ejecución

Para poder levantar la aplicacion se debe seguir estos pasos:

1. CLONAR EL REPOSITORIO: Abrir la terminal y ejecutar los siguientes comandos:
   git clone [https://github.com/JoaquT/ExamenParcialDS.git](https://github.com/JoaquT/ExamenParcialDS.git)
   cd ExamenParcialDS

2. CONFIGURAR LA BASE DE DATOS: La aplicación requiere una base de datos en PostgreSQL. Abrir la terminal de psql o pgAdmin y crea una base de datos vacía llamada "softwareincidencias" ejecutando:
   CREATE DATABASE softwareincidencias;

3. CONFIGURAR CREDENCIALES: Ve al archivo ubicado en "src/main/resources/application.properties" y verifica que las credenciales coincidan con las de tu entorno local de PostgreSQL:
   spring.datasource.url=jdbc:postgresql://localhost:5432/softwareincidencias
   spring.datasource.username=TU_USUARIO_AQUI
   spring.datasource.password=TU_CONTRASEÑA_AQUI
   spring.jpa.hibernate.ddl-auto=update

4. COMPILAR Y LEVANTAR EL SERVIDOR: Este proyecto incluye el Maven Wrapper, por lo que no necesitas tener Maven instalado globalmente en tu sistema. Ejecuta el comando correspondiente en la raíz del proyecto según tu sistema operativo:
   
   En Linux / macOS:
   ./mvnw clean spring-boot:run
   
   En Windows:
   mvnw.cmd clean spring-boot:run

---

## 🎮 Uso de la Aplicación

1. Una vez que la terminal indique que la aplicación ha iniciado (usualmente en el puerto 8080), abre tu navegador y entra a: http://localhost:8080
2. La aplicación está protegida por un sistema de sesión. Serás redirigido al Login.
3. Haz clic en "Regístrate ahora" para crear un usuario de prueba.
4. Flujo de Roles:
   * Ciudadano: Si te registras como ciudadano, podrás ver el panel de incidencias globales y tendrás acceso al botón para registrar un nuevo reporte.
   * Supervisor Municipal: Si te registras como supervisor, tu interfaz incluirá controles avanzados para Actualizar el Estado de los reportes (Revisado, En Proceso, Resuelto) y un botón para Eliminar incidencias.

(Nota: La aplicación está configurada mediante un CommandLineRunner para insertar automáticamente las categorías por defecto en la base de datos al iniciar por primera vez).

---
