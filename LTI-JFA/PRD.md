
# 📄 Documento de Requisitos de Producto (PRD)

## Sistema ATS (Applicant Tracking System) para entorno LTI

---

## 1. Introducción y Objetivos

El presente documento define los requisitos para el desarrollo de un sistema **ATS (Applicant Tracking System)** integrado a un entorno **LTI (Learning Tools Interoperability)**. El objetivo principal es facilitar la gestión eficiente de procesos de selección para organizaciones educativas o empresas con LMS, permitiendo el seguimiento completo de los candidatos desde la postulación hasta la contratación.

---

## 2. Stakeholders

| Rol                      | Descripción                                                                         |
| ------------------------ | ----------------------------------------------------------------------------------- |
| **Candidato**            | Persona que aplica a una vacante y desea seguimiento transparente.                  |
| **Reclutador**           | Profesional de RRHH encargado de publicar vacantes, evaluar y contactar candidatos. |
| **Administrador**        | Gestiona la configuración general del sistema, roles y permisos.                    |
| **Equipo de desarrollo** | Diseña e implementa la solución técnica.                                            |
| **LMS/LTI integrador**   | Provee la interoperabilidad con sistemas educativos o de formación.                 |

---

## 3. Historias de Usuario (Resumen)

1. **Como candidato**, quiero cargar mi CV y postular a una vacante desde el LMS para no duplicar esfuerzos.
2. **Como reclutador**, quiero publicar vacantes y visualizar los candidatos por estado para organizar mi flujo de selección.
3. **Como candidato**, quiero recibir notificaciones automáticas para saber el estado de mi postulación.
4. **Como reclutador**, quiero mover candidatos entre etapas del proceso y registrar comentarios para tomar decisiones informadas.
5. **Como administrador**, quiero controlar los permisos y roles de usuarios para asegurar el acceso adecuado a cada módulo.

---

## 4. Componentes Principales y Sitemap

### Componentes Principales:

* Módulo de Vacantes
* Módulo de Postulación
* Gestión de Pipeline
* Evaluaciones y Feedback
* Reportes y Métricas
* Integración LTI/LMS
* Gestión de Usuarios

### Sitemap Simplificado:

```
[Inicio]
 ├── Ver Vacantes
 ├── Postularme
 ├── Mi Perfil
 └── Panel del Reclutador
      ├── Crear Vacante
      ├── Ver Candidatos
      ├── Evaluaciones
      ├── Reportes
      └── Configuración
```

---

## 5. Características y Funcionalidades

Ordenadas por prioridad:

1. 📥 **Centralización de postulaciones** con formularios integrados LTI.
2. 🗂️ **Gestión de pipeline** con etapas personalizadas (drag-and-drop).
3. 🔍 **Filtros inteligentes** por habilidades, experiencia y ubicación.
4. 📝 **Evaluaciones estructuradas** y comentarios colaborativos.
5. ✉️ **Notificaciones automatizadas** y plantillas personalizadas.
6. 📊 **Reportes y métricas** sobre eficiencia del proceso.
7. ✅ **Cumplimiento legal (GDPR/local)** y trazabilidad.
8. 🔌 **Integración con LMS y otras herramientas** (firmas, calendarios).
9. 🧑‍🤝‍🧑 **Gestión de usuarios y roles**.

---

## 6. Diseño y Experiencia del Usuario

* **Candidato**: interfaz limpia y responsiva, formularios simples, seguimiento visual de su aplicación.
* **Reclutador**: panel tipo Kanban para pipeline, buscador avanzado, reportes visuales.
* **UX universal**: accesible en móvil y escritorio, flujos sin fricción, mensajes claros y oportunos.

---

## 7. Requisitos Técnicos

* **Frontend**: React / Vue (SPA)
* **Backend**: Django REST / Node.js
* **Base de Datos**: PostgreSQL
* **Integración LTI**: soporte LTI 1.3 con OAuth2 + JWT
* **Autenticación**: SSO con LMS o autenticación propia con roles
* **Notificaciones**: SMTP / SendGrid
* **Infraestructura**: Docker + CI/CD + despliegue en nube (AWS/Azure)

---

## 8. Planificación del Proyecto

| Fase                              | Duración Estimada | Actividades Principales                 |
| --------------------------------- | ----------------- | --------------------------------------- |
| 1. Descubrimiento y diseño        | 2 semanas         | Análisis de requisitos, wireframes, UX  |
| 2. Desarrollo MVP                 | 4 semanas         | Back y front de vacantes, postulaciones |
| 3. Integración LTI + Evaluaciones | 3 semanas         | Autenticación LMS, feedback técnico     |
| 4. Reportes y analítica           | 2 semanas         | Métricas, exportaciones                 |
| 5. QA y pruebas piloto            | 2 semanas         | Pruebas funcionales y de carga          |
| 6. Despliegue y soporte           | 1 semana          | Documentación y capacitación            |

---

## 9. Criterios de Aceptación

* ✅ Publicación de vacantes operativa
* ✅ Postulación desde LMS sin errores
* ✅ Flujo de selección funcional y visible
* ✅ Reportes descargables en Excel/PDF
* ✅ Cumplimiento básico de privacidad de datos
* ✅ Integración con al menos un LMS LTI

---

## 10. Apéndices y Recursos Adicionales

* 📘 Diagrama de casos de uso UML (ver documento original)
* 📄 Diagrama de entidad-relación (ERD) del modelo de datos
* 🔗 Referencias de sistemas ATS existentes (OpenCATS, Greenhouse, Lever…)
* 🧠 Glosario de términos técnicos (ATS, LTI, LMS, pipeline, GDPR, etc.)

---
