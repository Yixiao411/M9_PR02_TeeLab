# TeeLab - API de Camisetas y Comandas

API REST para la gestión de camisetas y comandas.

## Instrucciones de inicio

### 1. Instalar dependencias
```bash
npm i
```

### 2. Ejecutar en modo desarrollo
```bash
npm run dev
```

El servidor estará disponible en `http://localhost:3001/`

### 3. Ejecutar tests
```bash
npm test
```

Para ejecutar tests en modo watch:
```bash
npm run test:watch
```

---

## Endpoints

### Camisetas

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| GET | `/camisetas` | Obtener todas las camisetas |
| GET | `/camisetas/:id` | Obtener una camiseta por ID |

### Comandas

| Método | Endpoint | Descripción |
|--------|----------|-------------|
| GET | `/comandas` | Obtener todas las comandas |
| GET | `/comandas/:id` | Obtener una comanda por ID |
| POST | `/comandas` | Crear una nueva comanda |

---

## Tests

Los tests están implementados con **Jest** y **Supertest** y cubren los siguientes casos:

### POST /comandas
- ✅ Crear una comanda exitosamente
- ✅ Retornar 400 cuando camisetaId es inválido
- ✅ Retornar 400 cuando falta el nombre del cliente
- ✅ Retornar 400 cuando falta el email del cliente
- ✅ Retornar 400 cuando items está vacío

### GET /comandas/:id
- ✅ Retornar 404 cuando comanda no existe
- ✅ Retornar la comanda cuando existe

### GET /comandas
- ✅ Retornar todas las comandas creadas

---

## Tecnologías utilizadas

- **Express.js** - Framework web
- **CORS** - Middleware para compartir recursos entre orígenes
- **Nodemon** - Reinicio automático en desarrollo
- **Jest** - Framework de testing
- **Supertest** - Testing HTTP de APIs

