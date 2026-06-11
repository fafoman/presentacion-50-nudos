# Instrucciones para Claude Code

Este proyecto es la **guía de consulta web** del concurso comercial "50 Nudos — Velocidad de Crucero" de Torres Guarín × Seguros Bolívar. Nació como presentación de slides para proyector y fue convertida en un documento scrolleable de referencia (header sticky con índice de secciones, scroll-spy, reveals on-scroll).

## Archivos importantes que debes leer ANTES de escribir código:

1. **PROMPT.md** — Instrucciones originales del contenido, sección por sección
2. **DESIGN.md** — Sistema de diseño con paleta, tipografía, componentes, y animaciones
3. **DATA.md** — Todos los datos del concurso (mercado, metas, zonas, premios)
4. **references/** — DESIGN.md de SpaceX, Lamborghini, y Apple como referencia estética

## Output esperado

Un solo archivo `public/index.html` con todo inline (CSS + JS + datos). Se despliega en Vercel como static site.

## Estructura de la guía

Secciones ancladas (ids): `#intro`, `#rutas`, `#ruta1`, `#ruta2`, `#final`, `#contactos`, `#cierre`. El atributo `data-section` de cada `<section>` alimenta el scroll-spy del header.

## Stack

- HTML/CSS/JS vanilla (NO frameworks, sin GSAP — IntersectionObserver + transiciones CSS)
- Google Fonts via CDN
- Responsive / mobile-first: breakpoints 560px, 768px, 1024px (los vendedores la consultan en el celular)
