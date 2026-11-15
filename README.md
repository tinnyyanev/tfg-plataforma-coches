# Plataforma de comparación y evaluación del riesgo en la compra de vehículos de segunda mano en Europa

Trabajo Fin de Grado del Grado en Ingeniería Informática (Universidad de Alcalá).

Aplicación web que actúa como metabuscador de vehículos de segunda mano: reúne y normaliza anuncios de varios países europeos, permite compararlos con criterios ponderables, muestra un análisis de riesgo explicable y estima el coste total de compra o importación a España. La compraventa no se realiza en la aplicación: el usuario es redirigido al anuncio original. El sistema apoya la decisión de compra, pero no garantiza la seguridad de la operación.

La demostración utiliza un conjunto de datos simulado con anuncios de Alemania, Bulgaria, República Checa y España.

## Estado

Proyecto en fase inicial. De momento el repositorio solo contiene la estructura de carpetas y la configuración del entorno; todavía no hay funcionalidad implementada.

## Tecnologías previstas

| Área | Tecnología |
|---|---|
| Presentación | Next.js con TypeScript |
| API y lógica de negocio | Python, FastAPI y Pydantic |
| Base de datos | PostgreSQL, SQLAlchemy y Alembic |
| Despliegue | Docker y Docker Compose |
| Pruebas | Pytest, Vitest y Playwright |
| Integración continua | GitHub Actions |

La arquitectura es un monolito modular: Next.js es solo la capa de presentación y la API en FastAPI concentra la lógica de negocio. Las fuentes de anuncios se integran mediante el patrón Gateway, de modo que puedan intercambiarse fuentes reales y simuladas.

## Estructura del repositorio

| Carpeta | Contenido |
|---|---|
| `docs/` | Documentación de ingeniería y memoria. |
| `backend/` | API en FastAPI, módulos de negocio, adaptadores de fuentes, migraciones y pruebas. |
| `frontend/` | Aplicación Next.js y sus pruebas unitarias. |
| `e2e/` | Pruebas extremo a extremo con Playwright. |
| `data/` | Conjunto de datos de demostración y su documentación. |
| `infra/` | Docker, Docker Compose y despliegue. |
| `scripts/` | Utilidades de desarrollo. |
