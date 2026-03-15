# Gestor de Colecciones — Estado y guía rápida

## Resumen rápido

Proyecto: aplicación web para gestionar libros (por leer / leídos) y puntuarlos.
Estado actual: Definición de documentación y plantillas; fase 1 (documentación y maquetación) próxima.

## Decisiones clave (resumen)

- Soporte: multiusuario. Autenticación: Google y Email. (Ver: docs/alcance_del_proyecto.md)
- Portadas: solo URLs externas.
- Notas: texto libre por libro.
- Filtros: por autor, etiqueta, puntuación, fecha.
- Autocompletado: integrar APIs externas (p. ej. Google Books).
- Soporte offline y sincronización posterior.
- Accesibilidad objetivo: WCAG 2.1 AA.
- Tests: cobertura mínima (configurable).
- Deploy: automático en `main` (Firebase Hosting).

## Links rápidos

- Alcance: [docs/alcance_del_proyecto.md](docs/alcance_del_proyecto.md)
- Sistema de diseño: [docs/sistema_de_diseño.md](docs/sistema_de_diseño.md)
- Tech stack: [docs/tech_stack.md](docs/tech_stack.md)
- Arquitectura: [docs/arquitectura_del_proyecto.md](docs/arquitectura_del_proyecto.md)
- Plantillas: [docs/plantillas/documento_template.md](docs/plantillas/documento_template.md)

## Formato obligatorio para actualizaciones rápidas

Usar la plantilla en `docs/plantillas/readme_update_template.md`. Cada cambio relevante del proyecto debe añadirse como una entrada breve en este README y enlazar al documento completo en `docs/`.

## Responsable de la actualización

Indicar en cada entrada quién realizó la actualización.
