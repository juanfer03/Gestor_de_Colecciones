# Alcance del proyecto

## Propósito

Aplicación web para que usuarios gestionen su colección de libros: marcar por leer / leídos y puntuar con estrellas. Soporte multiusuario con autenticación Google/Email.

## Público objetivo

- Lectores que desean llevar un registro personal de su biblioteca y progreso de lectura.

## MVP (funcionalidades mínimas)

- Registro e inicio de sesión (Google, Email).
- Crear/editar/eliminar libros (título, autores, cover URL, notas, etiquetas).
- Visualizar galería tipo biblioteca con tarjetas de libro.
- Cambiar estado del libro (TO_READ, READING, READ).
- Puntuación con estrellas (0-5) y filtrado por puntuación.
- Búsqueda básica y filtros (autor, etiqueta, puntuación, fecha).
- Importar/exportar datos en JSON/CSV.

## Requisitos no funcionales

- Idioma: Español (i18n preparado para futuro).
- Accesibilidad objetivo: WCAG 2.1 AA.
- Soporte offline con sincronización posterior.
- Deploy automático en `main` a Firebase Hosting.
- Tests: cobertura mínima configurada (por defecto 70%).

## Restricciones

- Portadas: solo URLs externas (no upload inicial).

## Métricas de éxito

- Tiempo de carga de la galería < 1s en conexiones típicas.
- Feature complete del MVP en la Fase 3.
- > =70% de cobertura de tests al finalizar Fase 3.

## Entregables por Fase (ver también docs/fase_1_maquetacion.md)

- Fase 1: docs completos y maquetación HTML/CSS estática.
- Fase 2: app React+TS con componentes y datos mock.
- Fase 3: integración con Firebase (persistencia y auth).

## Aceptación

- Cada característica listada en MVP tiene criterios de aceptación en el documento técnico correspondiente (usar plantilla en `docs/plantillas/documento_template.md`).
