# Spring Proyectos Errores

Este repositorio contiene una colección de proyectos Spring Boot enfocados en el manejo y tratamiento de errores, excepciones y respuestas de error en aplicaciones web. Los proyectos demuestran mejores prácticas para la gestión de excepciones, validación de datos y respuestas HTTP apropriadas.

**Autor:** Juan Daniel Muñoz Queupul

---

## 📋 Proyectos Incluidos

### 1. springboot-error

#### Descripción
Proyecto educativo que implementa un sistema completo de manejo de errores en Spring Boot. Demuestra cómo capturar, procesar y responder a excepciones de manera elegante y estructurada. Incluye modelos de dominio, servicios, controladores y un manejador centralizado de excepciones.

#### Características
- ✅ Manejo centralizado de excepciones mediante `@ControllerAdvice`
- ✅ Excepciones personalizadas (`UserNotFoundException`)
- ✅ Modelo de respuesta de errores estructurado
- ✅ Servicio de usuarios con validaciones
- ✅ Configuración de propiedades para manejo de rutas no encontradas
- ✅ Roles y entidades de dominio

#### Estructura del Proyecto
```
springboot-error/
├── src/
│   ├── main/
│   │   ├── java/com/andres/curso/springboot/error/springbooterror/
│   │   │   ├── SpringbootErrorApplication.java (Clase principal)
│   │   │   ├── AppConfig.java (Configuración)
│   │   │   ├── controllers/
│   │   │   │   ├── AppController.java
│   │   │   │   └── HandlerExceptionController.java
│   │   │   ├── exceptions/
│   │   │   │   └── UserNotFoundException.java
│   │   │   ├── models/
│   │   │   │   ├── domain/
│   │   │   │   │   ├── User.java
│   │   │   │   │   └── Role.java
│   │   │   │   └── Error.java
│   │   │   └── services/
│   │   │       ├── UserService.java (Interfaz)
│   │   │       └── UserServiceImpl.java (Implementación)
│   │   └── resources/
│   │       └── application.properties
│   └── test/
├── pom.xml
├── mvnw / mvnw.cmd
└── target/
```

#### Stack Tecnológico
- **Lenguaje:** Java 17
- **Framework:** Spring Boot 3.1.2
- **Build Tool:** Maven
- **Dependencias Clave:**
  - `spring-boot-starter-web` - Para crear aplicaciones web
  - `spring-boot-starter-actuator` - Monitoreo y endpoints actuales
  - `spring-boot-devtools` - Herramientas de desarrollo
  - `spring-boot-starter-test` - Framework de testing

#### Configuración Principal
```properties
spring.mvc.throw-exception-if-no-handler-found=true
spring.web.resources.add-mappings=false
```

#### Cómo Ejecutar
```bash
# Navegar al directorio del proyecto
cd springboot-error

# Ejecutar con Maven
./mvnw spring-boot:run

# O compilar y ejecutar
./mvnw clean install
java -jar target/springboot-error-0.0.1-SNAPSHOT.jar
```

---

### 2. springboot-error 2

#### Descripción
Segunda versión del proyecto de manejo de errores. Mantiene la misma estructura y funcionalidad que el proyecto anterior, ofreciendo un ejemplo adicional o versión mejorada del sistema de gestión de excepciones en Spring Boot.

#### Características
- ✅ Manejo centralizado de excepciones
- ✅ Modelos de error personalizados
- ✅ Controladores con validación de datos
- ✅ Servicio de usuarios implementado
- ✅ Configuración y propiedades optimizadas
- ✅ Estructura de controladores con manejadores de excepciones

#### Estructura del Proyecto
```
springboot-error 2/
├── src/
│   ├── main/
│   │   ├── java/com/andres/curso/springboot/error/springbooterror/
│   │   │   ├── SpringbootErrorApplication.java (Clase principal)
│   │   │   ├── controllers/
│   │   │   │   ├── AppController.java
│   │   │   │   └── HandlerExceptionController.java
│   │   │   ├── models/
│   │   │   │   └── Error.java
│   │   │   └── services/
│   │   └── resources/
│   │       └── application.properties
│   └── test/
├── pom.xml
├── mvnw / mvnw.cmd
└── target/
```

