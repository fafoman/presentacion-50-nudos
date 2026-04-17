# Prompt 1 — Ajuste de marca y colores

Lee BRAND.md — contiene los colores reales de ambas marcas extraídos de sus sitios web.

## Problema actual
La presentación no refleja la identidad de marca real de ninguna de las dos empresas. Los colores son genéricos.

## Colores reales

**Torres Guarín** es AZUL (no verde):
- Navy script: `#2c3c5b`
- Azul principal: `#08a8e0`
- Cyan: `#00b0e0`

**Seguros Bolívar** es VERDE:
- Verde principal: `#05794a`
- Teal: `#00b889`
- Dorado: `#ffd543`

## Qué cambiar

1. **Fondo oscuro principal:** `#0c1a2e` — un navy profundo que es territorio neutro entre el azul TG y el verde SB

2. **Fondo claro (slides alternos):** `#f0f4f2` — crema neutra, sin sesgo hacia ninguna marca

3. **Acento de datos/métricas:** NO usar un solo color. Usar un gradient o alternar:
   - En slides compartidos: blanco o gold para números
   - En slides de Ruta 1: acento `#08a8e0` (azul TG)
   - En slides de Ruta 2: acento `#00b889` (teal SB)

4. **Gold del premio:** `#ffd543` — neutral, del crucero, no de ninguna marca

5. **Logos:** Hay archivos PNG/SVG en `logos/` (o `public/assets/`):
   - `logo-torres-guarin.png` — logo completo con badge 50 años
   - `logo-seguros-bolivar.png` — logo oficial con isotipo
   - `logo-seguros-bolivar-white.svg` — versión blanca para fondos oscuros
   - Usa `<img>` tags, NO texto como fallback. Los logos deben ser imágenes reales.
   - Ambos logos MISMO TAMAÑO visual. Ni uno más grande que el otro.

6. **Tipografía:** Verifica:
   - Playfair Display para títulos (serif, dramática)
   - DM Sans para body
   - JetBrains Mono para TODOS los números
   - Google Fonts CDN:
   ```html
   <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
   ```

## Regla fundamental
Ninguna marca debe dominar visualmente. Si alguien de Seguros Bolívar ve la presentación, no debe sentir que es "de Torres Guarín". Si alguien de Torres Guarín la ve, no debe sentir que es "de Seguros Bolívar". El protagonista es el concurso: **50 Nudos**.
