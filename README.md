# Photoless - Photography Portfolio Platform

Plataforma web para gestión y exhibición de fotografías construida con Astro.js y AWS.

## Arquitectura

- **Frontend**: Astro.js desplegado en AWS Amplify
- **Backend**: AWS Lambda + API Gateway
- **Storage**: S3 para imágenes, DynamoDB para metadatos
- **Auth**: AWS Cognito (opcional)

## Estructura del Proyecto

```
photoless/
├── frontend/          # Aplicación Astro.js
├── backend/           # Funciones Lambda
├── infrastructure/    # Terraform/CDK
└── docs/             # Documentación
```

## Plan de Desarrollo

### Fase 1: Configuración Base
- [ ] **1.1** Inicializar proyecto Astro.js con TypeScript
- [ ] **1.2** Configurar estructura de carpetas del backend
- [ ] **1.3** Setup inicial de infraestructura AWS (Terraform/CDK)
- [ ] **1.4** Configurar repositorio y CI/CD básico

### Fase 2: Backend Core
- [ ] **2.1** Crear tabla DynamoDB para metadatos de fotos
- [ ] **2.2** Configurar bucket S3 para almacenamiento de imágenes
- [ ] **2.3** Lambda para upload de imágenes (pre-signed URLs)
- [ ] **2.4** Lambda para CRUD de fotografías
- [ ] **2.5** API Gateway con endpoints REST

### Fase 3: Procesamiento de Imágenes
- [ ] **3.1** Lambda para redimensionado automático (thumbnails)
- [ ] **3.2** Optimización de imágenes (WebP conversion)
- [ ] **3.3** Extracción de metadatos EXIF
- [ ] **3.4** CloudFront para CDN de imágenes

### Fase 4: Frontend Base
- [ ] **4.1** Páginas principales (Home, Gallery, About)
- [ ] **4.2** Componente de galería responsive
- [ ] **4.3** Visor de imágenes con navegación
- [ ] **4.4** Integración con API backend
- [ ] **4.5** Optimización de carga (lazy loading)

### Fase 5: Gestión de Contenido
- [ ] **5.1** Implementar Cognito para autenticación admin
- [ ] **5.2** Panel de administración para upload
- [ ] **5.3** Gestión de álbumes/categorías
- [ ] **5.4** Edición de metadatos de fotos
- [ ] **5.5** Sistema de tags y búsqueda

### Fase 6: Optimización y Deploy
- [ ] **6.1** Configurar Amplify para deploy automático
- [ ] **6.2** Implementar caching strategies
- [ ] **6.3** Optimización SEO y meta tags
- [ ] **6.4** Testing y monitoring
- [ ] **6.5** Documentación final

## Tecnologías

### Frontend
- Astro.js 4.x
- TypeScript
- Tailwind CSS
- View Transitions API

### Backend
- Node.js 18+ (Lambda Runtime)
- AWS SDK v3
- Sharp (procesamiento de imágenes)

### Infraestructura
- AWS Lambda
- API Gateway
- S3 + CloudFront
- DynamoDB
- Cognito
- AWS Amplify

## Comandos Rápidos

```bash
# Desarrollo frontend
cd frontend && npm run dev

# Deploy infraestructura
cd infrastructure && terraform apply

# Deploy funciones Lambda
cd backend && npm run deploy
```

## Variables de Entorno

```env
# Frontend (.env)
PUBLIC_API_URL=
PUBLIC_CDN_URL=

# Backend
BUCKET_NAME=
DYNAMODB_TABLE=
COGNITO_USER_POOL_ID=
```

## Próximos Pasos

1. Ejecutar tarea **1.1** - Inicializar Astro.js
2. Configurar AWS credentials
3. Definir esquema de base de datos