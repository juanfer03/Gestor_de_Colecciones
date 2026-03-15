# Sistema de Diseño

## Propósito

Definir las reglas visuales y componentes reutilizables para mantener coherencia y accesibilidad.

## Tokens de diseño

- Paleta (ejemplo):
  - Primario: #2B6CB0 (azul)
  - Secundario: #EDF2F7 (gris claro)
  - Accent: #ED8936 (naranja)
  - Texto principal: #1A202C
  - Fondo: #FFFFFF
- Tipografía:
  - Familia: `Inter`, `system-ui`, sans-serif.
  - Escalas: 16px base; headings 1.5x/1.25x/1.125x.
- Espaciado: sistema de 8px (8,16,24,32,...)

## Componentes (ejemplos y variantes)

- `BookCard`:
  - Elementos: portada (img), título, autores, estado, estrellas, botones (editar, cambiar estado).
  - Tamaños: pequeño (list), mediano (galería), grande (detalle).
  - Accesibilidad: imagen con `alt`, botones con `aria-label`, foco visible.
- `Gallery`:
  - Grid responsive: 1 columna (móvil), 2-3 columnas (tablet), 4+ columnas (desktop).
- `StarRating`:
  - Soporta selección por teclado y pantallas táctiles.
  - Valores enteros 0–5; aria-live para lectura del cambio.
- `Form` (Agregar/Editar): etiquetas visibles, `aria-invalid` y mensajes de error claros.

## Estilos y metodologías

- Organizar CSS con CSS Modules o BEM.
- Variables CSS (`:root`) para tokens (colores, espacios, tipografías).
- Mobile-first y responsive.

## Accesibilidad (WCAG 2.1 AA)

- Contraste de texto >= 4.5:1 para texto normal.
- Navegación completa por teclado (tabindex natural, controles focusables).
- Roles y atributos ARIA donde sea necesario.
- Controles táctiles con tamaño mínimo recomendado 44x44 px.

## Component Library / Figma

- Recomiendo mantener un archivo de diseño (Figma/Sketch) y exportar ejemplos de componentes. Documentar variantes y tokens en `docs/sistema_de_diseño.md`.

## Exportables

- CSS snippets para `BookCard`, `Gallery` y `StarRating` en la fase 1 (maquetación estática).
