# 📝 Fullstack TODO

Aplicación **Full Stack de gestión de tareas** con autenticación de usuarios, API REST y operaciones CRUD sobre tareas.

El proyecto está diseñado para practicar y demostrar la integración entre **React, Node.js, Express y MongoDB**, implementando autenticación mediante **JWT** y seguridad básica con **bcrypt**.

---

## 🛠️ Stack Tecnológico

### Frontend
- **React**
- **Vite**
- **Tailwind CSS v4.3**

### Backend
- **Node.js**
- **Express.js**

### Base de Datos
- **MongoDB**
- **Mongoose**

### Autenticación y Seguridad
- **JWT (JSON Web Tokens)**
- **bcrypt**

### Arquitectura
- **API REST**
- Integración **Frontend ↔ Backend**
- Middleware para autenticación y protección de rutas

---

## 📋 Funcionalidades

### 🔐 Autenticación

- Registro de usuarios
  - Nombre
  - Email
  - Password
- Login
- Generación de JWT
- Protección de rutas privadas
- Logout

### 📊 Dashboard

- Visualización de las tareas del usuario autenticado.
- Acceso restringido mediante JWT.

### ✅ Gestión de tareas

Implementación completa de operaciones **CRUD**:

| Operación | Acción |
|---|---|
| **Create** | Crear una tarea |
| **Read** | Consultar tareas |
| **Update** | Actualizar una tarea |
| **Delete** | Eliminar una tarea |

---

## 🏗️ Arquitectura del Proyecto

```text
FULLSTACK TODO
│
├── frontend/
│   ├── React
│   ├── Vite
│   └── Tailwind CSS
│
└── backend/
    ├── Controllers
    ├── Models
    ├── Routes
    ├── Middleware
    ├── Config
    └── Server.js
```

---

## 🔄 Flujo de la Aplicación

```text
React
   │
   │ HTTP Request
   ▼
Express
   │
   ▼
Middleware
   │
   │ JWT Validation
   ▼
Controllers
   │
   ▼
Mongoose
   │
   ▼
MongoDB
```

---

## 🏷️ Tech Tags

```text
React
Vite
Tailwind CSS
Node.js
Express.js
MongoDB
Mongoose
JWT
bcrypt
REST API
CRUD
Middleware
Authentication
Frontend / Backend Integration
```

---

# ⚙️ Configuración y Desarrollo

## Paso 1 — Crear el Backend

```bash
mkdir backend
cd backend
```

---

## Paso 2 — Crear el Backend Mínimo

Configurar el proyecto de Node.js y preparar el servidor Express.

---

## Paso 3 — Crear el Primer Endpoint

Implementar el primer endpoint de prueba para verificar que el servidor responde correctamente.

---

## Paso 4 — Probar el Endpoint

Utilizar herramientas como **Postman** para comprobar las respuestas de la API.

---

## Paso 5 — Configurar MongoDB

Conectar el backend con **MongoDB** mediante **Mongoose**.

---

## Paso 6 — Crear el Modelo `User`

Definir el esquema de usuario:

```text
User
├── name
├── email
└── password
```

---

## Paso 7 — Implementar Registro

Crear el endpoint para registrar nuevos usuarios.

Proceso:

```text
Request
   ↓
Validación
   ↓
Hash de Password
   ↓
Guardar Usuario
   ↓
Response
```

La contraseña debe almacenarse utilizando **bcrypt**, nunca como texto plano.

---

## Paso 8 — Implementar Login + JWT

Crear el sistema de autenticación:

```text
Email + Password
        ↓
Validación
        ↓
JWT
        ↓
Cliente
```

El token será utilizado posteriormente para acceder a las rutas protegidas.

---

## Paso 9 — Crear el Modelo `Task`

Definir el esquema de tareas y su relación con el usuario autenticado.

```text
Task
├── title
├── description
├── completed
└── user
```

---

## Paso 10 — Implementar CRUD

Crear los endpoints REST para administrar tareas:

```text
POST    /api/tasks
GET     /api/tasks
GET     /api/tasks/:id
PUT     /api/tasks/:id
DELETE  /api/tasks/:id
```

Las operaciones deben estar protegidas mediante autenticación JWT.

---

## Paso 11 — Crear el Frontend

Inicializar el proyecto utilizando:

```text
React + Vite + Tailwind CSS
```

---

## Paso 12 — Conectar React → API

Integrar el frontend con el backend mediante solicitudes HTTP.

```text
React
  │
  ├── POST → Register
  ├── POST → Login
  ├── GET  → Tasks
  ├── POST → Create Task
  ├── PUT  → Update Task
  └── DELETE → Delete Task
```

---

## Paso 13 — Proteger el Dashboard

El dashboard solamente debe ser accesible cuando existe una sesión válida.

```text
Usuario
   ↓
Login
   ↓
JWT
   ↓
Protected Route
   ↓
Dashboard
```

---

## Paso 14 — Pulir la UI

Mejorar la experiencia visual y de usuario:

- Responsive Design
- Estados de loading
- Mensajes de error
- Validación de formularios
- Feedback visual
- Empty states
- Diseño consistente
- Componentes reutilizables

---

## Paso 15 — GitHub

Versionar y publicar el proyecto.

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin <repository-url>
git push -u origin main
```

---

# 🎯 Objetivo del Proyecto

Este proyecto tiene como objetivo demostrar conocimientos prácticos en:

```text
React
   ↓
HTTP
   ↓
Express
   ↓
Middleware
   ↓
JWT
   ↓
Mongoose
   ↓
MongoDB
   ↓
CRUD
   ↓
Seguridad básica
   ↓
Frontend / Backend Integration
```

> **Resultado esperado:** una aplicación Full Stack funcional donde los usuarios puedan registrarse, iniciar sesión y administrar sus propias tareas mediante una API REST protegida.
