# Redirección de rubenpa79.github.io/atalaya-verde

Sustituye el contenido del repo público `RubenPA79/atalaya-verde` **después** de que https://atalayaverde.github.io responda 200.

- `index.html`, `privacidad.html`, `aviso-legal.html`, `ejemplos/*` y `404.html` redirigen a la misma ruta en https://atalayaverde.github.io conservando query y hash (JavaScript `location.replace`). Hay `meta refresh`, `rel=canonical` y un enlace visible por si el JS no corre.
- `confirmar.html` y `baja.html` son copias funcionales (llaman a los mismos RPC de Supabase). No se redirigen automáticamente: los correos ya enviados apuntan a esta URL y el token va en `?t=`. Un `meta refresh` estático perdería el token si JavaScript no se ejecuta. Un aviso enlaza a la nueva dirección con los mismos parámetros.
