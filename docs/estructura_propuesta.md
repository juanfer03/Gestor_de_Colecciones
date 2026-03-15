# Estructura de archivos propuesta

Raíz del proyecto (resumen):

- `docs/` — toda la documentación viva del proyecto.
- `public/` — assets estáticos para la app.
- `src/` — código fuente organizado por capas DDD.
- `README.md` — resumen del estado y links rápidos a `docs/`.
- `package.json`, `tsconfig.json`, `.firebaserc`, `firebase.json` — configuraciones.

Estructura `src/` recomendada:

- `src/domain/`
  - `book/` (entities, valueObjects, repository interface)
- `src/application/`
  - `useCases/` (addBook, changeStatus, rateBook, listBooks)
- `src/infrastructure/`
  - `firebase/` (implementación repositorios, adaptadores)
- `src/presentation/`
  - `components/` (BookCard, Gallery, StarRating)
  - `pages/`
  - `hooks/`
- `src/styles/`
- `src/assets/`
- `src/types/`

Notas:

- Mantener `domain` independiente de infra y presentation.
- No crear carpetas por fase; los documentos en `docs/` se actualizarán por fase.
