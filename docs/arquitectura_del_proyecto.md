# Arquitectura del proyecto (visión DDD)

## Capas y responsabilidades

- `domain/`: Entidades, Value Objects y reglas de negocio puras. No depende de infra.
- `application/`: Casos de uso (orquestan el dominio y las interfaces de repositorio).
- `infrastructure/`: Implementaciones concretas (Firebase, adaptadores de repositorio, almacenamiento).
- `presentation/`: UI (React), componentes y hooks. Depende de `application` a través de interfaces.

## Entidades principales

- `Book`:
  - `id: string`
  - `title: string`
  - `authors: string[]`
  - `coverUrl?: string`
  - `status: TO_READ | READING | READ`
  - `rating: number (0-5)`
  - `tags: string[]`
  - `notes?: string`
  - `createdAt: string` `updatedAt: string`

## Repositorios / Contratos

- `IBookRepository` (interfaz en `domain`): `add(book)`, `update(book)`, `delete(id)`, `findById(id)`, `find(query)`.

## Infraestructura: Firebase

- Firestore collections: `users/{userId}/books/{bookId}`.
- Auth: Firebase Auth (Google, Email).
- Storage: no usado inicialmente (covers via URL). Opcional más adelante.
- Reglas de security: cada documento de libro solo accesible por su `userId`.

## Flujo de datos (ej. añadir un libro)

1. UI (`presentation`) envía comando al caso de uso `AddBook`.
2. `AddBook` valida datos y crea entidad `Book`.
3. `AddBook` usa `IBookRepository` para persistir (infra implementa con Firestore).
4. UI observa cambios (listener) o actualiza estado tras respuesta.

## Offline y sincronización

- Usar Firestore offline persistence + colas locales para sincronizar cambios pendientes.
- Resolver conflictos por última modificación (`updatedAt`) y avisar al usuario en caso de colisión.

## Testing strategy

- `domain`: tests unitarios puros sin mocks pesados.
- `application`: tests de integración con mocks de repositorio.
- `presentation`: tests de componentes con React Testing Library.
- E2E: Playwright o Cypress en Fase 3.

## Diagramas

- Añadir diagramas de componentes y flujo de datos (usar herramientas externas y enlazar aquí).

## Notas de implementación

- Mantener `domain` libre de dependencias externas.
- Interfaces pequeñas y explícitas para facilitar testing y cambios de infra.
