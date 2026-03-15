# Plan final y cronograma

## Objetivo del plan

Proveer un roadmap claro en tres fases (aprendizaje) con entregables, criterios de aceptación y estimaciones para guiar el desarrollo y la documentación continua.

## Resumen de fases

- Fase 1 (2 semanas): Documentación completa + maquetación HTML/CSS estática.
- Fase 2 (3 semanas): Integración con React + TypeScript; componentes y lógica con datos mock.
- Fase 3 (3 semanas): Integración con Firebase (Auth, Firestore), offline sync y despliegue.

Duración estimada total: ~8 semanas (ajustable).

## Hitos y entregables

- Hito 1 (fin Fase 1): `docs/` completados; `static_prototype/` con `index.html`, `styles.css` y páginas de ejemplo.
- Hito 2 (fin Fase 2): app React+TS con componentes `BookCard`, `Gallery`, `StarRating` y mock data; tests unitarios básicos.
- Hito 3 (fin Fase 3): app conectada a Firebase, autenticación y persistencia; CI/CD en `main` con deploy automático a Firebase Hosting.

## Tareas por fase (alto nivel)

- Fase 1:
  - Completar docs: `alcance`, `arquitectura`, `tech_stack`, `sistema_de_diseño`.
  - Crear `static_prototype/` con HTML/CSS responsive.
  - Revisar accesibilidad (Lighthouse/axe).
- Fase 2:
  - Inicializar proyecto React+TS (`create-react-app` o Vite).
  - Implementar estructura `src/` DDD.
  - Componentes UI y state local.
  - Tests unitarios y config de lint/format.
- Fase 3:
  - Configurar Firebase (proyecto, Auth, Firestore rules).
  - Implementar repositorios infra y sincronización offline.
  - Integración con Google Books API para autocompletar.
  - E2E tests y despliegue automático.

## Criterios de aceptación y calidad

- Cada entrega incluye pruebas mínimas: unitarias para `domain`, integración para `application` y checks de accesibilidad.
- Cobertura objetivo: >=70% al finalizar Fase 3.

## CI/CD y despliegue

- GitHub Actions pipeline: `push`/`pull_request` → lint & tests → build → deploy (solo `main`).
- Variables y secretos en GitHub Secrets; `firebase` CLI en Actions.

## Roles y responsabilidades

- Responsable de docs: mantener `docs/` actualizado y registrar cambios en `README.md` usando la plantilla `docs/plantillas/readme_update_template.md`.
- Responsable de merges/despliegue: propietario del repo o persona designada.

## Riesgos y mitigaciones

- Riesgo: conflictos offline → Mitigación: heurística `updatedAt` y notificación al usuario.
- Riesgo: datos incompletos desde Google Books → Mitigación: permitir edición manual de campos.

## Próximos pasos inmediatos

1. Crear prototipo estático en `static_prototype/` (Fase 1.3).
2. Inicializar repo React+TS (Fase 2.1) cuando prototipo aprobado.
