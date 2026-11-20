# Canciones Personalizadas

Sitio estático (HTML + CSS + JavaScript) compatible con **GitHub Pages**. Sin backend ni servicios de pago.

## Archivos (subir todos a la raíz del repositorio)
- `index.html`: la página completa.
- `video/trabajo.mp4` y `img/poster-video.jpg`: video de la sección «Mirá cómo lo contamos».
- `og-image.png`: imagen que se ve al compartir el link en WhatsApp, Instagram, Facebook, etc.
- `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`: íconos de la pestaña y del celular.
- `sitemap.xml`, `robots.txt`: para que Google encuentre la página.
- `.nojekyll`: evita el procesamiento de Jekyll.
- `TEXTOS_PARA_REDES.md`: textos para redes (sin cambios).

## PASO OBLIGATORIO antes de publicar: poné tu dirección real
Tu dirección de GitHub Pages es `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`. Reemplazá ese texto en `index.html` (imagen para compartir), `sitemap.xml` y `robots.txt`.
En la terminal, desde la carpeta del proyecto:
```bash
sed -i 's#https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/#https://TU-REAL.github.io/TU-REPO/#g' index.html sitemap.xml robots.txt
```
(o usá buscar y reemplazar en tu editor). Sin esto, el link se comparte sin la imagen de vista previa.

## Ajustes rápidos (al inicio del `<script>` en `index.html`)
- `ENTREGA`: tiempo de entrega, por ejemplo `'3 a 5 días hábiles'`. Vacío = no se muestra. Si lo completás, aparece sobre los paquetes y en la pregunta «¿Cuánto tarda?».
- `BANNER`: aviso de temporada arriba de todo. `activo:false` lo apaga, `fin` es la fecha desde la cual deja de mostrarse (por defecto 25/12/2026), `limite` muestra una fecha tope en el texto (`'2026-12-18'`).
- `GOATCOUNTER`: tu código de goatcounter.com (gratis, sin cookies) para contar visitas.
- `WHATSAPP_NUMBER`: sin cambios.

## Qué incluye
- **Redes**: sección «Conocé nuestros trabajos» (`#redes`), menú «Nuestras redes», menú móvil desplegable y accesos en el pie.
- **Video** vertical en la sección `#video`: no se descarga hasta que el visitante toca play.
- **WhatsApp directo**: botón en la portada, enlace bajo el formulario y botón flotante.
- **Formulario que se guarda solo**: si la persona cierra la página, al volver retoma donde estaba (se guarda 7 días, solo en su dispositivo, con botón «Empezar de nuevo»).
- **Origen del pedido**: si compartís el link con `?utm_source=`, el mensaje de WhatsApp llega con la línea «Origen: …». Así sabés de qué red viene cada pedido.
- **SEO**: título y descripción para Argentina, datos estructurados y sitemap.

## Links para cada red (copiá y pegá)
```
https://TU-REAL.github.io/TU-REPO/?utm_source=instagram
https://TU-REAL.github.io/TU-REPO/?utm_source=tiktok
https://TU-REAL.github.io/TU-REPO/?utm_source=youtube
https://TU-REAL.github.io/TU-REPO/?utm_source=facebook
```

## Cómo agregar tus audios y testimonios
En `index.html`, buscá `const CATALOGO=[]`:
```js
const CATALOGO=[{titulo:'Nombre',ocasion:'Bodas y aniversarios',desc:'Breve descripción',audio:'audios/cancion1.mp3',portada:'img/portada1.jpg'}];
```
Subí las carpetas `audios/` e `img/`. Testimonios reales: `const TESTIMONIOS=[{texto:'...',autor:'Nombre'}]`. Mientras estén vacíos, la sección de testimonios no se muestra.

## Publicar en GitHub Pages
1. Subí todos los archivos a la raíz del repositorio (reemplazando los anteriores).
2. En GitHub: **Settings → Pages**, **Deploy from a branch**, rama `main`, carpeta `/ (root)`. Guardá.
3. Esperá 1 o 2 minutos.

## Prueba rápida
1. En el celular, tocá ☰ → **Nuestras redes** y probá los tres botones.
2. Completá dos pasos del formulario, cerrá la página y volvé a abrirla: debe retomar.
3. Tocá el video y el botón «Prefiero escribir por WhatsApp».
4. Compartí el link en WhatsApp y verificá que aparezca la imagen.
