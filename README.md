# Canciones Personalizadas

Sitio web estático para recibir pedidos de canciones personalizadas. El cliente elige el servicio, completa un formulario y al finalizar se abre WhatsApp con el pedido organizado para que lo revise y lo envíe.

## Archivos

- `index.html`: aplicación completa. No requiere servidor, base de datos ni instalación.
- `TEXTOS_PARA_REDES.md`: textos sugeridos para colocar en perfiles y publicaciones.
- `.nojekyll`: evita el procesamiento de Jekyll en GitHub Pages.

## Publicar gratis con GitHub Pages

1. Descargá y descomprimí el ZIP.
2. En GitHub, creá un repositorio nuevo. Por ejemplo: `canciones-personalizadas`.
3. Entrá al repositorio y elegí **Add file → Upload files**.
4. Subí `index.html`, `README.md`, `TEXTOS_PARA_REDES.md` y `.nojekyll` en la raíz del repositorio.
5. Presioná **Commit changes**.
6. Abrí **Settings → Pages**.
7. En **Build and deployment**, elegí **Deploy from a branch**.
8. Seleccioná la rama `main` y la carpeta `/ (root)`. Guardá.
9. Esperá a que GitHub Pages publique el sitio. La dirección tendrá un formato parecido a `https://TU-USUARIO.github.io/canciones-personalizadas/`.

## WhatsApp configurado

El formulario está configurado con el número comercial que aparece en la información compartida: **11 3765-8829**, Argentina. El enlace utiliza el formato internacional `5491137658829`.

Si el número cambia, buscá esta línea al final de `index.html` y reemplazala por el número correcto, solo con dígitos:

```js
const WHATSAPP_NUMBER = '5491137658829';
```

## Cómo funciona

- Los tres tipos de servicio pasan por el mismo formulario.
- Los campos principales son obligatorios; fecha y detalle de fotos son opcionales.
- Para el servicio de video aparece una pregunta adicional sobre las fotografías.
- Al confirmar, se prepara un mensaje con todas las respuestas y se abre WhatsApp.
- El cliente todavía debe tocar **Enviar** dentro de WhatsApp. El sitio no envía mensajes por sí solo.

## Importante sobre las redes sociales

Instagram y TikTok normalmente no hacen clicables los enlaces escritos en el texto de una publicación. Usá la URL de GitHub Pages en el campo de enlace del perfil y, cuando esté disponible, en historias con sticker de enlace. En YouTube colocala en la descripción del video y en el comentario fijado. En Facebook podés agregarla en la publicación y en los botones/enlaces de la página.

## Privacidad y alcance

Esta versión no guarda los formularios en una base de datos ni recibe pagos. Los datos quedan en el dispositivo mientras se completa el formulario y se pasan a WhatsApp únicamente cuando el usuario toca el botón final. El precio que figura es el de referencia que ya estaba en el prototipo; confirmá que siga vigente antes de publicar.
