


Proyecto: Fichados
Sección del proceso asignada: Pasos 2–3 y 6 del TO-BE: verificación de los datos antes del análisis y decisión del tutor sobre la alerta.
Rol principal de la U3: Documentación
Fecha: 17/11/2026

## 1. Información que necesito obtener
* **Pregunta 1:** Cuando el tutor revisa a un estudiante en riesgo, ¿qué hace y cómo deja constancia de su decisión?
* **Pregunta 2:** Cuando falta una calificación o una asistencia de un estudiante, ¿cómo se detecta y quién la completa?
* **Técnica elegida y motivo:** Entrevista breve, porque el tutor y control escolar son quienes realizan hoy estos pasos.
* **Fuente a consultar:** Tutor académico (pregunta 1) y control escolar (pregunta 2).
* **Fecha prevista o estado:** Pendiente.

## 2. Información que ya tengo
* **Fuente real:** Entrevista al Jefe de carrera, del 22/10/2026 (audio grabado al jefe de carrera).
* **Hallazgo comprobable:** Las calificaciones y la asistencia se registran en un sistema, algunos docentes llevan las suyas en Excel y algunos ponen cero a quien no entregó nada. El tutor concentra las listas de las materias en un archivo de Excel. Todavía no hay información sobre cómo se detectan los datos faltantes ni sobre dónde deja constancia el tutor de su decisión.
* **Dudas:** ¿Un cero significa que no entregó o que no se registró la calificación? ¿Dónde queda registrada hoy la decisión del tutor?

## 3. Necesidad identificada
* Saber cuándo la información académica de un estudiante está incompleta antes de analizarla. Respaldo parcial: F-01; falta confirmar con control escolar.
* Dejar constancia de la decisión del tutor sobre cada alerta. Pendiente de confirmar con el tutor; la entrevista disponible no lo menciona.

## 4. Requisitos provisionales (borrador)
*Nota: Los IDs son provisionales; el equipo asignará los definitivos al integrar el catálogo de E01 (en el documento final del equipo corresponden al RF-02 y RF-06).*

| ID | Tipo | Enunciado verificable | Origen | Prioridad y motivo | Autor | Estado |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| RF-01 | RF | El sistema debe mostrar un aviso cuando a un estudiante le falte una calificación o una asistencia necesaria para el análisis, y no debe analizarlo hasta que el dato se complete o se verifique. | Documento U2-E01 · Tablas 7 y 8 (caso con error y prueba propuesta); propuesta inicial U1-E02, apartado 9 (riesgos iniciales). | P1 · Con datos incompletos el análisis puede generar una alerta incorrecta, riesgo que el equipo ya identificó. | Gilberto Juarez Hernández | Por validar |
| RF-02 | RF | El sistema debe permitir al tutor registrar, para cada alerta que recibe, si el estudiante requiere seguimiento o no, y guardar esa decisión con la fecha. | Documento U2-E01 · pasos 5–6 del TO-BE e indicador del proyecto (alertas revisadas por una persona responsable). | P1 · Cierra el proceso y permite medir el indicador; sin este registro no se sabe qué alertas se revisaron. | Gilberto Juarez Hernández | Por validar |

## 5. Comprobación propuesta (Criterios de aceptación)

| Requisito | Condición (Dado) | Acción (Cuando) | Resultado comprobable (Entonces) |
| :--- | :--- | :--- | :--- |
| RF-01 · éxito | A un estudiante le falta la calificación de una materia. | Se intenta realizar el análisis de su información. | Se muestra un aviso con el dato que falta y no se genera alerta para ese estudiante hasta completarlo o verificarlo. |
| RF-01 · alternativa | Un estudiante tiene completas sus calificaciones y asistencias. | Se realiza el análisis. | El análisis continúa sin mostrar el aviso. |
| RF-02 · éxito | El tutor tiene una alerta recibida. | Marca si el estudiante requiere seguimiento o no. | Se guarda la decisión con la fecha y la alerta queda como revisada. |
| RF-02 · alternativa | Una alerta no tiene decisión registrada. | Se consulta su estado. | Aparece como pendiente de revisión. |

