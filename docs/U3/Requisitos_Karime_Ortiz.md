<!-- Archivo: docs/U3/U3-E01_Fichados_Requisitos.md -->
# U3 · Especificación de requisitos — Fichados

**Versión:** 0.2  
**Fecha:** 16/11/2026  
**Equipo y roles:** 
Frida Sofía Zamora Quezada: Análisis.
Jocelyn Fernanda Pérez Muñoz: Desarrollo
Karime Ortiz Reyes : Coordinación
Gilberto Juarez Hernández :Documentación y Calidad 

**Estado:** En elaboración
## A. Identificación y alcance

- Proyecto: Fichados – Sistema Inteligente de Gestión Estudiantil y Riesgo Académico.
- Proceso TO-BE seleccionado: Seguimiento académico de los estudiantes (proceso mejorado de la Unidad 2).
- Objetivo de esta especificación: Facilitar la consulta y el análisis de la información académica para identificar posibles señales de riesgo y ayudar al tutor a dar seguimiento a los estudiantes.
- Dentro del alcance:
  - Consultar calificaciones y asistencias.
  - Identificar materias no acreditadas.
  - Detectar posibles señales de riesgo académico.
  - Generar alertas para que el tutor revise los casos.
  - Conservar la información de participación extracurricular.
- Fuera del alcance:
  - Tomar decisiones automáticamente sobre los estudiantes.
  - Determinar por sí solo si un estudiante abandonará sus estudios.
  - Sustituir el trabajo del tutor.

## B. Fuentes y necesidades

### B1. Plan de obtención

| Pregunta por resolver                                                                                    | Persona o documento a consultar              | Técnica                          | Responsable                               | Estado    |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------- | -------------------------------- | ----------------------------------------- | --------- |
| ¿Qué criterios se usan para considerar que un estudiante está en riesgo?                                 | Tutor académico y reglamento institucional   | Entrevista o análisis documental | Análisis (Frida Sofía Zamora Quezada)     | Pendiente |
| ¿Qué datos académicos y extracurriculares puede entregar la escuela, desde qué periodo y en qué formato? | Control escolar                              | Entrevista o análisis documental | Desarrollo (Jocelyn Fernanda Pérez Muñoz) | Pendiente |
| ¿Quién debe tener acceso a los datos de los estudiantes?                                                 | Control escolar                              | Entrevista                       | Análisis (Frida Sofía Zamora Quezada)     | Pendiente |
| ¿Cómo se registran hoy los cambios de club y se conserva la participación de un periodo a otro?          | Responsable de actividades extracurriculares | Entrevista                       | Desarrollo (Jocelyn Fernanda Pérez Muñoz) | Pendiente |
| Cuando el tutor revisa a un estudiante en riesgo, ¿qué hace y cómo deja constancia de su decisión?       | Tutor académico                              | Entrevista                       | Análisis (Frida Sofía Zamora Quezada)     | Pendiente |
| Cuando falta una calificación o una asistencia, ¿cómo se detecta y quién la completa?                    | Control escolar y docentes                   | Entrevista                       | Desarrollo (Jocelyn Fernanda Pérez Muñoz) | Pendiente |

### B2. Fuentes realmente consultadas

Para conocer cómo se realiza actualmente el seguimiento de los estudiantes, se tomó como referencia la información obtenida en las entrevistas realizadas al jefe de carrera y al jefe de actividades extracurriculares.

| ID   | Técnica    | Fuente                                | Fecha de obtención | Hallazgo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Respaldo                                         | Validación |
| ---- | ---------- | ------------------------------------- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | ---------- |
| F-01 | Entrevista | Jefe de carrera                       | 22/10/2026         | En calificaciones, el sistema ahora registra valores como 30 o 40 (no solo ceros), lo que da una pista del riesgo. Algunos maestros usan Excel para sumar rubros y otros ponen cero a quien no entrega. La asistencia solo se marca como sí o no, y las faltas indican mayor riesgo. Cada materia envía su lista al tutor, quien junta todo en una "sábana generacional" (Excel con el historial semestre por semestre) para buscar números rojos. También usan el Kardex y la retícula a color, donde las materias reprobadas se marcan en rojo. | Audio grabado al jefe de carrera                 | Validado   |
| F-02 | Entrevista | Jefe de actividades extracurriculares | Septiembre 2026    | Se lleva un seguimiento de las actividades extracurriculares.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Documentos y notas de la U1 del equipo Fichados. | Validado   |


### B3. Necesidades identificadas

