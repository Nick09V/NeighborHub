# NeighborHub

## 📱 Descripción del Proyecto

NeighborHub es una aplicación móvil diseñada especialmente para **tienderos de barrio**, facilitando la gestión de su catálogo de productos y el proceso de compras de sus clientes. Nuestra plataforma conecta a los comerciantes locales con los vecinos del barrio, haciendo que comprar y vender productos sea fácil y eficiente, apoyando la economía local y la comodidad de todos.

### Características Principales
- Gestión de catálogo de productos
- Sistema de compras integrado
- Conexión entre tienderos y clientes locales
- Herramientas de administración para comerciantes
- Interfaz móvil intuitiva y fácil de usar

---

## 👥 Equipo de Desarrollo

### Frontend y Diseño UI/UX
- Alejandro Minda
- Nick Valverde

### Backend
- Bryan Salazar

### Scrum master - Project Management
- Nick Valverde

### Database Administrator and QA
- Jonatan Claudio

---

## 🛠️ Tecnologías

### Frontend
- **React Native** - Framework para desarrollo móvil multiplataforma

### Backend
- **Python** - Lenguaje de programación
- **FastAPI** - Framework web moderno y de alto rendimiento

### Base de Datos
- **Supabase** - Backend as a Service (BaaS) con PostgreSQL

### Hosting
- **Render** - Plataforma de hosting para aplicaciones web

---

## 🏗️ Arquitectura Cliente-Servidor

```
┌───────────────────────────────────────────────────────────┐
│                         CLIENTE                           │
│  ┌────────────────────────────────────────────────────┐   │
│  │          Aplicación Móvil (React Native)           │   │
│  │  ┌──────────────┐  ┌──────────────┐  ┌──────────┐ │    │
│  │  │   UI/UX      │  │   Lógica de  │  │  Estado  │ │    │
│  │  │  Componentes │  │   Negocio    │  │  Global  │ │    │
│  │  └──────────────┘  └──────────────┘  └──────────┘ │    │
│  └────────────────────────────────────────────────────┘   │
└───────────────────────────────────────────────────────────┘
                              ↕ HTTP/HTTPS (REST API)
┌────────────────────────────────────────────────────────────┐
│                         SERVIDOR                           │
│  ┌────────────────────────────────────────────────────┐    │
│  │            API Backend (FastAPI + Python)          │    │
│  │  ┌──────────────┐  ┌──────────────┐  ┌──────────┐ │     │
│  │  │  Endpoints   │  │  Middleware  │  │  Modelos │ │     │
│  │  │  REST API    │  │  Auth/Valid. │  │  Datos   │ │     │
│  │  └──────────────┘  └──────────────┘  └──────────┘ │     │
│  └────────────────────────────────────────────────────┘    │
│                              ↕                             │
│  ┌────────────────────────────────────────────────────┐    │
│  │          Base de Datos (Supabase)                  │    │
│  │  ┌──────────────┐  ┌──────────────┐  ┌──────────┐ │     │
│  │  │  PostgreSQL  │  │     Auth     │  │  Storage │ │     │
│  │  │   Database   │  │   Service    │  │  Files   │ │     │
│  │  └──────────────┘  └──────────────┘  └──────────┘ │     │
│  └────────────────────────────────────────────────────┘    │
│                                                            │
│              Hosted on Render                              │
└────────────────────────────────────────────────────────────┘
```

### Flujo de Datos
1. **Cliente (App Móvil)**: Los usuarios interactúan con la interfaz de React Native
2. **API REST**: La aplicación se comunica con el backend a través de endpoints HTTP/HTTPS
3. **Servidor (FastAPI)**: Procesa las solicitudes, aplica lógica de negocio y valida datos
4. **Base de Datos (Supabase)**: Almacena y recupera información de productos, usuarios y transacciones

---

## 📁 Estructura del Proyecto

```
NeighborHub/
├── frontend/           # Aplicación móvil React Native
│   ├── src/
│   ├── assets/
│   ├── .env.example
│   └── package.json
│
├── backend/            # API FastAPI
│   ├── app/
│   ├── requirements.txt
│   └── .env.example
│
└── README.md
```

---

## 🚀 Comenzando

### Prerrequisitos
- Node.js y npm (para React Native)
- Python 3.8+ (para FastAPI)
- Cuenta en Supabase
- Cuenta en Render (para deployment)

### Instalación

Consulta los README específicos en cada carpeta:
- [Frontend Setup](./frontend/README.md)
- [Backend Setup](./backend/README.md)

---

## 📝 Licencia

Este proyecto está bajo desarrollo.
