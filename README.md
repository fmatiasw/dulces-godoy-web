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
