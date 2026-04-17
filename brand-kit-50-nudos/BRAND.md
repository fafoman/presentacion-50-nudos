# BRAND.md — Identidad de Marca Real

## Seguros Bolívar
**Logo:** `logos/logo-seguros-bolivar.png` (600×315, fondo transparente) y `logos/logo-seguros-bolivar-white.svg` (SVG blanco para fondos oscuros)

| Color | Hex | Uso |
|-------|-----|-----|
| Verde primario | `#05794a` | Color principal, texto del logo |
| Verde oscuro | `#016d38` | Hover, estados activos |
| Verde medio | `#009056` | Botones, CTAs |
| Teal | `#00b889` | Elementos secundarios |
| Dorado | `#ffd543` | Títulos premium sobre oscuro |
| Dorado claro | `#ffe16f` | Highlights, badges |
| Negro | `#1b1b1b` | Texto principal |
| Fondo claro | `#f2f9f6` | Background con tinte verde |

## Torres Guarín
**Logo:** `logos/logo-torres-guarin.png` (con badge 50 años)

| Color | Hex | Uso |
|-------|-----|-----|
| Navy TG (script) | `#2c3c5b` | Texto caligráfico "Torres Guarín" |
| Azul TG | `#08a8e0` | "Asesores en Seguros", badge 50, estrella |
| Azul claro TG | `#80d0e8` | Tonos suaves, degradados |
| Cyan TG | `#00b0e0` | Acentos brillantes |

## Paleta neutra para 50 Nudos

TG = azul, SB = verde. Son complementarios naturales. El gold es neutral (del premio).

```css
:root {
  /* Fondos */
  --bg-dark: #0c1a2e;         /* Navy profundo — territorio neutro */
  --bg-light: #f0f4f2;        /* Crema neutra — ni verde ni azul */

  /* Marca TG */
  --tg-navy: #2c3c5b;         /* Script del logo */
  --tg-blue: #08a8e0;         /* Azul principal TG */
  --tg-cyan: #00b0e0;         /* Acento TG */

  /* Marca SB */
  --sb-green: #05794a;        /* Verde principal SB */
  --sb-teal: #00b889;         /* Teal SB */

  /* Neutro — Premio */
  --gold: #ffd543;            /* Dorado del crucero */
  --gold-light: #ffe16f;      /* Dorado suave */

  /* Texto */
  --text-dark: #1b1b1b;
  --text-gray: #6b7280;
  --text-light: #f0f4f8;
}
```

### Regla de uso
- Slides compartidos (portada, premio, timeline, cierre): navy + gold, ambos logos iguales
- Slides Ruta 1 (Magisterio): puede tener acento TG blue `#08a8e0`
- Slides Ruta 2 (SENA-UNAD): puede tener acento SB teal `#00b889`
- Los datos/números: blancos o gold, nunca en el color de una sola marca
- Progress bars: gradient neutro o gold
