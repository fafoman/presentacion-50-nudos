# PROMPT.md — Instrucciones para Claude Code

## Qué construir

Una presentación HTML interactiva single-file, optimizada para proyector 16:9.

**Nombre del concurso:** "50 Nudos — Velocidad de Crucero"
**Contexto:** Concurso comercial de Torres Guarín (intermediario de seguros, cumple 50 años) dirigido a la fuerza de ventas de Seguros Bolívar. El premio es un crucero por el Caribe. Se presenta en proyector frente a la fuerza de ventas.

## Antes de escribir código

1. Lee `DESIGN.md` completo — contiene la paleta, tipografía, componentes, y reglas de animación
2. Lee `DATA.md` completo — contiene todos los datos del concurso que van en la presentación
3. Respeta el lenguaje visual descrito: fusión náutica-premium de SpaceX (dramático oscuro) + Lamborghini (gold-on-black) + Apple (claridad informativa)

## Requisitos técnicos

- **Un solo archivo HTML** con CSS y JS inline (todo embebido)
- **Google Fonts** via CDN (ver DESIGN.md sección 9)
- **GSAP 3.12.5** via CDN para animaciones:
  - `https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js`
- **NO usar frameworks**: vanilla HTML/CSS/JS
- **NO usar reveal.js** ni ningún framework de presentaciones
- Output final: `public/index.html`

## Navegación

- Flechas del teclado (← →) para cambiar slides
- Click en cualquier parte también avanza
- Barra de navegación inferior: dots clickeables + contador tipo "3 / 12"
- Botones ‹ › a los lados de la nav bar
- Transición entre slides: fade + translateY (ver DESIGN.md sección 6)

## Arquitectura de Slides

### SLIDE 1 — Portada
- Fondo: navy gradient + grid overlay sutil + wave animation en la parte inferior
- Logo row centrado: `Torres Guarín | 50 | Seguros Bolívar` (igual prominencia)
- Título hero (Playfair 900): "50 Nudos"
- Tagline (DM Sans 300 italic): "Velocidad de Crucero"
- Subtítulo: "Un nudo es la velocidad en el mar. 50 nudos es velocidad de crucero. Y este año, cumplimos 50."
- Badge: "Concurso Comercial 2026–2027"
- Compass rose decorativo bottom-right, baja opacidad
- Nota pequeña bottom: "← → para navegar"

### SLIDE 2 — Dos Rutas, Un Destino
- Fondo: claro (cream warm)
- Título: "Dos Rutas de Navegación. Un Solo Destino." (con "Un Solo Destino" en accent color)
- Dos cards side-by-side:
  - **Ruta 1: Magisterio** — Territorio: zonas actuales | Tripulación: Dir. Ventas y Dir. Satélite | Métrica: recaudo mensual por libranza
  - **Ruta 2: SENA — UNAD** — Territorio: nuevos horizontes | Tripulación: Dir. Ventas y Asesores | Métrica: % participación del mercado
- Tag al fondo: "Mayo — Diciembre 2026"

### SLIDE 3 — El Océano de Educadores
- Fondo: navy gradient + grid overlay
- Tag: "Ruta 1"
- Título: "El Océano de Educadores" (Educadores en cyan)
- Subtítulo: "Potencial país: educadores, SENA y UNAD"
- Stat row con 3 números grandes:
  - 383.800 (Potencial País) — counter-up animation
  - 54.200 (Vigentes)
  - 329.600 (Vidas por Conquistar) — en gold
- Progress bar animada: 14.1% penetración actual (fill en cyan, track transparente)
- Labels: "Penetración actual: 14.1%" | "Mercado disponible: 85.9%"

### SLIDE 4 — Coordenadas de Éxito (Ruta 1)
- Fondo: navy
- Tag: "Ruta 1 — Metas de Recaudo"
- Título: "Coordenadas de Éxito" (Éxito en cyan)
- Flow visual horizontal con flechas:
  - ⚓ El Origen: "Crecimiento exclusivo en nuevos negocios. Solo productos de convenios Torres Guarín."
  - 🚢 El Vehículo: "Recaudo mensual garantizado. Todo nuevo negocio ingresa por libranza."
  - 🏝️ Llegada a Puerto: "Pólizas vigentes y recaudadas al corte: Febrero 2027."
- Tabla compacta de metas mensuales (datos en DATA.md)
- Nota: "*Agosto tiene meta reducida por estacionalidad"

### SLIDE 5 — Nuevos Horizontes (Ruta 2 — Zonas)
- Fondo: claro (cream)
- Tag: "Ruta 2"
- Título: "Explorando Nuevos Horizontes" (Nuevos Horizontes en accent)
- Subtítulo: "SENA — UNAD en territorios sin operación previa"
- 8 zone chips/badges en grid: Valle, Santander/Arauca, Bolívar, Risaralda/Quindío, Meta, N. Santander, Córdoba, Sucre
- Highlight box: "Solo participan Directores y Asesores asignados a estas localidades específicas."

