# ClaseLive

App web/PWA para:
- Grabar audio de una clase en vivo desde el micrófono.
- Transcribir en tiempo real con Web Speech API.
- Descargar la transcripción como TXT o PDF.
- Convertir la grabación a MP3 en el navegador mediante lamejs.
- Instalarse como PWA en navegadores compatibles.

## Despliegue rápido en GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube `index.html`, `manifest.json` y `sw.js`.
3. Ve a Settings → Pages.
4. Selecciona Deploy from a branch → `main` → `/root`.
5. Abre la URL HTTPS publicada.

## Importante

El micrófono requiere un contexto seguro (HTTPS), salvo localhost.
La compatibilidad de `SpeechRecognition` varía entre navegadores. En algunos casos el reconocimiento utiliza un servicio remoto del navegador. Para clases importantes, conviene conservar siempre el audio original como respaldo.

La app carga `lamejs` y `jsPDF` desde CDN para mantener el proyecto simple. Para una versión 100% independiente/offline, conviene alojar esas dependencias dentro del repositorio.
