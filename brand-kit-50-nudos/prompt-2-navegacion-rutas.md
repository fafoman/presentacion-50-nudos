# Prompt 2 — Navegación no-lineal por rutas

## El cambio
La presentación actual es lineal (slide 1 → 2 → 3... → 12). Necesito que sea **divergente**: después de la introducción, el usuario escoge Ruta 1 o Ruta 2, navega por esa ruta, y al final ambas convergen en los slides compartidos.

La metáfora náutica no debe ser solo decorativa — debe SER la navegación.

## Nueva estructura

```
COMPARTIDO (Inicio)
│
├─ Slide 1: Portada — "50 Nudos: Velocidad de Crucero"
├─ Slide 2: "Dos Rutas, Un Destino" — PUNTO DE BIFURCACIÓN
│      Aquí aparecen dos cards/botones grandes clickeables:
│      [🔵 Ruta 1: Magisterio]    [🟢 Ruta 2: SENA-UNAD]
│
├── RUTA 1 (azul TG) ──────────────────────────────────────
│   ├─ 1A: El Océano de Educadores (383.800 potencial, penetración 14%)
│   ├─ 1B: Coordenadas de Éxito (flow: origen → vehículo → puerto)
│   ├─ 1C: Metas de Recaudo (tabla mensual Dir. Ventas / Dir. Satélite)
│   └─ → Botón: "Ir al Puerto Final" (salta a slides compartidos)
│       + Botón secundario: "Ver Ruta 2" (salta a Ruta 2)
│
├── RUTA 2 (teal SB) ──────────────────────────────────────
│   ├─ 2A: Nuevos Horizontes (8 zonas autorizadas)
│   ├─ 2B: El Tamaño del Juego (tabla zonas con potencial y metas)
│   ├─ 2C: La Gran Brecha / Iceberg (261 vigentes vs 8.162 potencial)
│   ├─ 2D: Fórmula del Éxito (índice participación, barrera 30%)
│   └─ → Botón: "Ir al Puerto Final" (salta a slides compartidos)
│       + Botón secundario: "Ver Ruta 1" (salta a Ruta 1)
│
├── COMPARTIDO (Convergencia — "Puerto Final") ────────────
│   ├─ Slide F1: Timeline (mayo 2026 → febrero 2027 → crucero)
│   ├─ Slide F2: Niveles + Premios mensuales ($500K/$300K/$200K)
│   ├─ Slide F3: El Gran Premio — Crucero por el Caribe
│   └─ Slide F4: Cierre — "Nos vemos a bordo"
```

## Cómo implementar la navegación

### Opción recomendada: sistema de secciones con botones
- Mantener el sistema de slides pero agrupar en SECCIONES: `intro`, `ruta1`, `ruta2`, `final`
- El slide "Dos Rutas" tiene dos botones que llevan al primer slide de cada ruta
- Dentro de cada ruta, las flechas ← → navegan SOLO dentro de esa ruta
- Al final de cada ruta, un botón "Ir al Puerto Final" salta a la sección compartida
- Un botón opcional "Ver la otra ruta" permite cruzar

### Navegación inferior (nav bar)
- Mostrar en qué sección estás: `INICIO · RUTA 1 · RUTA 2 · PUERTO FINAL`
- Los dots de la nav bar se agrupan por sección
- Se puede clickear una sección para saltar a ella

### Estética por sección
- **Inicio:** Navy neutro + gold
- **Ruta 1:** Navy + acento azul TG (`#08a8e0`) — un sutil tinte azulado en las cards o borders
- **Ruta 2:** Navy + acento teal SB (`#00b889`) — un sutil tinte verde/teal en las cards o borders
- **Puerto Final:** Navy + gold — la convergencia

El cambio de acento debe ser SUTIL (color de borders, tags, progress bars) — no pintar toda la pantalla de azul o verde.

### El slide de bifurcación ("Dos Rutas")
Este slide es clave. Debe tener:
- Dos cards grandes, lado a lado, que se sientan como puertas/caminos a elegir
- Card izquierda: borde azul, "Ruta 1: Magisterio (Educadores)" con breve descripción
- Card derecha: borde teal, "Ruta 2: SENA — UNAD" con breve descripción
- Efecto hover que invite a clickear
- Cuando haces click, transición suave hacia el primer slide de esa ruta

### Keyboard navigation
- ← → navegan dentro de la sección actual
- Si estás en el último slide de una ruta y presionas →, vas al Puerto Final
- En el slide de bifurcación: 1 y 2 como atajos (presionar "1" → Ruta 1, "2" → Ruta 2)

## Lo que NO cambiar
- El contenido de cada slide se mantiene igual
- Las animaciones GSAP se mantienen
- La tipografía se mantiene
- Los datos del concurso se mantienen
