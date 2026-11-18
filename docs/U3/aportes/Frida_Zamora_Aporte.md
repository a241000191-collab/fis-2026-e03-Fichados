# Aporte individual — Frida Sofia Zamora Quezada

**Proyecto:** Fichados

**Sección del proceso asignada:** Pasos 3–4 del TO-BE: análisis de patrones y generación de la alerta

**Rol principal de la U3:** Análisis

**Fecha:** 2026-11-09

## 1. Información que necesito obtener
- Pregunta 1: ¿Con qué criterios decide hoy el tutor que un alumno requiere atención (número de materias reprobadas, inasistencias, otros)?
- Pregunta 2: ¿Existe un reglamento con criterios de reprobación por inasistencias o de seguimiento a alumnos?
- Pregunta 3: ¿Qué información necesita ver el tutor en una alerta para evaluar el caso?
- Técnica elegida y motivo: entrevista al tutor (conoce el criterio real) y análisis documental del reglamento
- Fuente a consultar: tutor académico; reglamento académico / control escolar
- Fecha prevista o estado:Pendiente

## 2. Información que ya tengo
- Fuente real: entrevistas de la U2 al Jefe de carrea, fecha 22/10/26, respaldo [notas / enlace]
- Hallazgo comprobable: el tutor ubica a los alumnos con varias materias reprobadas usando un concentrado en Excel, el kardex y la retícula a color
- Dudas: cuántas reprobadas o inasistencias consideran riesgo; qué datos podrá usar el proyecto; el AS-IS no incluye un paso extracurricular

## 3. Necesidad identificada
N-01 (provisional): el tutor necesita ubicar a los alumnos con más materias reprobadas sin armar manualmente el concentrado. Depende de que la entrevista tenga respaldo; si no, queda «Por validar».

## 4. Requisitos 
| ID | Tipo | Enunciado verificable | Origen | Prioridad y motivo | Autor | Estado |
|---|---|---|---|---|---|---|
| RF-xx | RF | El sistema debe generar una alerta asociada a un alumno únicamente cuando sus indicadores cumplan los criterios de riesgo definidos. | Origen pendiente · ver B4 | P1 · Sin esta condición el sistema alertaría sin sustento o dejaría pasar casos. | Frida Zamora | Por validar |
| RF-xx | RF | El sistema debe mostrar al tutor, junto con cada alerta, los indicadores que la originaron. | Origen pendiente · ver B4 | P1 · Sin ese detalle el tutor no puede evaluar el caso. | Frida Zamora | Por validar |



## 5. Criterios de aceptación
| Requisito | Condición (Dado) | Acción (Cuando) | Resultado comprobable (Entonces) |
|---|---|---|---|
| Generar alerta · éxito | Un alumno cuyos indicadores cumplen los criterios de riesgo [criterio por confirmar con el tutor]. | El sistema realiza el análisis. | Se genera una alerta asociada a ese alumno. |
| Generar alerta · alternativa | Un alumno cuyos indicadores no cumplen los criterios. | El sistema realiza el análisis. | No se genera alerta. |
| Mostrar indicadores · éxito | Un alumno con una alerta generada. | El tutor abre la alerta. | Ve la lista de indicadores que la originaron. |
| Mostrar indicadores · alternativa | El sistema no puede determinar los indicadores. | El tutor abre la alerta. | Aparece un aviso de que el detalle no está disponible. |

## 6. Pendientes
- Consultar al tutor sobre los criterios de riesgo; al obtenerlos, pasar el primer requisito a «Validado» y registrar la fuente.
- Confirmar con el equipo que no se dupliquen estos requisitos con los de otras partes del proceso.
