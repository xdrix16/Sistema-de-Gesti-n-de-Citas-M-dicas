# 🏥 MedConnect — Sistema de Gestión de Citas Médicas

## 📌 1. Descripción General
**MedConnect** es una solución digital y plataforma web diseñada para la programación, consulta y gestión integral de citas médicas, optimizando la comunicación entre pacientes, médicos y centros de salud.

## 🎯 2. Objetivo del Proyecto
Desarrollar un sistema centralizado e intuitivo que automatice la reserva de citas médicas, reduzca los tiempos de espera en centros de salud y proporcione una gestión eficiente de expedientes y horarios médicos.

## 🛠️ 3. Problema que Resuelve
* Largas filas y tiempos de espera en recepción para la programación de citas.
* Ineficiencia en la gestión de disponibilidad de horarios para los especialistas.
* Falta de un historial accesible y notificaciones de confirmación para los pacientes.

## ✨ 4. Funcionalidades Principales
1. **Autenticación y Perfiles:** Registro e inicio de sesión seguro para pacientes y personal médico.
2. **Gestión de Médicos y Especialidades:** Catálogo dinámico de profesionales de la salud.
3. **Reserva y Programación de Citas:** Selección de especialidad, médico, fecha y hora disponible.
4. **Gestión de Horarios:** Configuración de la agenda médica y disponibilidad.
5. **Notificaciones y Recordatorios:** Confirmación de citas programadas e historial del paciente.

## 🏗️ 5. Arquitectura del Sistema
El sistema utiliza una arquitectura basada en **Servicios / Cliente-Servidor Desacoplado**:
* **Patrón ArquITECTÓNICO:** MVC (Modelo-Vista-Controlador) para la separación limpia de capas.
* **Modelo de Comunicación:** API REST mediante peticiones HTTP/HTTPS con respuestas estructuradas en `JSON`.

---

## 💻 6. Organización Frontend y Backend

### 🌐 Frontend (Interfaz de Usuario)
* **Responsabilidad:** Presentación visual, captura de eventos, interacción intuitiva con pacientes/médicos y renderizado de formularios de reserva.
* **Tecnologías:** HTML5, CSS3, JavaScript / Figma (Diseño UI/UX).
* **Flujo:** Renderiza vistas (`Login`, `Registro`, `Catálogo de Médicos`, `Reserva de Citas`, `Mis Citas`) y solicita o envía información a la API.

### ⚙️ Backend (Servidor y Lógica de Negocio)
* **Responsabilidad:** Procesamiento de lógica de negocio, autenticación, validación de cruces de horarios, notificaciones y gestión de base de datos.
* **Tecnologías:** Node.js / Express (o Java Spring Boot) y Base de Datos Relacional (MySQL / PostgreSQL).
* **Flujo:** Recibe peticiones HTTP, ejecuta validaciones de disponibilidad, interactúa con la base de datos y retorna respuestas estructuradas en `JSON`.

### 🔄 Comunicación Frontend - Backend
1. El **Frontend** realiza solicitudes asíncronas (`FETCH` / `AXIOS`) a los endpoints del **Backend** (ej. `GET /api/medicos`, `POST /api/citas/reservar`).
2. El **Backend** procesa la solicitud, verifica que la fecha y hora no estén duplicadas en la base de datos.
3. El **Backend** responde con un código de estado (ej. `200 OK`, `400 Bad Request`) y los datos correspondientes.
4. El **Frontend** actualiza la interfaz mostrando la confirmación de la cita en tiempo real.

---

## 🧰 7. Herramientas Utilizadas
* **Diseño UI/UX:** Figma
* **Modelado UML y Arquitectura:** Visual Paradigm Online
* **Control de Versiones y Gestión:** Git, GitHub, GitHub Projects & Issues
* **Documentación:** Microsoft Word, Markdown

---

## 📊 8. Estado Actual del Proyecto
* **Fase Actual:** Cierre Técnico y Versión Inicial Controlada (v1.0.0).
* **Base de Datos:** Modelo entidad-relación y estructura relacional diseñada.
* **Modelado Técnico:** Casos de uso, diagramas de secuencias y arquitecturas documentadas.
