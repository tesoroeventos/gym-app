# Registro

Registro de entrenamientos de gimnasio. PWA offline, sin backend.

## Instalar

1. Repo **público** (GitHub Pages no sirve repos privados en plan gratuito)
2. Settings → Pages → Branch `main`, carpeta `/ (root)`
3. Abrir `https://tesoroeventos.github.io/gym-app/` en Chrome del celular
4. Menú → Instalar app

## Archivos

| Archivo | Qué hace |
|---|---|
| `index.html` | La app entera: UI, lógica, Dexie |
| `manifest.json` | Nombre, colores e íconos de instalación |
| `sw.js` | Service worker: cache offline |
| `icon.svg` | Ícono vectorial |
| `icon-192.png` `icon-512.png` | Íconos PWA |
| `icon-180.png` | Ícono iOS |
| `icon-maskable.png` | Ícono adaptativo Android |

## Datos

Todo vive en IndexedDB, en el teléfono. Nada sale de ahí.

Progreso → Datos → **Exportar JSON** para respaldar.

Borrar los datos del sitio en el navegador borra todo. Exportá seguido.

## Actualizar la app

Cambiá `CACHE = 'registro-v1'` a `v2` en `sw.js` cada vez que edites `index.html`.
Si no, el service worker sigue sirviendo la versión vieja.
