# Dulces Godoy — sitio web

Sitio de una página para Dulces Godoy (dulces caseros de Corrientes, desde 1954).
Construido con [Astro](https://astro.build), sin frameworks de UI — HTML/CSS/JS
plano para que sea fácil de mantener.

## Correrlo en tu máquina

```bash
npm install
npm run dev
```

Abre http://localhost:4321

## Compilarlo para producción

```bash
npm run build
```

Genera el sitio estático en `dist/` — son archivos HTML/CSS/JS que se pueden
subir a cualquier hosting (Vercel, Netlify, GitHub Pages, etc.).

## Subirlo a producción (recomendado: Vercel)

1. Subí esta carpeta a un repositorio de GitHub (ver más abajo).
2. Entrá a [vercel.com](https://vercel.com) con tu mail y conectá tu cuenta de GitHub.
3. "Import Project" → elegí este repositorio → Vercel detecta Astro automáticamente → "Deploy".
4. Te da una URL provisoria (`algo.vercel.app`). Para el dominio propio
   (`dulcesgodoy.com`, ya conectado) se agrega en Settings → Domains en Vercel,
   con los registros DNS cargados en Squarespace — esto ya está hecho.

### Subir esta carpeta a GitHub (si nunca lo hiciste)

```bash
git init
git add .
git commit -m "Sitio Dulces Godoy"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/dulces-godoy-web.git
git push -u origin main
```

(Creá el repositorio vacío primero en github.com/new)

## Analítica y verificación (Search Console, Analytics, Clarity, Meta Pixel)

Los 4 IDs van directo como constantes al principio de `src/pages/index.astro`
(no son datos secretos — quedan visibles en el código de cualquier sitio
publicado, así que no tiene sentido complicarlo con variables de entorno ni
tocar la configuración de Vercel). Cuando tengas un ID nuevo, pasámelo y lo
subo por GitHub como cualquier otro cambio — Vercel lo despliega solo.

Estado:

1. **Google Search Console** — ✅ verificado, por archivo HTML
   (`public/googleac11eb3488b5fad8.html`).
2. **Google Analytics 4** — ✅ cargado (`G-98NK5EN5Y2`).
3. **Microsoft Clarity** — pendiente. [clarity.microsoft.com](https://clarity.microsoft.com)
   → "Add new project" → nombre + `https://dulcesgodoy.com` → el **Project ID**
   está en la URL del proyecto que te crea.
4. **Meta Pixel** — pendiente. [business.facebook.com/events_manager](https://business.facebook.com/events_manager)
   (con la cuenta de Meta Business de @dulcescaserosgodoy) → "Conectar orígenes
   de datos" → "Web" → "Meta Pixel" → creá uno nuevo → el **Pixel ID** es el
   número que te muestra.

## Qué falta confirmar antes de considerarlo terminado

- Microsoft Clarity y Meta Pixel (punto anterior).
- Fotos por tamaño que todavía faltan: ver el punto "fotos que faltan" que
  se le pasó a Matías por chat — Guayaba no tiene ninguna foto real todavía;
  varios sabores faltan en 1,75kg.
- Costo/plazo real de envío a otras provincias (courier a usar).

## Estructura

```
src/pages/index.astro   → todo el sitio (una sola página)
public/images/          → logo real y fotos de producto (ya recortadas y sobre blanco)
```
