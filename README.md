# Aim Lab G203 — sensiw4y

Página HTML autocontenida (sin build, sin dependencias) para encontrar tu mejor sensibilidad de mouse en **Sea of Thieves**, usando un Logitech G203 como referencia de hardware.

Tiene tres secciones, accesibles desde la barra superior:

## 1. Specs

Muestra los datos del mouse (polling rate, DPI, perfiles) y los 3 valores oficiales de sensibilidad que trae Sea of Thieves por defecto:

- **3.3** — precisión / largo alcance
- **5.0** — valor por defecto a mano alzada
- **7.0** — rápida, para combate cercano (trabuco)

Rare (el estudio) nunca publicó una fórmula de "grados por punto" como sí existe en Valorant o CS2, así que estos 3 valores oficiales son el único punto de referencia real que tenemos.

## 2. Calibrar

Es la parte principal: una prueba real de puntería, no una calculadora con regla de tres.

1. Apretas **Empezar prueba** y el cursor normal se esconde — aparece una mira dorada que se mueve con tu mouse.
2. Salen 4 blancos por ronda, uno a la vez. Los apuntas con la mira y haces click.
3. Son 3 rondas, una por cada sensibilidad oficial (3.3 / 5.0 / 7.0), con la velocidad de giro de la mira escalada proporcionalmente a cada valor.
4. Al terminar las 3 rondas, te muestra una tabla comparando precisión y tiempo de reacción promedio en cada una, y te dice cuál sensibilidad te rindió mejor — además de valores sugeridos para las sensibilidades de apuntado (trabuco/pistola y mosquete de largo alcance), en la misma proporción que usa el juego por defecto.

Puedes salir a mitad de la prueba cambiando de pestaña arriba.

## 3. Entrenar

Un rango de tiro libre de 30 segundos: aparecen blancos al azar y los clickeas lo más rápido y preciso posible, con el cursor normal (sin mira). Sirve para practicar reflejo y precisión general de mano. Guarda tu mejor porcentaje de precisión en el navegador (localStorage), para que lo veas la próxima vez que entres.

## Cómo instalarlo / usarlo

No necesita instalación ni servidor: es un solo archivo HTML.

```bash
git clone <url-de-este-repo>
cd sensiw4y
xdg-open index.html   # o simplemente abre index.html con doble click en tu navegador
```

También puedes publicarlo con GitHub Pages (Settings → Pages → Deploy from branch → `main` / raíz) si quieres una URL para abrirlo desde cualquier dispositivo sin clonar el repo.

**Requisitos:** un navegador moderno de escritorio con mouse (usa `mousemove`/`mousedown` directamente, no está pensado para pantalla táctil). Funciona sin conexión salvo por la tipografía, que se carga desde Google Fonts.