#### Stack Tecnológico
- **Lenguaje:** Java 17
- **Framework:** Spring Boot 3.1.2
- **Build Tool:** Maven
- **Dependencias Clave:**
  - `spring-boot-starter-web` - Para aplicaciones REST
  - `spring-boot-starter-actuator` - Health checks y monitoreo
  - `spring-boot-devtools` - Recarga automática en desarrollo
  - `spring-boot-starter-test` - Testing y JUnit

#### Cómo Ejecutar
```bash
# Navegar al directorio del proyecto
cd "springboot-error 2"

# Ejecutar con Maven
./mvnw spring-boot:run

# O compilar y ejecutar
./mvnw clean install
java -jar target/springboot-error-0.0.1-SNAPSHOT.jar
```

---

## 🔧 Stack Tecnológico General

| Componente | Versión | Descripción |
|-----------|---------|------------|
| Java | 17 | Lenguaje de programación principal |
| Spring Boot | 3.1.2 | Framework web y IoC |
| Maven | 3.x | Gestor de dependencias y build |
| Spring Web | 3.1.2 | Módulo para aplicaciones web REST |
| Spring Actuator | 3.1.2 | Monitoreo y endpoints de actuación |
| JUnit | 5.x | Framework de testing |

---

## 📝 Conceptos Clave Implementados

### Manejo de Excepciones
- **ControllerAdvice:** Manejador centralizado de excepciones
- **ExceptionHandler:** Métodos para capturar excepciones específicas
- **ResponseEntity:** Respuestas HTTP personalizadas

### Modelos
- **Domain:** Entidades del negocio (User, Role)
- **Error:** Modelo de respuesta para errores
- **Excepciones Personalizadas:** UserNotFoundException

### Capas
- **Controllers:** Endpoints REST
- **Services:** Lógica de negocio
- **Models:** Estructuras de datos
- **Exceptions:** Excepciones personalizadas

---

## 🚀 Casos de Uso

Estos proyectos son ideales para:
- 📚 Aprender manejo de errores en Spring Boot
- 🔍 Entender capas de aplicación (controllers, services, models)
- 🛡️ Implementar excepciones personalizadas
- 📊 Respuestas HTTP apropiadas según el error
- 🧪 Testing de excepciones y comportamientos

---

## 📦 Dependencias Comunes

Ambos proyectos comparten las mismas dependencias principales:

```xml
<!-- Spring Boot Web -->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>

<!-- Spring Boot Actuator -->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-actuator</artifactId>
</dependency>

<!-- Spring Boot DevTools -->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <scope>runtime</scope>
    <optional>true</optional>
</dependency>

<!-- Spring Boot Test -->
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-test</artifactId>
    <scope>test</scope>
</dependency>
```

---

## 🔍 Endpoints Típicos

### AppController
- `GET /` - Endpoint de prueba
- `GET /users/{id}` - Obtener usuario (puede lanzar `UserNotFoundException`)

### HandlerExceptionController
- Manejo de excepciones globales
- Respuestas formateadas para errores

---

## 📚 Recursos Adicionales

- [Documentación Spring Boot](https://spring.io/projects/spring-boot)
- [Spring Boot Error Handling](https://spring.io/blog/2013/11/01/exception-handling-in-spring-mvc)
- [Java 17 Features](https://www.oracle.com/java/technologies/javase/17-relnotes.html)

---

## ✨ Notas de Desarrollo

- Ambos proyectos utilizan **Java 17** como versión mínima
- La configuración de propiedades en `application.properties` es crítica para el manejo de errores
- Los proyectos están optimizados para desarrollo con Spring Boot DevTools
- Se incluyen herramientas Maven wrapper (`mvnw`) para facilitar la compilación

---

## 📞 Información del Autor

**Juan Daniel Muñoz Queupul**

---

*Última actualización: Febrero de 2026*