| ID | Necesidad | Fuente que la respalda |
|---|---|---|
| N-01 | Facilitar la consulta de información académica. | F-01 |
| N-02 | Conservar la información de participación de los estudiantes. | F-02 |
| N-03 | Reducir el trabajo manual de concentrar en Excel las listas de varias materias. | F-01 |
| N-04 | Saber cuándo la información de un estudiante está incompleta antes de analizarla (respaldo parcial: un cero puede significar que no entregó o que no se registró). | F-01 |

### B4. Pendientes

| Duda                                                            | Fuente por consultar                         | Responsable |
| --------------------------------------------------------------- | -------------------------------------------- | ----------- |
| Qué datos pueden utilizarse en el sistema                       | Control escolar                              | Jocelyn     |
| Qué registros extracurriculares están disponibles               | Responsable de actividades extracurriculares | Jocelyn     |
| Qué criterios definen a un estudiante en riesgo                 | Tutor académico y reglamento                 | Frida       |
| Quién debe tener acceso a los datos y a las alertas             | Control escolar                              | Karime      |
| Cómo deja constancia el tutor de su decisión sobre una alerta   | Tutor académico                              | Gilberto    |
| Si una alerta debe ser revisada por una persona antes de actuar | Tutor o coordinación                         | Frida       |

## C. Organización del alcance

- Ruta elegida: B (directa), requisitos directos.
- Motivo de elección: El proceso está acotado y queremos trabajar directamente con las necesidades identificadas, convirtiéndolas en requisitos para el sistema, sin tener que desarrollar una épica.
- Proceso: Seguimiento académico de los estudiantes.
- Objetivo: Facilitar la consulta de la información académica y la identificación de posibles señales de riesgo.
- Requisitos vinculados: RF-01 a RF-06, RNF-01 y RNF-02 (propuestos, ver sección E).

Los requisitos se enfocarán principalmente en:

- Consulta de información académica.
- Identificación de posibles señales de riesgo.
- Conservación de información extracurricular.

## D. Reglas del dominio

| ID    | Regla                                                                                                                                                                      | Quién la establece                               | Origen en B2              | Estado      |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------ | ------------------------- | ----------- |
| RG-01 | La información académica debe estar registrada para poder realizar un análisis.                                                                                            | Personal responsable de los registros académicos | F-01 (parcial)            | Por validar |
| RG-02 | Una alerta de posible riesgo debe ser revisada por el tutor antes de tomar alguna decisión.                                                                                | Tutor académico y coordinación                   | Origen pendiente · ver B4 | Propuesto   |
| RG-03 | La información extracurricular debe conservarse para poder consultar la participación de los estudiantes en diferentes periodos.                                           | Jefe de actividades extracurriculares            | F-02 (parcial)            | Por validar |
| RG-04 | La institución define los criterios para considerar a un estudiante en riesgo (por ejemplo, inasistencias o materias reprobadas); los valores exactos están por confirmar. | Institución (tutor académico y reglamento)       | Origen pendiente · ver B4 | Propuesto   |

## E. Catálogo de requisitos

> RF y RNF se numeran por separado. Los IDs no indican orden de ejecución.

