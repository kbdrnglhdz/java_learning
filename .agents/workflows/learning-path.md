---
description: Ruta de aprendizaje progresiva de Java Fundamentos hasta Spring Boot
---

# Ruta de Aprendizaje: Java → Spring Boot

Este workflow organiza el recorrido de aprendizaje en tres grandes módulos con tareas específicas.
El agente **no desbloqueará el siguiente módulo** hasta que el Evaluador de Progreso confirme
que el estudiante domina el módulo actual.

> 📌 **Para comenzar**: escribe _"Inicia la ruta de aprendizaje"_ o _"Comienza el módulo 1"_.

---

## Módulo 1 — Fundamentos de Java (`java_basics`)

> **Prerequisito**: Ninguno. Punto de entrada del flujo.

### Tarea 1 — Configuración del entorno y Hola Mundo

**Conceptos clave**: clase, método `main`, `System.out.println`, compilación y ejecución.

**Contenido**:
- Instalar JDK (versión LTS recomendada: 21).
- Configurar variable de entorno `JAVA_HOME`.
- Crear y ejecutar el primer programa `HolaMundo.java`.
- Explicar la estructura básica de una clase Java: `public class`, `main`, `System.out.println`.

🎯 **Reto autónomo**: Modificar el programa `HolaMundo.java` para que imprima tu nombre, tu ciudad y el año actual en líneas separadas, usando concatenación de `String`.

---

### Tarea 2 — Variables y Tipos de Datos

**Conceptos clave**: variable, tipo primitivo, tipo referencia, declaración, asignación, `String`.

**Contenido**:
- Qué es una variable (analogía: una caja con etiqueta y contenido).
- Tipos primitivos: `int`, `double`, `boolean`, `char`.
- Tipo referencia: `String`.
- Convención `camelCase` para nombres de variables.
- Diferencia entre declarar y asignar.

🎯 **Reto autónomo**: Declarar variables para almacenar: nombre (texto), edad (número entero), altura (número decimal) y si es estudiante (verdadero/falso). Imprimirlas en un mensaje descriptivo con una oración coherente.

---

### Tarea 3 — Estructuras de Control

**Conceptos clave**: condicionales, bucles, `break`, `continue`, flujo de ejecución.

**Contenido**:
- `if / else if / else` — toma de decisiones (analogía: un semáforo).
- Bucle `for` — repetición con contador conocido.
- Bucle `while` — repetición con condición.
- `break` para salir del bucle y `continue` para saltar una iteración.

🎯 **Reto autónomo**: Crear un programa que imprima los números del 1 al 20, indicando si cada uno es **par** o **impar**. Los múltiplos de 10 deben imprimirse con el mensaje `"¡Número redondo!"`.

---

## Módulo 2 — Programación Orientada a Objetos (`java_poo`)

> **Prerequisito**: Completar y aprobar **todos los retos** del Módulo 1.
> 🔒 El evaluador debe confirmar el avance antes de comenzar.

### Tarea 4 — Clases y Objetos

**Conceptos clave**: clase, objeto, atributo, método, constructor, `this`, `new`.

**Contenido**:
- Qué es POO y por qué existe (analogía: molde/plano vs. objeto real).
- Crear una clase con atributos (campos) y métodos.
- Constructores: qué son y para qué sirven.
- La palabra clave `this` para referenciar la instancia actual.
- Instanciar objetos con `new`.

🎯 **Reto autónomo**: Crear la clase `Producto` con los campos `nombre` (String), `precio` (double) y `stock` (int). Añadir un constructor que reciba los tres valores y un método `mostrarInfo()` que los imprima. Instanciar 3 productos distintos desde el `main`.

---

### Tarea 5 — Herencia y Polimorfismo

**Conceptos clave**: herencia, `extends`, sobreescritura de métodos, `@Override`, polimorfismo, referencia de tipo padre.

**Contenido**:
- `extends` — relación "es un" (analogía: perro es un animal).
- Sobreescritura de métodos con `@Override`.
- Por qué `@Override` es buena práctica aunque no es obligatorio.
- Polimorfismo: usar una referencia del tipo padre para apuntar a un objeto hijo.

🎯 **Reto autónomo**: Crear la clase `Vehiculo` con un método `describir()`. Crear las subclases `Coche` y `Moto` que extiendan `Vehiculo` y sobreescriban `describir()` con una descripción propia. Desde el `main`, instanciar ambos como tipo `Vehiculo` y llamar a `describir()`.

---

### Tarea 6 — Interfaces y Abstracción

**Conceptos clave**: clase abstracta, interfaz, `implements`, contrato, abstracción.

**Contenido**:
- Qué problema resuelve la abstracción.
- Diferencia entre clase abstracta e interfaz.
- Implementar una interfaz con `implements`.
- Cuándo usar cada enfoque (guía práctica básica).

🎯 **Reto autónomo**: Definir la interfaz `Figura` con el método `calcularArea()` (que devuelve `double`). Implementarla en las clases `Circulo` (radio) y `Rectangulo` (base y altura). Crear ambas figuras en el `main` e imprimir sus áreas.

---

## Módulo 3 — Introducción a Spring Boot (`spring_intro`)

> **Prerequisito**: Completar y aprobar **todos los retos** del Módulo 2.
> ⛔ **Barrera inamovible**: el evaluador debe confirmar el dominio completo de POO antes de continuar.
> El agente rechazará cualquier intento de acceder a este módulo antes de cumplir el prerequisito.

### Tarea 7 — Inyección de Dependencias e IoC

**Conceptos clave**: acoplamiento, IoC (Inversión de Control), DI (Inyección de Dependencias), contenedor de Spring.

**Contenido**:
- El problema del acoplamiento fuerte: ¿por qué es un problema?
- Analogía: ensambladora de autos (IoC) vs. taller artesanal (acoplamiento fuerte).
- Diferencia entre acoplamiento fuerte y débil.
- Cómo Spring actúa como el "ensamblador".

---

### Tarea 8 — Creación del Proyecto con Spring Initializr

**Conceptos clave**: Spring Initializr, estructura de un proyecto Spring Boot, `pom.xml`, dependencias.

**Contenido**:
- Visitar [start.spring.io](https://start.spring.io).
- Seleccionar dependencias: **Spring Web**, **Lombok**.
- Importar el proyecto en el IDE y explorar su estructura.
- Entender el rol de `pom.xml` o `build.gradle`.

---

### Tarea 9 — Primer Controlador REST

**Conceptos clave**: `@RestController`, `@GetMapping`, endpoint, request, response, JSON.

**Contenido**:
- Anotaciones básicas: `@RestController`, `@GetMapping`.
- Crear un endpoint `/hola` que devuelva un mensaje en texto plano.
- Probar con Postman o el navegador.

🎯 **Reto autónomo**: Añadir un endpoint `/saludo/{nombre}` que devuelva un saludo personalizado en formato `"¡Hola, {nombre}! Bienvenido a Spring Boot."`. Probarlo con al menos 3 nombres distintos.

---

## Reglas Generales del Flujo

| Regla | Descripción |
|-------|-------------|
| **Explicación antes que código** | Cada tarea inicia con una explicación conceptual + analogía. |
| **Código incremental** | El agente escribe el código por partes; el estudiante debe explicarlo o modificarlo. |
| **Validación obligatoria** | Cada tarea concluye con un reto autónomo evaluado por la skill `evaluator`. |
| **Avance bloqueado** | No se puede pasar al siguiente módulo sin aprobación del evaluador. |
| **Estilo de código** | `PascalCase` para clases, `camelCase` para métodos y variables, comentarios educativos obligatorios. |
