# Aporte individual — Jocelyn Fernanda Pérez Muñoz

**Proyecto:** Fichados (Sistema Inteligente de Gestión Estudiantil y Riesgo Académico)
**Sección del proceso asignada:** Paso 5 del TO-BE (consulta de la información del estudiante por el tutor) y conservación del historial extracurricular
**Rol principal de la U3:** Desarrollo
**Fecha:** 2026-11-16

## 1. Información que necesito obtener
- **Pregunta 1:** ¿Cómo se registran actualmente los cambios de club o bajas en actividades extracurriculares y qué datos exactos conserva la institución entre semestres?
- **Pregunta 2:** ¿Qué campos específicos de la sábana generacional, kardex y retícula a color necesita ver el tutor en pantalla para revisar el caso de un estudiante?
- **Técnica elegida y motivo:** Análisis documental de los hallazgos previos (U2-E01) y entrevista breve de seguimiento con el responsable de actividades extracurriculares y tutores, porque permite confirmar qué información existe realmente sin inventar datos.
- **Fuente a consultar:** Jefe de Actividades Extracurriculares y Coordinación de División / Tutores académicos.
- **Fecha prevista o estado:** Pendiente de validación con las fuentes institucionales.

## 2. Información que ya tengo
- **Fuente real:** Entrevista al Coordinador de División (F-01, documentada en U2-E01 Tabla 6) y entrevista al Jefe de Actividades Extracurriculares (F-02, documentada en U2-E01).
- **Hallazgo comprobable:** Actualmente el tutor concentra las listas de calificaciones en una sábana generacional en Excel y consulta el kardex y la retícula a color para identificar materias no acreditadas y revisar el avance académico. En actividades extracurriculares se confirmó que es importante conservar los registros de participación a lo largo de los semestres, aunque falta confirmar cómo se manejan los cambios de club.
- **Dudas:** Confirmar si los registros actuales de clubes se pierden o simplemente requieren volver a solicitarse al cambiar de periodo, y validar qué formato exacto de historial extracurricular puede proporcionar la institución.

## 3. Necesidad identificada
- **N-01 (Respaldada en F-01):** Centralizar en una sola vista de consulta las calificaciones, asistencias y materias no acreditadas de cada estudiante para que el tutor revise su situación sin consultar documentos dispersos.
- **N-03 (Respaldada en F-02):** Conservar el historial de participación y asistencia en clubes y actividades extracurriculares para que permanezca disponible en semestres posteriores sin eliminarse al cierre del periodo.

## 4. Dos requisitos propios propuestos
> *Nota: Los IDs provisionales corresponden a mi aporte individual; al integrarse en el catálogo colectivo U3-E01 se numeraron como `RF-05` y `RNF-02`. Se quitó como hecho que los registros «se pierden» cuando un estudiante cambia de club, porque todavía no está comprobado.*

| ID provisional | Tipo | Enunciado verificable | Origen (Fuente / Necesidad) | Prioridad y motivo | Estado |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **RF-01** *(RF-05 en E01)* | RF | El sistema debe permitir al tutor consultar, para un estudiante seleccionado, sus calificaciones, asistencias y materias no acreditadas. | Documento U2-E01 · Tabla 6 (pasos 4–6 del AS-IS: concentrado de calificaciones, Kardex y retícula) y paso 5 del TO-BE; entrevista F-01 [fecha pendiente]. | **P1:** Sin esta consulta el tutor no puede revisar el caso de un estudiante. | Por validar |
| **RNF-02** *(RNF-02 en E01)* | RNF | El sistema debe conservar la información de participación de los estudiantes en clubes y actividades extracurriculares y mantenerla disponible para consulta en los semestres siguientes, sin eliminarla automáticamente al terminar un periodo. | Propuesta inicial U1-E02 · necesidad de no recopilar la información nuevamente cada semestre (F-02). Falta confirmar cómo se registran hoy los cambios de club. | **P2:** Aporta al objetivo de no volver a pedir la información, pero la primera versión puede generar alertas con los datos académicos. | Por validar |

## 5. Criterios de aceptación

| Requisito | Condición (Dado) | Acción (Cuando) | Resultado comprobable (Entonces) |
| :--- | :--- | :--- | :--- |
| **RF-01 · éxito** | Un estudiante registrado en el sistema. | El tutor lo busca y lo selecciona. | Ve sus calificaciones, asistencias y materias no acreditadas, que corresponden a ese estudiante. |
| **RF-01 · alternativa** | Un nombre o matrícula que no existe en el sistema. | El tutor lo busca. | El sistema indica que no se encontró al estudiante. |
| **RNF-02 · éxito** | Terminó un semestre y hay registros de participación extracurricular. | Se consulta la información en el semestre siguiente. | Los registros del semestre anterior siguen disponibles. |
| **RNF-02 · alternativa** | Un estudiante cambió de club o dejó una actividad. | Se consulta su historial de participación. | El registro anterior sigue disponible y no se elimina automáticamente. |

## 6. Pendientes y referencias
- **Pendiente de validación:** Consultar al responsable de actividades extracurriculares cómo se registran hoy los cambios de club y si los registros se conservan; al obtenerlo, registrar la fuente y pasar `RNF-02` a «Validado». También confirmar la fecha exacta de la entrevista con Coordinación de División (`F-01`).
- **Referencias:**
  - Documento del equipo `U1-E02` y `U2-E01` (Tabla 6: proceso AS-IS y TO-BE).
  - Notas de entrevista con Coordinador de División (`F-01`) y Jefe de Actividades Extracurriculares (`F-02`).
