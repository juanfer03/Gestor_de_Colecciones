# Tech Stack

## Resumen

Stack principal: React + TypeScript en frontend, Firebase (Firestore, Auth, Hosting) como backend/persistencia, y CSS para estilos. Prioridad: simplicidad, facilidad de aprendizaje y despliegue rápido.

## Componentes principales

- Frontend: React + TypeScript
  - Estado local: React `useState` / `useReducer` y `Context` para scopes simples.
  - Ruteo: `react-router`.
  - Forms: `react-hook-form` (opcional) o formularios controlados.
  - Peticiones HTTP: `fetch` o `axios` para llamadas a APIs externas (Google Books).
- Estilos: CSS (preferible CSS Modules o BEM para escalabilidad). Evitar frameworks CSS pesados; si se desea, considerar `Tailwind` en fases posteriores.
- Backend / Persistencia: Firebase
  - Firestore: colecciones por usuario (`users/{userId}/books/{bookId}`).
  - Firebase Auth: Google, Email/Password.
  - Firebase Hosting: despliegue (CI/CD con GitHub Actions).

## Librerías de soporte recomendadas

- `i18next` para i18n (preparado aunque inicio en español).
- `date-fns` para manejo de fechas.
- `clsx` para composición de clases CSS.

## Testing

- Unit + integration: `Jest` + `React Testing Library`.
- E2E: `Playwright` o `Cypress` (preferencia: Playwright por su velocidad y soporte multi-browser).

## Calidad de código y CI

- Linter: `ESLint` con configuración TypeScript.
- Formateo: `Prettier`.
- Hooks Git: `husky` + `lint-staged` para formateo antes de commits.
- CI: `GitHub Actions` (lint → test → build → deploy a Firebase Hosting on `main`).

## Infraestructura y seguridad

- Variables de entorno: usar `.env.local` para configuración Firebase en desarrollo; `secrets` en GitHub Actions para despliegue.
- Reglas Firestore: reglas que aseguren que cada documento de `books` pertenece a su `userId` autenticado.
- Backup/Export: permitir exportar JSON/CSV del usuario para recuperación.

## Integraciones externas

- Google Books API para autocompletar metadatos.
- Analytics: Firebase Analytics u otra herramienta ligera para métricas (libros leídos por mes, uso activo).

## Notas y decisiones

- Empezamos con CSS simple y migramos a CSS Modules si el proyecto crece.
- Storage de portadas está fuera del MVP; soportamos solo URL externas inicialmente.
