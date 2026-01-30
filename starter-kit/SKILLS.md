---
name: project-starter
description: Analiza proyectos y explica cómo levantarlos. Usar cuando pregunten
  "cómo inicializo el proyecto", "setup", "cómo inicio", "qué necesito para levantar".
license: MIT
metadata:
  author: Deuna
  tags: starter-kit, init, start
---

# Project Starter

## Seguridad

**NUNCA leer:** `.env`, `*secret*`, `*credential*`, `*.key`, `*.pem`

**SÍ leer:** `.env.example`, archivos de config, `docker-compose.yml`

## Pasos

### 1. Detectar Ecosistema

| Archivo | Ecosistema |
|---------|------------|
| `package.json` | Node.js |
| `requirements.txt` / `pyproject.toml` | Python |
| `go.mod` | Go |
| `Cargo.toml` | Rust |
| `pubspec.yaml` | Flutter |
| `Gemfile` | Ruby |
| `pom.xml` / `build.gradle` | Java |
| `composer.json` | PHP |

### 2. Detectar Package Manager

| Lock file | Manager |
|-----------|---------|
| `pnpm-lock.yaml` | pnpm |
| `yarn.lock` | yarn |
| `bun.lockb` | bun |
| `package-lock.json` | npm |
| `poetry.lock` | poetry |
| `Pipfile.lock` | pipenv |

### 3. Detectar Framework

Lee dependencias y detecta frameworks (Next.js, Angular, Expo, NestJS, Django, FastAPI, Rails, etc.)

### 4. Detectar Servicios

Si existe `docker-compose.yml`, identifica: postgres, mysql, mongo, redis, etc.

### 5. Variables de Entorno

De `.env.example`: lista solo NOMBRES, agrupa por categoría.

### 6. Seeds/Mocks

Busca scripts: `seed`, `db:seed`, `migrate`, `setup`, `mock`

## Formato de Respuesta

```markdown
## 🚀 {nombre}

**Stack:** {tecnologías}
**Package Manager:** {pm}

### ⚡ Mínimo
{comandos para dev rápido sin servicios externos}

### 🔧 Completo
{comandos con todo: docker, migraciones, seeds}

### 📍 URLs
| Servicio | URL |
|----------|-----|

### 🧪 Datos de Prueba
{seeds si existen}

### 🛠 Scripts Útiles
| Comando | Descripción |
|---------|-------------|
```

 
