# ExamenParcialDS

# 🏢 softwareincidencias
**Examen Parcial - Desarrollo de Software**

Plataforma web cívica que permite a los ciudadanos reportar incidencias urbanas (baches, problemas de iluminación, fugas de agua, etc.) y a las autoridades municipales gestionar su resolución en tiempo real. 

## 🛠️ Stack Tecnológico
* **Backend:** Java 21, Spring Boot 3.x (Spring Web, Spring Data JPA).
* **Base de Datos:** PostgreSQL.
* **Frontend:** HTML5, Thymeleaf, Bootstrap 5 (CDN), Bootstrap Icons.
* **Patrones de Diseño Aplicados:** MVC, Facade (Fachada), Builder.
* **Gestión de dependencias:** Maven / Lombok.

---

## 📋 Requisitos Previos

Para ejecutar este proyecto en un entorno local, necesitas tener instalado:
1. **Java Development Kit (JDK) 21** o superior.
2. **PostgreSQL** (v12 o superior) ejecutándose en el puerto por defecto `5432`.
3. **Git** para clonar el repositorio.

---

## 🚀 Guía de Instalación y Ejecución

Sigue estos pasos para levantar la aplicación desde cero:

### 1. Clonar el repositorio
Abre tu terminal y ejecuta:
bash
git clone [https://github.com/JoaquT/ExamenParcialDS.git](https://github.com/JoaquT/ExamenParcialDS.git)
cd ExamenParcialDS

La aplicación requiere una base de datos en PostgreSQL. Abre tu terminal psql o pgAdmin y crea una base de datos vacía llamada softwareincidencias:
CREATE DATABASE softwareincidencias;

Configurar credenciales:
Ve al archivo ubicado en src/main/resources/application.properties y verifica que las credenciales coincidan con las de tu entorno local de PostgreSQL:
spring.datasource.url=jdbc:postgresql://localhost:5432/softwareincidencias
spring.datasource.username=TU_USUARIO_AQUI
spring.datasource.password=TU_CONTRASEÑA_AQUI
spring.jpa.hibernate.ddl-auto=update

Compilar y levantar el servidor:
Este proyecto incluye el Maven Wrapper, por lo que no necesitas instalar Maven globalmente. Ejecuta el siguiente comando en la raíz del proyecto:
Linux/MacOs:
./mvnw clean spring-boot:run
Windows:
mvnw.cmd clean spring-boot:run
