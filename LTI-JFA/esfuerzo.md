Excelente. Como los tickets ya están claramente definidos, relacionados entre sí y con criterios técnicos bien descritos, la metodología más conveniente en este caso es la **secuencia de Fibonacci**, ya que:

* ✅ Permite diferenciar esfuerzos pequeños, medios y grandes de forma objetiva.
* ✅ Se adapta bien a tareas técnicas detalladas como las descritas (autenticación, carga de archivos, formularios, etc.).
* ✅ Facilita una futura planificación por sprints.

---

## 📊 Estimación de Tickets con Secuencia Fibonacci

| Ticket                                                                      | Estimación (pts) | Justificación                                                                                                     |
| --------------------------------------------------------------------------- | ---------------- | ----------------------------------------------------------------------------------------------------------------- |
| **1. Implementación de Autenticación LTI y Precarga de Datos desde LMS**    | **8**            | Requiere integración con estándar LTI 1.3, verificación de tokens JWT, manejo de usuarios y sesiones.             |
| **2. Diseño del Formulario de Postulación con Precarga de Datos**           | **5**            | Frontend con precarga de campos, validaciones visuales, diseño responsive. Complejidad media.                     |
| **3. Carga y Validación del CV del Candidato**                              | **3**            | Tarea técnica acotada (validar, subir, asociar archivo). Requiere medidas básicas de seguridad.                   |
| **4. Confirmación Visual y Notificación por Correo de Postulación Exitosa** | **3**            | Incluye diseño simple y lógica de envío de correo. Bajo riesgo y bien soportado técnicamente.                     |
| **5. Registro de Postulación en Base de Datos y Prevención de Duplicados**  | **5**            | Incluye validaciones, relación con otras entidades, lógica de persistencia y seguridad básica. Complejidad media. |

---

¿Te gustaría que agregue esta estimación al documento `.docx` de los tickets ya generado, o que prepare una tabla independiente para planificación en sprint o Jira?
