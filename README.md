# Canciones Personalizadas — rediseño premium

Sitio estático (HTML + CSS + JavaScript) compatible con **GitHub Pages**. No requiere backend ni dependencias de pago.

## Archivos
- `index.html`: página completa (hero, ocasiones, formulario de 10 pasos, catálogo, sección de redes, paquetes, FAQ y WhatsApp).
- `.nojekyll`: evita el procesamiento de Jekyll.
- `TEXTOS_PARA_REDES.md`: textos para redes (sin cambios).

## Conservado del proyecto original
- Número de WhatsApp (`WHATSAPP_NUMBER`, al inicio del script): `5491137658829`.
- Precio "Desde $10.000"; los otros dos servicios siguen "a coordinar por WhatsApp".
- Todos los campos del pedido original y el envío con mensaje prellenado.

## Redes sociales
La página incluye una sección **Conocé nuestros trabajos** y enlaces en el pie de página:
- YouTube: https://www.youtube.com/@Cancionpersonalizada
- TikTok: https://www.tiktok.com/@cancion_personalizada
- Instagram: https://www.instagram.com/cancion.personalizada/

## Cómo agregar tus audios
En `index.html`, buscá `const CATALOGO=[]` y completá:
```js
const CATALOGO=[{titulo:'Nombre',ocasion:'Bodas y aniversarios',desc:'Breve descripción',audio:'audios/cancion1.mp3',portada:'img/portada1.jpg'}];
```
Subí las carpetas `audios/` e `img/` al repositorio. Testimonios reales: `const TESTIMONIOS=[{texto:'...',autor:'Nombre'}]`; mientras esté vacío, la sección no se muestra.

## Publicar en GitHub Pages
1. Subí todos los archivos a la raíz de tu repositorio (reemplazando los anteriores).
2. En GitHub: **Settings → Pages**.
3. En **Source**, elegí **Deploy from a branch**, rama `main` y carpeta `/ (root)`. Guardá.
4. Esperá 1–2 minutos: el sitio queda en `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

## Prueba rápida
Completá el formulario, revisá el resumen, marcá la casilla y tocá **Enviar mi pedido por WhatsApp**.