| ID     | Tipo | Enunciado verificable                                                                                                                                                                                                                            | Origen (F / N)            | Prioridad | Motivo                                                                                                                          | Autor                        | Estado      |
| ------ | ---- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------- | ---------------------------- | ----------- |
| RF-01  | RF   | El sistema debe permitir al personal administrativo y a los docentes cargar o sincronizar las calificaciones y asistencias de los estudiantes, sin duplicar registros.                                                                           | F-01 / N-03               | P1        | Sin los datos cargados no hay información que centralizar ni analizar.                                                          | Karime Ortiz Reyes           | Por validar |
| RF-02  | RF   | El sistema debe mostrar un aviso cuando a un estudiante le falte una calificación o una asistencia necesaria para el análisis, y no debe analizarlo hasta que el dato se complete o se verifique.                                                | F-01 / N-04               | P1        | Con datos incompletos el análisis puede generar una alerta incorrecta.                                                          | Gilberto Juarez Hernández    | Por validar |
| RF-03  | RF   | El sistema debe generar una alerta asociada a un alumno únicamente cuando sus indicadores cumplan los criterios de riesgo definidos.                                                                                                             | Origen pendiente · ver B4 | P1        | Sin esta condición el sistema alertaría sin sustento o dejaría pasar casos.                                                     | Frida Sofía Zamora Quezada   | Propuesto   |
| RF-04  | RF   | El sistema debe mostrar al tutor, junto con cada alerta, los indicadores que la originaron.                                                                                                                                                      | Origen pendiente · ver B4 | P1        | Sin ese detalle el tutor no puede evaluar el caso.                                                                              | Frida Sofía Zamora Quezada   | Propuesto   |
| RF-05  | RF   | El sistema debe permitir al tutor consultar, para un estudiante seleccionado, sus calificaciones, asistencias y materias no acreditadas.                                                                                                         | F-01 / N-01               | P1        | Sin esta consulta el tutor no puede revisar el caso de un estudiante.                                                           | Jocelyn Fernanda Pérez Muñoz | Por validar |
| RF-06  | RF   | El sistema debe permitir al tutor registrar, para cada alerta que recibe, si el estudiante requiere seguimiento o no, y guardar esa decisión con la fecha.                                                                                       | Origen pendiente · ver B4 | P1        | Cierra el proceso y permite medir cuántas alertas se revisan.                                                                   | Gilberto Juarez Hernández    | Propuesto   |
| RNF-01 | RNF  | El sistema debe permitir consultar los datos académicos y las alertas de un estudiante únicamente a usuarios autenticados con un rol autorizado (tutor asignado o personal administrativo).                                                      | Origen pendiente · ver B4 | P1        | Son datos personales de estudiantes y un acceso indebido sería un riesgo grave.                                                 | Karime Ortiz Reyes           | Propuesto   |
| RNF-02 | RNF  | El sistema debe conservar la información de participación de los estudiantes en clubes y actividades extracurriculares y mantenerla disponible para consulta en los semestres siguientes, sin eliminarla automáticamente al terminar un periodo. | F-02 / N-02               | P2        | Aporta al objetivo de no volver a pedir la información, pero la primera versión puede generar alertas con los datos académicos. | Jocelyn Fernanda Pérez Muñoz | Por validar |

## F. Criterios de aceptación

| ID                   | Condición (Dado)                                                                                   | Acción (Cuando)                                      | Resultado comprobable (Entonces)                                                                                     |
| -------------------- | -------------------------------------------------------------------------------------------------- | ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| RF-01 · éxito        | Un archivo con calificaciones y asistencias válidas.                                               | Un usuario autorizado lo carga.                      | Los datos quedan registrados en el sistema sin duplicar a ningún estudiante.                                         |
| RF-01 · alternativa  | Un archivo con un estudiante que ya estaba registrado.                                             | Se carga el archivo.                                 | Se actualiza su registro y no se crea uno nuevo.                                                                     |
| RF-02 · éxito        | A un estudiante le falta la calificación de una materia.                                           | Se intenta realizar el análisis de su información.   | Se muestra un aviso con el dato que falta y no se genera alerta para ese estudiante hasta completarlo o verificarlo. |
| RF-02 · alternativa  | Un estudiante tiene completas sus calificaciones y asistencias.                                    | Se realiza el análisis.                              | El análisis continúa sin mostrar el aviso.                                                                           |
| RF-03 · éxito        | Un alumno cuyos indicadores cumplen los criterios de riesgo [criterio por confirmar con el tutor]. | El sistema realiza el análisis.                      | Se genera una alerta asociada a ese alumno.                                                                          |
| RF-03 · alternativa  | Un alumno cuyos indicadores no cumplen los criterios de riesgo.                                    | El sistema realiza el análisis.                      | No se genera alerta.                                                                                                 |
| RF-04 · éxito        | Un alumno con una alerta generada.                                                                 | El tutor abre la alerta.                             | Ve la lista de indicadores que la originaron.                                                                        |
| RF-04 · alternativa  | El sistema no puede determinar los indicadores que originaron la alerta.                           | El tutor abre la alerta.                             | Aparece un aviso de que el detalle no está disponible.                                                               |
| RF-05 · éxito        | Un estudiante registrado en el sistema.                                                            | El tutor lo busca y lo selecciona.                   | Ve sus calificaciones, asistencias y materias no acreditadas, que corresponden a ese estudiante.                     |
| RF-05 · alternativa  | Un nombre o matrícula que no existe en el sistema.                                                 | El tutor lo busca.                                   | El sistema indica que no se encontró al estudiante.                                                                  |
| RF-06 · éxito        | El tutor tiene una alerta recibida.                                                                | Marca si el estudiante requiere seguimiento o no.    | Se guarda la decisión con la fecha y la alerta queda como revisada.                                                  |
| RF-06 · alternativa  | Una alerta no tiene decisión registrada.                                                           | Se consulta su estado.                               | Aparece como pendiente de revisión.                                                                                  |
| RNF-01 · éxito       | Un usuario autenticado con rol de tutor asignado al estudiante.                                    | Consulta una alerta o los datos del estudiante.      | Puede verlos.                                                                                                        |
| RNF-01 · alternativa | Un usuario sin autenticar o sin rol autorizado.                                                    | Intenta consultar los datos de un estudiante.        | El acceso se bloquea y se muestra un mensaje de acceso no autorizado.                                                |
| RNF-02 · éxito       | Terminó un semestre y hay registros de participación extracurricular.                              | Se consulta la información en el semestre siguiente. | Los registros del semestre anterior siguen disponibles.                                                              |
| RNF-02 · alternativa | Un estudiante cambió de club o dejó una actividad.                                                 | Se consulta su historial de participación.           | El registro anterior sigue disponible y no se elimina automáticamente.                                               |
## G. Backlog y boceto

