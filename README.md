# Servicio Técnico TICO — Partes de avería

Web estática con los 9 partes de avería de la actividad, en el orden del documento
original. Índice (archivador) + ficha individual de cada parte.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub.
2. Sube estos tres archivos a la raíz: `index.html`, `logo-ies.jpg`, `.nojekyll`.
3. Ve a **Settings → Pages**, y en *Source* elige **Deploy from a branch**,
   rama `main` y carpeta `/ (root)`. Guarda.
4. En un par de minutos la web estará en
   `https://TUUSUARIO.github.io/NOMBREDELREPO/`.

No necesita nada más: no hay build, ni dependencias, ni servidor.

## Cómo está montado

- Un solo `index.html` autocontenido (HTML, CSS y JS). Las tipografías vienen de
  Google Fonts.
- Navegación por *hash* (`#/parte/4`), así que funciona en GitHub Pages sin
  configurar redirecciones. Cada parte tiene su propia URL para poder enlazarla
  o proyectarla en clase.
- El color del papel codifica el nivel: blanco = nivel 1, amarillo = nivel 2,
  rosa = nivel 3 (como un juego de papel autocopiativo).

## Freno al copiar y pegar

Está activo lo siguiente:

- Selección de texto desactivada (`user-select`), también al arrastrar.
- Bloqueo de clic derecho, `Ctrl+C`, `Ctrl+X`, `Ctrl+A`, `Ctrl+S`, `Ctrl+U`,
  `Ctrl+P`, `F12` y `Ctrl+Shift+I/J/C`.
- El texto de los partes **no está en el HTML en claro**: va codificado y se
  reconstruye al cargar la página. Ver el código fuente o descargar el archivo
  con `curl` no devuelve el enunciado legible.
- La impresión sale en blanco con un aviso.

Ojo: esto disuade, no impide. Con las herramientas de desarrollo abiertas a mano
o desactivando JavaScript el texto se puede recuperar, y siempre queda la foto
con el móvil. Frena el atajo cómodo de copiar y pegar en una IA, que es de lo
que se trata.

### Si quieres desactivar alguna restricción

Al final del `index.html`, en el bloque comentado `--- Freno al copiar y pegar ---`:

- Para permitir imprimir: borra `"p"` de la lista de teclas y quita el bloque
  `@media print` del CSS.
- Para permitir seleccionar texto: quita `selectstart` y `copy` de la lista de
  eventos y la regla `user-select:none` del `body`.

## Cambiar el contenido

Los textos van codificados dentro de `index.html`, así que no se editan a mano.
Si necesitas modificar un parte, dímelo y te regenero el archivo.
