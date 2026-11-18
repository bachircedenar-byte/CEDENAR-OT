# CEDENAR OT

App web (PWA) de **Órdenes de Trabajo** y **Eventos y Revisiones** para **CEDENAR S.A.E.S.P.** — Centrales Eléctricas de Nariño.

## Qué incluye

- **Órdenes de trabajo** (6 pasos): datos generales, descripción de trabajos, permisos, fotos con y sin ubicación, egreso y cierre.
- **Pestaña Eventos y Revisiones**: registro de eventos y revisiones con materiales, fecha de inicio/fin, duración, responsable ("Realizado por") y **evidencias fotográficas**.
- **PDF de Eventos y Revisiones** con documento autónomo: fuentes y logo incrustados, evidencias numeradas **de dos en dos por fila** (nunca se desbordan ni se salen de la página), firmas y pie.
- **Dictado por voz** en el campo Observaciones de Eventos y Revisiones (Web Speech API, español de Colombia).
- **Modo noche**, 100 % offline (IndexedDB + Service Worker), sin CDN ni fuentes externas.

## Publicación

El sitio se publica con **GitHub Pages** desde la rama `main` mediante `.github/workflows/pages.yml`.

Los recursos binarios (logo, íconos, tipografías Montserrat y el worker de PDF.js) se guardan en el repositorio codificados en Base64 dentro de `assets-b64/`; el workflow los reconstruye antes de publicar. Esto mantiene el repositorio íntegramente en texto plano.

## Estructura

```
index.html            App completa (HTML + CSS + JS en un solo archivo)
service-worker.js     Cache offline (network-first para el HTML, cache-first para estáticos)
manifest.json         Manifiesto de la PWA
assets-b64/           Recursos binarios en Base64 (reconstruidos en el deploy)
.github/workflows/    Despliegue automático a GitHub Pages
```

## Versión actual

**v2.9** — Portal CEDENAR + dictado por voz.
