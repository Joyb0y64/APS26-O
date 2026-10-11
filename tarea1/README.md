# Tarea 1: Fundamentos de Administración de Proyectos y Licenciamiento

**UEA:** Administración de Proyectos de Software  
**Clave UEA:** 1151055  
**Trimestre:** 26-O  
**Licenciatura:** Ingeniería en Computación  
**Nombre:** Erick Araujo Galán  
**Matrícula:** 2192006136  
**Profesor:** Gabriel Hurtado Avilés  
**Fecha:** 10 de Octubre de 2026  

---

## 1. ¿Qué es un proyecto de software?

### Proyecto frente a operación continua
Un **proyecto de software** es un esfuerzo temporal emprendido para crear un producto, servicio o resultado único, delimitado por un inicio y un fin definidos (Project Management Institute [PMI], 2021). En contraste, una **operación continua** abarca las actividades funcionales y repetitivas de una organización enfocadas en mantener la continuidad del negocio y el mantenimiento diario de los sistemas existentes (Pressman y Maxim, 2021). Mientras que el proyecto busca la transformación o innovación con fecha de caducidad, la operación persigue la estabilidad permanente.

### Proyecto, producto y proceso
En la ingeniería de software, estos tres conceptos guardan una relación jerárquica y complementaria:
* **Proyecto:** El vehículo organizacional y temporal que gestiona los recursos, el presupuesto y los plazos para cumplir con un objetivo.
* **Producto:** El artefacto ejecutable final, el sistema o la solución de software que se entrega a los usuarios finales.
* **Proceso:** El conjunto estructurado de actividades, métodos, prácticas y herramientas empleadas por el equipo para construir el producto a lo largo del ciclo de vida del proyecto (Pressman y Maxim, 2021).

### Alcance, tiempo, costo y calidad
Estos cuatro elementos conforman la restricción cuádruple clásica de la gestión de proyectos:
1. **Alcance:** Define el límite del trabajo necesario para entregar el software con las funciones especificadas.
2. **Tiempo:** La programación temporal o cronograma establecido para completar las fases y entregables.
3. **Costo:** El presupuesto financiero y los recursos asignados para la ejecución.
4. **Calidad:** El grado en que el software satisface los requisitos implícitos y explícitos, garantizando confiabilidad y usabilidad (PMI, 2021).

Cualquier cambio en una de las tres restricciones principales (alcance, tiempo o costo) altera inevitablemente la calidad final del software entregado.

---

## 2. ¿Cómo se administra?

### PMBOK y Scrum
La **Guía del PMBOK** (Project Management Body of Knowledge) es un marco holístico estándar desarrollado por el PMI que ofrece principios, dominios de desempeño y buenas prácticas aplicables a cualquier tipo de proyecto (PMI, 2021). Por otro lado, **Scrum** es un marco de trabajo ligero y ágil diseñado específicamente para la gestión evolutiva de productos complejos mediante ciclos de desarrollo cortos e iterativos denominados *Sprints* (Schwaber y Sutherland, 2020).

### Modelos de desarrollo: Predictivo, Iterativo y Ágil
* **Predictivo (Cascada / Waterfall):** Plantea un plan secuencial rígido donde los requisitos, el alcance, el costo y el tiempo se definen por completo al inicio. No acepta cambios fácilmente en fases avanzadas (PMI, 2021).
* **Iterativo:** Modifica y mejora progresivamente el producto mediante entregas sucesivas de prototipos o versiones funcionales, permitiendo aprender de la retroalimentación en cada ciclo.
* **Ágil:** Combina el enfoque iterativo e incremental para responder de forma rápida ante el cambio. En lugar de seguir un plan estricto, prioriza el software funcionando, la colaboración continua y la adaptación (Schwaber y Sutherland, 2020).