### Backlog priorizado
| Orden | ID | Prioridad | Depende de | Tarjeta Trello |
| :--- | :--- | :--- | :--- | :--- |
| 1 | RNF-01 | P1 | Ninguno | [Pendiente enlazar URL tarjeta Trello] |
| 2 | RF-01 | P1 | RNF-01 | [Pendiente enlazar URL tarjeta Trello] |
| 3 | RF-02 | P1 | RF-01 | [Pendiente enlazar URL tarjeta Trello] |
| 4 | RF-03 | P1 | RF-02 | [Pendiente enlazar URL tarjeta Trello] |
| 5 | RF-04 | P1 | RF-03 | [Pendiente enlazar URL tarjeta Trello] |
| 6 | RF-05 | P1 | RF-01 | [Pendiente enlazar URL tarjeta Trello] |
| 7 | RF-06 | P1 | RF-04, RF-05 | [Pendiente enlazar URL tarjeta Trello] |
| 8 | RNF-02 | P2 | RNF-01 | [Pendiente enlazar URL tarjeta Trello] |

### Cuatro estados del recorrido principal (Prototipo)
* **Archivo guardado en:** `docs/U3/prototipo/U3_Prototipo_Fichados_Recorrido.png`
* **Requisitos representados en las vistas:** `RNF-01`, `RF-01`, `RF-03`, `RF-04`, `RF-05`, `RF-06` *(nota: `RF-02` y `RNF-02` no tienen representación visual directa en el boceto actual y su comprobación se detalla en la tabla de trazabilidad H)*.

![Recorrido principal Fichados](prototipo/U3_Prototipo_Fichados_Recorrido.png)

* **Explicación del recorrido y su relación con los requisitos:**
  * **Vista `00 · Login - Inicio de Sesión` (`RNF-01`):** Punto de acceso al sistema donde el tutor o personal administrativo ingresa su correo institucional y contraseña para acceder únicamente a la información autorizada por su rol.
  * **Vista `Ext 01 · Captura de Datos` (`RF-01`):** Permite al docente o personal autorizado registrar y guardar las asistencias y evaluaciones parciales por materia y grupo sin duplicar registros.
  * **Vista `01 · Inicio - Panel de Seguimiento` (`RF-03`, `RF-04`):** Pantalla principal del tutor que muestra el resumen de alumnos, el total de alertas activas generadas para quienes cumplen criterios de riesgo (`RF-03`) y el indicador principal que originó cada alerta, como porcentaje de asistencia o promedio (`RF-04`).
  * **Vista `Ext 02 · Expediente del Alumno` (`RF-04`, `RF-05`, `RF-06`):** Al seleccionar «Ver Expediente», el tutor consulta la matrícula, promedio global, detalle del diagnóstico/indicadores (`RF-04`) y la retícula semestral con las materias acreditadas y no acreditadas del estudiante (`RF-05`). En la parte inferior incluye las opciones para registrar la decisión del tutor («Archivar Alerta» o «Agendar Cita / Canalizar», vinculadas a `RF-06`).
  * **Vistas `02 · Acción`, `03A · Éxito`, `03B · Error` y `04 · Resultado` (`RF-06`):** Ilustran el recorrido propuesto para que el tutor registre su decisión de seguimiento sobre una alerta (ya sea canalizando mediante cita con fecha/hora en `02`, o archivando la alerta en `Ext 03A/03B`). Si los datos son válidos (`03A`), se guarda el registro y en la vista `04 · Panel Actualizado` el tutor puede consultar posteriormente el estado del seguimiento del estudiante (`Cita Agendada`). Si ocurre un error o falta información (`03B`), se muestra un mensaje explicativo en texto con la opción de corregir. *(Nota: Los detalles operativos sobre citas de canalización y archivo de alertas quedan marcados como «Por validar» hasta confirmarse con Coordinación de División en B4).*

---

