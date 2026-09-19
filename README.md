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
4. Te da una URL provisoria (`algo.vercel.app`). Para usar tu propio dominio
   (por ejemplo `dulces.tonuttigodoy.com`), andá a Settings → Domains en Vercel,
   agregá el dominio, y copiá el registro DNS que te muestra a donde administrás
   `tonuttigodoy.com`.

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

El código de las 4 integraciones ya está en `src/pages/index.astro`, apagado
por defecto. Cada una se enciende sola apenas le des el ID correspondiente
en un archivo `.env` (copiá `.env.example` a `.env`) o, una vez desplegado,
como variable de entorno en Vercel/Netlify. Ninguna requiere tocar código de
nuevo — solo pegar el valor.

Como crear cada cuenta y sacar el ID es algo que solo podés hacer vos (no
puedo crear cuentas ni loguearme por vos en estos servicios), acá está el
paso a paso de cada una. Cuando tengas los valores, pasámelos y los cargo.

1. **Google Search Console** — [search.google.com/search-console](https://search.google.com/search-console)
   → "Agregar propiedad" → tipo "Prefijo de URL" con la URL del sitio (una
   vez que esté publicado) → método de verificación "Etiqueta HTML" → copiá
   solo el valor del atributo `content` de la etiqueta que te muestra →
   `PUBLIC_GSC_VERIFICATION`.
2. **Google Analytics 4** — [analytics.google.com](https://analytics.google.com)
   → Admin → Crear propiedad (nombre "Dulces Godoy") → al crear el "flujo de
   datos" web te da un **Measurement ID** con formato `G-XXXXXXXXXX` →
   `PUBLIC_GA_MEASUREMENT_ID`.
3. **Microsoft Clarity** — [clarity.microsoft.com](https://clarity.microsoft.com)
   → "Add new project" → nombre + la URL del sitio → el **Project ID** es el
   código que aparece en la URL del proyecto (`clarity.microsoft.com/projects/view/XXXXXXXXXX`)
   → `PUBLIC_CLARITY_PROJECT_ID`.
4. **Meta Pixel** — [business.facebook.com/events_manager](https://business.facebook.com/events_manager)
   (con la cuenta de Meta Business que ya usan para @dulcescaserosgodoy) →
   "Conectar orígenes de datos" → "Web" → "Meta Pixel" → creá uno nuevo → el
   **Pixel ID** es el número que te muestra → `PUBLIC_META_PIXEL_ID`.

Nota sobre Search Console: la verificación (y que Google indexe algo) recién
tiene sentido una vez que el sitio esté en su dominio real — conviene hacer
este paso junto con el dominio/DNS (sección "Subirlo a producción" arriba),
no antes. Los otros tres podés cargarlos ya mismo si querés, incluso antes
de publicar, para que el sitio salga con la analítica funcionando desde el
primer día.

## Qué falta confirmar antes de considerarlo terminado

Ver la sección 12 del blueprint de marca para la lista completa. Los puntos
más importantes:

- A qué corresponde cada uno de los dos precios de Aguaí en la lista de
  salón (dulce vs. mermelada).
- Precio y disponibilidad actual de Higo, Kinoto, Guayaba y Batatita.
- Costo/plazo real de envío a otras provincias (courier a usar).
- Una foto real de Naranja (hoy se muestra solo un color).

## Estructura

```
src/pages/index.astro   → todo el sitio (una sola página)
public/images/          → logo real y fotos de producto (ya recortadas y sobre blanco)
```