### Elección para el proyecto del curso
Para un proyecto escolar como el de este curso, la elección idónea es un **modelo ágil (Scrum/Kanban)**. La naturaleza del trimestre académico exige flexibilidad frente a ajustes de requisitos, entregas periódicas de tareas en lapsos de tiempo cortos y la capacidad de adaptar las prioridades de desarrollo conforme avanza la retroalimentación del profesor sin la rigidez de un plan predictivo inicial (PMI, 2021; Schwaber y Sutherland, 2020).

---

## 3. ¿Con qué herramientas?

### Herramientas de la ingeniería de software moderna
* **Control de versiones:** Herramientas como Git que registran los cambios realizados en el código fuente a lo largo del tiempo, facilitando el trabajo colaborativo, la auditoría de revisiones y la reversión de errores (Chacon y Straub, 2014).
* **Tableros de trabajo:** Herramientas visuales (e.g., Trello, GitHub Projects) basadas en metodologías Kanban para rastrear el estado de las tareas (*Por hacer*, *En proceso*, *Hecho*) y transparentar el flujo de trabajo (Schwaber y Sutherland, 2020).
* **Contenedores:** Entornos aislados y ligeros que empaquetan una aplicación junto con sus dependencias y librerías, garantizando que el código se ejecute de forma idéntica en cualquier equipo (Merkel, 2014).
* **Integración continua (CI):** Práctica de automatizar la compilación, pruebas y verificación de cada cambio subido al repositorio para detectar fallos tempranamente.

### Herramientas específicas del curso

#### Docker frente a una Máquina Virtual (VM)
Una máquina virtual emula un hardware completo y requiere ejecutar un sistema operativo invitado (*Guest OS*) sobre un hipervisor, lo que consume elevados recursos. En cambio, **Docker** comparte el núcleo (*kernel*) del sistema operativo anfitrión y aísla los procesos mediante contenedores, ofreciendo un arranque inmediato y un consumo reducido de memoria (Merkel, 2014).

#### Dockerfile frente a `compose.yaml`
* **Dockerfile:** Archivo de texto con las instrucciones paso a paso para construir una **imagen individual** de Docker.
* **compose.yaml:** Archivo de configuración usado por *Docker Compose* para definir y orquestar servicios **multicontenedor** (redes, volúmenes, puertos y múltiples aplicaciones vinculadas) (Merkel, 2014).

#### Volumen en Docker
Mecanismo de almacenamiento persistente independiente del ciclo de vida de los contenedores. Evita que la información o los datos generados por una base de datos o aplicación se borren al detener o eliminar el contenedor.

#### Comandos fundamentales de Docker
* `docker compose up -d`: Inicia los contenedores definidos en `compose.yaml` en segundo plano (*detached mode*).
* `docker exec`: Ejecuta un comando internamente dentro de un contenedor en ejecución (ej. `docker exec -it mi_contenedor bash`).
* `docker stop`: Detiene de manera ordenada uno o más contenedores activos sin borrarlos.
* `docker compose down`: Detiene y elimina por completo los contenedores, redes y recursos creados por el archivo de Compose.
* `docker ps`: Lista los contenedores que se encuentran actualmente en ejecución en el sistema.
* `docker logs`: Muestra las salidas de consola y registros de depuración (*stdout/stderr*) emitidos por un contenedor.

---

## 4. ¿Bajo qué licencia se distribuye el software?

### a) Tipos de licencias: Permisivas vs. Copyleft

Las licencias de software libre y código abierto se dividen principalmente en dos grandes familias (Rosen, 2004; St. Laurent, 2004):

* **Licencias Permisivas:** Ofrecen libertad casi ilimitada para usar, modificar, redistribuir y vender el software, incluso integrándolo dentro de programas propietarios cerrados. Solo exigen conservar el aviso de derechos de autor original.
* **Licencias Copyleft (Recíprocas):** Exigen que cualquier obra derivada o modificación del software que se distribuya sea liberada obligatoriamente bajo la misma licencia abierta original, impidiendo que el código se privatice.

