# NeighborHub - Backend

API REST desarrollada con FastAPI y Python para gestionar el catálogo de productos y compras de tienderos de barrio.

## 🚀 Instalación

### Prerrequisitos
- Python 3.8 o superior
- pip (gestor de paquetes de Python)
- Cuenta en Supabase

### Configuración

1. Crea un entorno virtual:
```bash
python -m venv venv

# Activar en Windows
venv\Scripts\activate

# Activar en Linux/Mac
source venv/bin/activate
```

2. Instala las dependencias:
```bash
pip install -r requirements.txt
```

3. Copia el archivo de variables de entorno:
```bash
cp .env.example .env
```

4. Configura las variables de entorno en `.env` con tus credenciales de Supabase y configuración de base de datos.

### Ejecución

#### Modo desarrollo
```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

La API estará disponible en: `http://localhost:8000`

#### Documentación automática
- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

## 📁 Estructura

```
backend/
├── app/
│   ├── api/            # Endpoints de la API
│   │   ├── v1/         # Versión 1 de la API
│   │   └── deps.py     # Dependencias compartidas
│   ├── core/           # Configuración core
│   │   ├── config.py   # Configuración de la aplicación
│   │   └── security.py # Autenticación y seguridad
│   ├── models/         # Modelos de base de datos
│   ├── schemas/        # Esquemas Pydantic (validación)
│   ├── services/       # Lógica de negocio
│   └── main.py         # Punto de entrada de la aplicación
├── requirements.txt    # Dependencias del proyecto
└── .env.example        # Ejemplo de variables de entorno
```

## 🛠️ Tecnologías

- **FastAPI**: Framework web moderno y rápido
- **Pydantic**: Validación de datos
- **Supabase**: Backend as a Service con PostgreSQL
- **Uvicorn**: Servidor ASGI
- **Python-dotenv**: Gestión de variables de entorno

## 📋 Endpoints Principales

### Autenticación
- `POST /api/v1/auth/login` - Inicio de sesión
- `POST /api/v1/auth/register` - Registro de usuario

### Productos
- `GET /api/v1/products` - Listar productos
- `POST /api/v1/products` - Crear producto
- `GET /api/v1/products/{id}` - Obtener producto
- `PUT /api/v1/products/{id}` - Actualizar producto
- `DELETE /api/v1/products/{id}` - Eliminar producto

### Pedidos
- `GET /api/v1/orders` - Listar pedidos
- `POST /api/v1/orders` - Crear pedido
- `GET /api/v1/orders/{id}` - Obtener pedido

## 📝 Notas de Desarrollo

- Sigue las convenciones PEP 8 para Python
- Usa type hints en todas las funciones
- Documenta los endpoints con docstrings
- Mantén la separación de capas (API, Services, Models)