### SLIDE 6 — El Tamaño del Juego
- Fondo: navy gradient
- Título: "El Tamaño del Juego" (en cyan)
- Subtítulo italic: "El mercado que estamos dejando sobre la mesa"
- Tabla visual con las 8 zonas: Depto | Total | Vigentes | Potencial | Meta/mes
- Usar los datos actualizados de DATA.md (sección Ruta 2)
- Totales destacados al final: 8.423 total | 261 vigentes | 8.162 potencial | $160M meta/mes
- Los números más impactantes deben ser grandes y animados

### SLIDE 7 — La Gran Brecha (Iceberg visual)
- Fondo: deep dark (#050d1a gradient)
- Título: "La Gran Brecha: SENA — UNAD" (SENA — UNAD en cyan)
- Split layout:
  - Izquierda: Visualización tipo iceberg
    - Punta visible: "261 pólizas vigentes" (pequeño, arriba del agua)
    - Línea del agua en cyan
    - Masa sumergida: "8.162 mercado potencial" (grande, debajo)
  - Derecha: 
    - "Penetración actual:" + número gigante "3.1%" en gold
    - Texto: "Una gran oportunidad de llegar con un solo producto a tantos clientes."

### SLIDE 8 — Fórmula del Éxito (Ruta 2)
- Fondo: claro (cream)
- Tag: "Ruta 2"
- Título: "La Fórmula Matemática del Éxito"
- Formula box prominente: "Índice de Participación = Asegurados Vigentes ÷ Mercado Potencial"
  - Border cyan, sutil pulse animation
- Dos cards:
  - 🔒 La Barrera de Entrada: "Mínimo 30% de participación para calificar"
  - 🏆 El Boleto al Caribe: "El índice más alto al cierre gana el viaje"

### SLIDE 9 — Timeline
- Fondo: navy gradient + grid
- Título: "La Línea de Tiempo Hacia el Triunfo" (Triunfo en cyan)
- Timeline horizontal con 4 nodos:
  1. Mayo 2026 (cyan dot) — "Zarpe — Inicio simultáneo"
  2. Mayo — Dic 2026 (dim dot) — "Alta Mar — Producción y crecimiento"
  3. Febrero 2027 (gold dot) — "Llegada a Puerto — Corte evaluación final"
  4. Crucero (gold star) — "Líder Ruta 1 + Líder Ruta 2"
- Línea: gradient de cyan a gold
- Highlight box: "Todas las ventas deben estar vigentes y recaudadas en la fecha de corte."

### SLIDE 10 — Niveles, Seguimiento e Incentivos
- Fondo: navy + grid
- Título: "Niveles, Seguimiento e Incentivos" (Incentivos en gold)
- 3 columnas con cards:
  - **Niveles:** Bronce → Plata → Oro → 💎 Diamante (= crucero)
  - **Seguimiento:** Corte mensual + premiación primeros 5 días + canales (WhatsApp, correo, plenarias)
  - **Bonos Mensuales:** Top 1: $500K | Top 2: $300K | Top 3: $200K — con ranking badges (gold, silver, bronze circles)

### SLIDE 11 — El Gran Premio
- Fondo: deep dark
- Título: "El Gran Premio" (en gold, Playfair 900 huge)
- Prize card con shimmer: 🚢 "Crucero por el Caribe — 2 ganadores con acompañante"
- Subtexto italic: "Más que un premio... una experiencia que te ganaste con resultados."
- Stat row: 392K+ oportunidades | 8 zonas | 8 meses de competencia

### SLIDE 12 — Cierre
- Fondo: navy gradient + wave animation bottom + compass rose
- Texto 1 (gold italic): "¡El esfuerzo se premia!"
- Texto 2: "Donde otros ven un destino... Tú ves el resultado de tu esfuerzo." (último fragmento en cyan)
- Glow line
- Texto 3: "No es suerte... es desempeño." (desempeño en gold)
- Texto 4 (grande): "El primer reto comienza AHORA." (AHORA en cyan)
- Texto 5: "Nos vemos a bordo. 🚢"
- Logo row final: Seguros Bolívar | Torres Guarín — Desde 1976

## Calidad visual esperada

- Esto NO es una presentación genérica. Es una pieza de comunicación que debe sentirse premium, aspiracional, y profesional.
- Cada slide debe poder funcionar como un poster por sí solo.
- Los números son los protagonistas — deben dominar cada slide donde aparezcan.
- El gold debe usarse con moderación — solo para el premio y momentos aspiracionales.
- El cyan es para datos, progreso, y elementos informativos.
- La alternancia dark/light evita fatiga visual.
- Las animaciones deben ser suaves y rápidas — no showoff, sino profesionales.

## Deployment

- El archivo final va en `public/index.html`
- Se despliega en Vercel como static site
- Verificar que funcione abriendo directamente el archivo .html en un navegador