## H. Trazabilidad

| Fuente (B2 / Antecedente) | Necesidad (B3) | ID (E) | Criterio (F) | Boceto o comprobación (G) |
| :--- | :--- | :--- | :--- | :--- |
| F-01 / U2-E01 Tabla 6 (pasos 1–3 AS-IS y paso 1 TO-BE) | N-03 (Reducir el trabajo manual de concentrar datos) | **RF-01** | F. RF-01 (éxito y alternativa) | Vista `Ext 01 · Captura de Datos` |
| U2-E01 Tablas 7–8 / U1-E02 apartado 9 | N-04 (Saber cuándo la información está incompleta) | **RF-02** | F. RF-02 (éxito y alternativa) | No representable en boceto actual; prueba propuesta: intentar ejecutar el análisis con un dato faltante y verificar el aviso. |
| Pendiente B4 | Pendiente (Detectar señales de riesgo) | **RF-03** | F. RF-03 (éxito y alternativa) | Vista `01 · Inicio - Panel de Seguimiento` (listado de alertas activas) |
| Pendiente B4 | Pendiente (Mostrar indicadores de riesgo) | **RF-04** | F. RF-04 (éxito y alternativa) | Vista `01 · Panel de Seguimiento` y `Ext 02 · Expediente del Alumno` |
| F-01 / U2-E01 Tabla 6 (pasos 4–6 AS-IS y paso 5 TO-BE) | N-01 (Facilitar la consulta de información académica) | **RF-05** | F. RF-05 (éxito y alternativa) | Vista `Ext 02 · Expediente del Alumno` (promedio, asistencia y retícula) |
| U2-E01 (TO-BE pasos 5–6) | Pendiente (Registrar decisión del tutor) | **RF-06** | F. RF-06 (éxito y alternativa) | Vistas `02 · Acción`, `03A · Éxito`, `03B · Error`, `04 · Resultado` y `Ext 03A/03B · Archivar Alerta` |
| Pendiente B4 (Consultar con Control Escolar) | N-01 (Facilitar consulta y control de acceso) | **RNF-01** | F. RNF-01 (éxito y alternativa) | Vista `00 · Login - Inicio de Sesión` y prueba de intento de acceso no autorizado. |
| F-02 / Propuesta inicial U1-E02 | N-02 (Conservar la información de participación) | **RNF-02** | F. RNF-02 (éxito y alternativa) | No representable en boceto actual; prueba propuesta: consultar los registros de un semestre posterior. |

### Registro de cambios y revisiones
| Fecha      | Solicitud o motivo                                                                                   | IDs afectados                 | Decisión                                                                                                                              | Enlace al PR revisado                    |
| :--------- | :--------------------------------------------------------------------------------------------------- | :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------------ | :--------------------------------------- |
| 2026-11-16 | Integración de los 8 requisitos individuales del equipo y vinculación con el prototipo de recorrido. | RF-01 a RF-06, RNF-01, RNF-02 | Se unificaron los IDs de forma consecutiva evitando duplicados y se mantuvieron todos en estado «Por validar» hasta confirmar reglas. | [Pendiente enlazar URL del PR en GitHub] |

## I. Referencias y herramientas

### Fuentes de información

- Entrevista · Jefe de carrera · técnica: entrevista · fecha: 22/10/2026 · resumen: ver F-01 en B2 · respaldo: Audio grabado.
- Entrevista · Jefe de actividades extracurriculares · técnica: entrevista · fecha: Septiembre 2026 · resumen: ver F-02 en B2 · respaldo: Documentos de la U1.
- Equipo Fichados. (2026, 8 de septiembre). *Propuesta inicial del proyecto, Versión 0* (U1-E02) [Documento de trabajo del equipo]. Repositorio del equipo, docs/U1.
- Equipo Fichados. (2026). *Modelo de negocio* (U2-E01) [Documento de trabajo del equipo]. Repositorio del equipo, docs/U2.

### Herramientas y recursos

| Herramienta | Proveedor | Uso real | Enlace oficial |
|---|---|---|---|
| GitHub | GitHub, Inc. | Repositorio, ramas y Pull Requests | https://github.com |
| Trello | Atlassian | Tarjetas de trabajo del equipo | https://trello.com |
| Lucidchart | Lucid Software | Boceto del recorrido en docs/U3/prototipo/ | https://www.lucidchart.com |

**Uso de IA:** Se utilizó inteligencia artificial como apoyo para estructurar el catálogo, redactar los enunciados verificables y dar formato al Markdown. Toda la información, fuentes y decisiones fueron revisadas y validadas por el equipo.