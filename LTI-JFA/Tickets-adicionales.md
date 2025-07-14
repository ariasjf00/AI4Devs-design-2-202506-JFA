Perfecto, aquí tienes los **tickets restantes** derivados de la historia **US001 – Postulación desde el LMS con datos precargados**, todos siguiendo el mismo formato:

---

### 🧾 Título: Diseño del Formulario de Postulación con Precarga de Datos

**Descripción:**
Diseñar la interfaz del formulario de postulación accesible desde el LMS, con campos precargados desde el contexto LTI. El formulario debe incluir campos editables en caso de datos incompletos y un área para subir el CV y escribir una carta de motivación.

---

### ✅ Criterios de Aceptación:

* El formulario incluye campos: nombre, correo, carrera, CV (archivo) y carta de motivación.
* Los campos se completan automáticamente si los datos están disponibles desde LTI.
* El diseño es responsive y accesible desde dispositivos móviles.
* Se indica visualmente qué campos son requeridos.
* Se muestra una advertencia si falta algún dato esencial.

**Prioridad:** Alta
**Estimación:** 5 puntos de historia
**Asignado a:** Equipo de Frontend
**Etiquetas:** UI, Formulario, LTI, Sprint 1

**Comentarios:**
Consultar al equipo de UX sobre estilo y lineamientos del formulario. Se debe asegurar accesibilidad para lectores de pantalla.

**Enlaces:**

* Mockups iniciales del formulario
* Documento PRD del ATS

**Historial de Cambios:**

* 13/07/2025: Creado por Product Owner (ChatGPT)

---

### 🧾 Título: Carga y Validación del CV del Candidato

**Descripción:**
Permitir la carga de archivos adjuntos al formulario (formato PDF, Word), validando el tamaño máximo y extensiones permitidas. Almacenar el archivo en el sistema y vincularlo con la postulación del candidato.

---

### ✅ Criterios de Aceptación:

* El sistema permite adjuntar archivos PDF o DOCX de hasta 5MB.
* Archivos inválidos son rechazados con mensaje claro.
* El archivo se almacena de forma segura con un identificador único.
* El backend asocia correctamente el archivo a la postulación.

**Prioridad:** Alta
**Estimación:** 3 puntos de historia
**Asignado a:** Equipo de Backend
**Etiquetas:** Archivos, Validación, Seguridad, Sprint 1

**Comentarios:**
Considerar almacenamiento local o en S3 con acceso controlado. Evaluar riesgos de seguridad al permitir carga de archivos.

**Enlaces:**

* Política de seguridad de archivos de la organización

**Historial de Cambios:**

* 13/07/2025: Creado por Product Owner (ChatGPT)

---

### 🧾 Título: Confirmación Visual y Notificación por Correo de Postulación Exitosa

**Descripción:**
Mostrar una pantalla de confirmación amigable al enviar la postulación, y enviar un correo automático al candidato confirmando que su aplicación fue recibida.

---

### ✅ Criterios de Aceptación:

* El usuario ve un mensaje de confirmación con detalles básicos de su postulación.
* Se envía un correo automático al candidato usando una plantilla predefinida.
* El mensaje se personaliza con el nombre del candidato y título de la vacante.
* La acción queda registrada en el sistema con marca de tiempo.

**Prioridad:** Alta
**Estimación:** 3 puntos de historia
**Asignado a:** Equipo de Backend
**Etiquetas:** Notificaciones, UX, Email, Sprint 2

**Comentarios:**
Plantilla de correo a revisar con equipo de comunicaciones. Verificar sistema SMTP o SendGrid.

**Enlaces:**

* Plantilla de mensajes automáticos
* Configuración de notificaciones del sistema

**Historial de Cambios:**

* 13/07/2025: Creado por Product Owner (ChatGPT)

---

### 🧾 Título: Registro de Postulación en Base de Datos y Prevención de Duplicados

**Descripción:**
Registrar correctamente la postulación del candidato en la base de datos y validar que no existan duplicados (por usuario y vacante). Asociar el archivo adjunto y los datos del formulario al registro.

---

### ✅ Criterios de Aceptación:

* Se registra una nueva postulación con datos del formulario, estado inicial y fecha de creación.
* Se impide la duplicación de postulaciones a la misma vacante por el mismo candidato.
* Se vinculan correctamente el CV y carta de motivación.
* Se loguea la acción en un historial de actividad.

**Prioridad:** Alta
**Estimación:** 4 puntos de historia
**Asignado a:** Equipo de Backend
**Etiquetas:** Base de datos, Validación, Seguridad, Sprint 2

**Comentarios:**
Usar validaciones a nivel de backend y base de datos. Requiere modelo de datos estable.

**Enlaces:**

* Esquema de base de datos del ATS
* Diagrama ER del módulo de postulaciones

**Historial de Cambios:**

* 13/07/2025: Creado por Product Owner (ChatGPT)

---

¿Quieres que empaquete estos tickets en un documento o tablero (por ejemplo en formato `.docx`, `.csv` o compatible con Jira/Trello)?
