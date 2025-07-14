A partir de las **cuatro historias de usuario** que desarrollamos (postulación desde LMS, gestión de pipeline, notificaciones automáticas y recomendaciones con IA), los **requisitos técnicos** necesarios se pueden agrupar y organizar en categorías clave. A continuación, te presento una lista detallada de estos requisitos técnicos por módulo o funcionalidad:

---

## 🧩 1. Requisitos Técnicos por Historia de Usuario

---

### 🧾 **ATS-US001: Postulación desde el LMS (LTI)**

**🔌 Integración y autenticación**

* Soporte para el protocolo **LTI 1.3** (OAuth2 + JWT)
* Autenticación automática desde el LMS (SSO)
* Extracción de datos del usuario desde el contexto LTI

**🗂️ Backend**

* API RESTful para recibir y registrar postulaciones
* Servicio de almacenamiento de archivos (CVs en PDF/Word)
* Validación de campos obligatorios (datos y adjuntos)

**💻 Frontend**

* Formulario web responsive embebido vía LTI
* Precarga de datos del usuario
* Confirmación visual y mensaje de éxito

**📧 Notificaciones**

* Integración con sistema de correo (SMTP, SendGrid, Mailgun)

---

### 🧾 **ATS-US002: Panel de gestión de postulaciones (pipeline)**

**🗃️ Backend**

* Modelo de datos con etapas personalizables (postulado, entrevista, etc.)
* API para consultar, actualizar y mover candidatos entre etapas
* Registro de auditoría (logs de acciones y cambios de estado)

**🖼️ Frontend**

* Interfaz tipo **Kanban** con arrastrar y soltar (drag-and-drop)
* Filtros por vacante, estado, palabra clave
* Tarjetas informativas por candidato (nombre, fecha, estado)

**🔐 Seguridad**

* Control de permisos: solo usuarios con rol "reclutador" pueden gestionar pipeline

---

### 🧾 **ATS-US003: Notificaciones automáticas por cambio de estado**

**📨 Backend**

* Servicio de eventos que detecta cambios de estado en una postulación
* Plantillas personalizables de correo por etapa
* Registro del historial de notificaciones enviadas

**⚙️ Configuración**

* Panel de preferencias por usuario (correo, sistema, ambos)
* Activación o desactivación de notificaciones por vacante

**📧 Servicios externos**

* SMTP o integración con proveedor de email (SendGrid, AWS SES, etc.)

---

### 🧾 **ATS-US004: Recomendaciones personalizadas con IA**

**🧠 Machine Learning / IA**

* Modelo de recomendación (filtrado colaborativo, basado en contenido o híbrido)
* Pipeline de entrenamiento con historial de candidaturas, perfiles y vacantes
* Ajuste dinámico según interacciones del usuario (postulaciones, clics, feedback)

**🧾 Backend**

* Servicio de scoring que devuelve ranking de vacantes para un perfil
* Registro de feedback del usuario (interesado / no relevante)
* Almacenamiento vectorial de perfiles y vacantes para similitud semántica

**🎛️ Frontend**

* Sección de "Vacantes sugeridas para ti"
* Explicaciones de la sugerencia (“coincide con tu experiencia en análisis de datos”)
* Botones de retroalimentación (“me interesa”, “no es relevante”)

---

## 📦 2. Requisitos de Infraestructura General

* Contenedores Docker para despliegue modular
* Base de datos PostgreSQL o similar relacional
* Almacenamiento en la nube para archivos (ej. Amazon S3, Azure Blob)
* CI/CD para pruebas y despliegue automatizado (GitHub Actions, GitLab CI)
* Seguridad: HTTPS, control de acceso por roles, auditoría de acciones

---

## 🧰 3. Librerías, Frameworks y Tecnologías sugeridas

| Elemento                | Tecnología Sugerida               |
| ----------------------- | --------------------------------- |
| Backend API             | Django REST Framework / FastAPI   |
| Frontend SPA            | React / Vue.js                    |
| Recomendaciones IA      | scikit-learn, LightFM, TensorFlow |
| Notificaciones          | SendGrid / SMTP / Celery          |
| LTI Integration         | `pylti1.3` / `ims-lti` / JWT      |
| Base de Datos           | PostgreSQL                        |
| Almacenamiento archivos | Amazon S3, local con NGINX        |

---

¿Te gustaría que estos requisitos se conviertan en una tabla estructurada o documento técnico para usar en planificación o arquitectura?
