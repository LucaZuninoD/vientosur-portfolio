# VientoSur — Plataforma de Reclutamiento con IA

> Plataforma de reclutamiento y ATS con matching semántico por IA
> Empezó como tesis de Ingeniería en Sistemas · Hoy en lanzamiento comercial en Patagonia Argentina

[![Stack](https://img.shields.io/badge/Stack-Spring%20Boot%20%7C%20Angular%2019%20%7C%20PostgreSQL-667eea)](https://github.com/LucaZuninoD/vientosur-portfolio)
[![AI](https://img.shields.io/badge/IA-Cohere%20%7C%20pgvector-764ba2)](https://cohere.com)
[![Status](https://img.shields.io/badge/Status-Lanzamiento%20Comercial-28a745)]()

---

## Página del proyecto

**→ [Ver el portfolio completo](https://vientosur-portfolio.vercel.app/)**

> Si estás viendo este repo localmente, abrí `index.html` directamente en tu navegador.

---

## ¿Qué es esto?

VientoSur es una plataforma fullstack de reclutamiento y bolsa de trabajo con inteligencia artificial que conecta postulantes, empresas y reclutadores freelance mediante matching semántico, parseo automático de CV, mensajería en tiempo real, gestión de eventos y un ATS (Applicant Tracking System) completo con pipeline Kanban.

Empezó como mi proyecto final de tesis en Ingeniería en Sistemas y hoy avanza hacia el lanzamiento comercial para PyMEs, consultoras de RRHH y postulantes de la Patagonia argentina.

> El código fuente y el entorno productivo son privados — VientoSur está incorporando clientes reales. Este repo contiene únicamente la presentación de portfolio. Escribime si querés una demo guiada.

---

## Stack Tecnológico

| Capa | Tecnologías |
|---|---|
| Backend | Java 21, Spring Boot 3.2.4, Spring Security (JWT access + refresh), Apache PDFBox / Tika / iText, AWS SDK, Google Calendar API |
| Frontend | Angular 19 (componentes standalone + SSR), TypeScript 5.7, Bootstrap 5 + SCSS, ng-bootstrap, FullCalendar |
| Base de datos | PostgreSQL 17 + pgvector (búsqueda por similitud coseno, score de afinidad cacheado) |
| IA | Cohere API — embeddings multilingües + chat LLM (command-r7b) |
| Storage | AWS S3 — CVs, fotos de perfil, logos, adjuntos de chat (vía URLs firmadas) |
| Infraestructura | Docker + Compose (db / backend / frontend), Nginx |

---

## Funcionalidades clave

- **Matching semántico** — Embeddings de perfiles y ofertas vía Cohere, comparados por similitud coseno en pgvector, cacheados por par
- **Parseo automático de CV** — PDF a perfil estructurado usando PDFBox, Tika e iText
- **ATS con pipeline Kanban** — Etapas y sub-estados configurables, plantillas por categoría, acciones masivas
- **Chatbot diferenciado por rol** — Handlers por estrategia según rol, clasificación de intención, base de conocimiento
- **Gestión de entrevistas** — Sincronización con Google Calendar + recordatorios automáticos por email
- **Contenido asistido por IA** — Generación de cartas de presentación, sugerencias de optimización de ofertas
- **Mensajería en tiempo real** — Chat directo empresa-candidato con adjuntos
- **Seguridad de nivel empresarial** — JWT, RBAC en 4 roles, URLs firmadas de S3
- **Feed de actividad y timeline** — Trazabilidad completa de la actividad de reclutamiento por oferta

---

## Sobre las capturas de pantalla

La interfaz de VientoSur cambia con cada iteración, así que en lugar de mantener capturas estáticas que se desactualizan, esta página ofrece coordinar una demo guiada en vivo o compartir una grabación actualizada de la plataforma real.

---

## Contacto

**Luca Zunino** — Founder & Lead Engineer, VientoSur · Full-Stack Developer
lucazuninod@gmail.com
[LinkedIn](https://www.linkedin.com/in/lucazuninod/)
