# CuentasClaras — Landing de Ventas

## 1. Proyecto
- **Nombre:** CuentasClaras — Landing de Ventas
- **Producto:** Kit de Presupuesto 50/30/20 (App Web + Google Sheets), USD 12 (precio de lanzamiento, tachado USD 17)
- **URL producción:** https://cuentas-claras-landing-phi.vercel.app
- **Repo:** https://github.com/diazsergio63/cuentas-claras-landing

## 2. Stack
- HTML/CSS/JS puro, single file (`landing.html`)
- Sin frameworks ni dependencias externas
- Google Fonts (Poppins) como única dependencia externa
- Favicon: `favicon.svg` en la raíz

## 3. Deploy
- **Plataforma:** Vercel (NO Netlify — Netlify es solo para la app)
- Auto-deploy desde GitHub rama `main`
- **Archivo local:** `C:\Users\diazs\OneDrive\Escritorio\Workspace\cuentas-claras-landing\landing.html`
- **Redeploy manual:** `vercel --prod --yes`
- `vercel.json` reescribe `/` → `/landing.html`

## 4. Identidad visual
- Verde oscuro: `#1A7A4A`
- Verde medio: `#2D9E6B`
- Dorado/acento: `#F5A623`
- Fuente: Poppins (Google Fonts)

## 5. Estructura de la landing (en orden)
Los comentarios `<!-- N. ... -->` de `landing.html` marcan cada sección.

| # | Sección | Selector principal |
|---|---------|--------------------|
| 1 | Hero | `header.hero` |
| 2 | El problema | `section.problem` |
| 3 | Las dos herramientas (+ carrusel de la Sheet) | `section.tools` (`.sheet-demo`) |
| 3b | Mockup de celular (carrusel de la app) | `section.phone-section` |
| 4 | Cómo funciona | `section.how` |
| 5 | ¿Para quién es? | `section.for-who` |
| 6 | El método 50/30/20 | `section.method` |
| 7 | Qué incluye el kit | `section.includes` |
| 8 | Precio y CTA final | `section.pricing` |
| 9 | Footer | `footer` |

Son las 9 secciones originales más la 3b (mockup de celular), agregada después.

## 6. Assets
- `favicon.svg` — ícono checkmark verde
- `screenshots/` — 4 capturas de la app (`inicio`, `movimientos`, `resumen`, `ajustes`, todas `.jpg`)
- `screenshots/sheet-*.jpg` — 3 capturas de Google Sheets (`sheet-ajustes`, `sheet-movimientos`, `sheet-resumen`)

## 7. Carruseles
- **Mockup celular** (`#carousel`): 4 slides, autoplay 2s, swipe táctil, flechas laterales
- **Sheet** (`#sheetScreen`): 3 slides (Ajustes → Movimientos → Resumen), mismo comportamiento
- Ambos usan la función `initCarousel()` unificada
- El autoplay se pausa con hover/touch y no arranca con `prefers-reduced-motion`

## 8. Links críticos
- Botones CTA (hero y sección de precio) → https://pay.hotmart.com/V108269135J
- App web: https://miscuentasclara.netlify.app
- Google Sheets /copy: https://docs.google.com/spreadsheets/d/1WU60peDMAkr4OJ-6JZbmt9P1YIcu6go1hXlPCGyRNRE/copy

Los links de la app web y de la Sheet no están en `landing.html` hoy; se entregan con el kit.

## 9. Cosas que NO tocar sin avisar
- Los `href` de los botones CTA (link de Hotmart)
- El orden de las slides de los carruseles
- `vercel.json`
- La carpeta `screenshots/`

## 10. Antes de cada sesión
- [ ] Leer este archivo
- [ ] Verificar que https://cuentas-claras-landing-phi.vercel.app responde 200
- [ ] Confirmar con el usuario qué sección se va a tocar
- [ ] No reescribir bloques completos — cambios puntuales
