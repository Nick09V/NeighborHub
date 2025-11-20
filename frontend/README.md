# NeighborHub - Frontend

Aplicación móvil desarrollada con React Native para tienderos de barrio y sus clientes.

## 🚀 Instalación

### Prerrequisitos
- Node.js (v16 o superior)
- npm o yarn
- React Native CLI
- Android Studio (para desarrollo Android)
- Xcode (para desarrollo iOS, solo macOS)

### Configuración

1. Instala las dependencias:
```bash
npm install
# o
yarn install
```

2. Copia el archivo de variables de entorno:
```bash
cp .env.example .env
```

3. Configura las variables de entorno en `.env` con tus credenciales de Supabase y la URL de tu API.

### Ejecución

#### Android
```bash
npm run android
# o
yarn android
```

#### iOS (solo macOS)
```bash
cd ios && pod install && cd ..
npm run ios
# o
yarn ios
```

## 📁 Estructura

```
frontend/
├── src/
│   ├── components/     # Componentes reutilizables
│   ├── screens/        # Pantallas de la aplicación
│   ├── navigation/     # Configuración de navegación
│   ├── services/       # Servicios de API
│   ├── utils/          # Utilidades y helpers
│   ├── hooks/          # Custom hooks
│   └── theme/          # Estilos y temas
├── assets/             # Imágenes, fuentes, etc.
└── .env.example        # Ejemplo de variables de entorno
```

## 🛠️ Tecnologías

- React Native
- React Navigation
- Axios (para peticiones HTTP)
- Supabase Client

## 📝 Notas de Desarrollo

- Sigue las convenciones de código del proyecto
- Usa componentes funcionales y hooks
- Mantén los componentes pequeños y reutilizables