| Licencia | Tipo | Lo que permite | Lo que exige |
| :--- | :--- | :--- | :--- |
| **MIT** | Permisiva | Uso comercial, modificación, distribución y sublicenciamiento privado. | Incluir la nota de copyright original y el texto de la licencia. |
| **BSD (3-Clause)** | Permisiva | Uso comercial, redistribución y modificación sin restricciones. | Conservar avisos de copyright y no usar el nombre de los autores para promoción. |
| **Apache 2.0** | Permisiva | Uso, modificación, distribución y otorgamiento expreso de patentes. | Conservar avisos de copyright, marcas y declarar explícitamente los archivos modificados. |
| **GPL (v3)** | Copyleft Fuerte | Uso comercial, modificación y distribución del código. | Liberar **todo** el código fuente derivado bajo la misma licencia GPL. |
| **LGPL (v3)** | Copyleft Débil | Enlazar la librería con software propietario sin cerrar la librería. | Las modificaciones directas a la librería misma deben liberarse bajo LGPL. |
| **AGPL (v3)** | Copyleft de Red | Uso comercial, modificación y ejecución en servicios SaaS/Nube. | Liberar el código fuente completo a los usuarios que interactúen con el software a través de una red. |

### b) Elección de la licencia MIT para este repositorio
El repositorio del curso utiliza la **Licencia MIT**. Se eligió por su simplicidad técnica y su máxima flexibilidad: permite que tanto el profesor como otros estudiantes puedan reutilizar, inspeccionar o extender el trabajo realizado sin ninguna barrera legal (Rosen, 2004).

Si se hubiera seleccionado la licencia **GPLv3**, cualquier proyecto que tomara fragmentos de este código o se derivara de él estaría legalmente obligado a hacer público todo su código fuente bajo la misma licencia GPL. Esto prevendría la inclusión de estas tareas en proyectos comerciales de código cerrado.

### c) Caso real de bifurcación: MySQL y MariaDB
* **Qué pasó y cuándo:** En el año 2008, Sun Microsystems adquirió la empresa desarrolladora de la base de datos **MySQL**. En 2009-2010, Oracle Corporation compró Sun Microsystems, tomando el control de MySQL. Ante la incertidumbre sobre si Oracle restringiría el acceso abierto o privatizaría componentes futuros del motor de datos, Michael "Monty" Widenius (creador original de MySQL) realizó un *fork* (bifurcación) en 2009 para lanzar **MariaDB** como un reemplazo directo y 100% abierto (St. Laurent, 2004).
* **Licencia del proyecto:** El motor de MySQL estaba distribuido bajo la licencia **GNU GPL v2**.
* **Por qué la licencia lo permitió:** La licencia **GPL v2** garantiza explícitamente el derecho inalienable de cualquier usuario a estudiar, modificar y redistribuir el código fuente. Gracias a esta clausula, la comunidad de MariaDB no tuvo que solicitar autorización legal ni pagar regalías a Oracle Corporation para copiar el código base existente y continuar su desarrollo de forma independiente.

---

## Referencias

* Chacon, S., y Straub, B. (2014). *Pro Git* (2.ª ed.). Apress.
* Merkel, D. (2014). Docker: lightweight Linux containers for consistent development and deployment. *Linux Journal*, 2014(239), 2.
* Project Management Institute. (2021). *A guide to the project management body of knowledge (PMBOK guide)* (7.ª ed.). Project Management Institute.
* Pressman, R. S., y Maxim, B. R. (2021). *Software engineering: A practitioner's approach* (9.ª ed.). McGraw-Hill Education.
* Rosen, L. (2004). *Open source licensing: Software freedom and intellectual property law*. Prentice Hall Professional.
* Schwaber, K., y Sutherland, J. (2020). *La Guía de Scrum: Las Reglas del Juego*. Scrum.org.
* St. Laurent, A. M. (2004). *Understanding open source and free software licensing*. O'Reilly Media.