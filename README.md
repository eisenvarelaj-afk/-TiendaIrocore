# IRONCORE FITNESS

Tienda web ficticia de productos deportivos para un proyecto escolar. Sitio estático hecho con HTML, CSS y JavaScript puro, listo para GitHub Pages. No se procesan pagos.

## Qué incluye
Catálogo de 12 productos en COP, buscador por nombre, filtros por categoría, ofertas, carrito (agregar, quitar, cambiar cantidades, total, contador y mensaje de carrito vacío) guardado en `localStorage`, preguntas frecuentes y formulario de contacto con validación.

## Estructura
```
ironcore-fitness/
├── index.html
├── css/styles.css
├── js/app.js
├── assets/images/   (logo, hero y 12 ilustraciones SVG de productos)
├── README.md
└── .nojekyll
```
Todas las rutas son relativas, así que funciona en `https://USUARIO.github.io/ironcore-fitness/`.

## Probar en tu computador
Abre `index.html` con doble clic. Si prefieres un servidor local: `python -m http.server` y entra a `http://localhost:8000`.

## Publicar en GitHub Pages
1. Crea una cuenta en github.com e inicia sesión.
2. Pulsa **New repository**, nómbralo `ironcore-fitness`, déjalo **Public** y créalo.
3. En el repositorio, elige **Add file → Upload files** y arrastra el contenido de la carpeta (index.html, css, js, assets, README.md y .nojekyll). Si tu sistema oculta `.nojekyll`, no pasa nada: el sitio funciona igual.
4. Pulsa **Commit changes**.
5. Ve a **Settings → Pages**. En **Source** elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`, y pulsa **Save**.
6. Espera uno o dos minutos y abre `https://TU-USUARIO.github.io/ironcore-fitness/`.

Si ves un error 404, revisa que `index.html` esté en la raíz del repositorio (no dentro de otra carpeta) y que el repositorio sea público.

## Formulario de contacto
Valida nombre, correo y mensaje en el navegador, pero no envía mensajes: un sitio estático no tiene servidor. Para recibirlos de verdad, usa un servicio externo como Formspree o Web3Forms y apunta el `action` del formulario a su URL.

## Cambiar productos e imágenes
Los productos están en la lista `PRODUCTS` de `js/app.js`. Las imágenes son ilustraciones SVG generadas para la demostración; para usar fotos, reemplaza los archivos `assets/images/pN.svg` o cambia el campo `img` (y la extensión en `card()` y `renderCart()`).

## Diseño (versión 2)
Dirección de arte tomada del repositorio taste-skill (dirección "contact sheet", paleta grafito y naranja, tipografía Switzer): catálogo como tiras de recuadros por categoría, colores planos sin degradados ni sombras, botones cuadrados de un solo color y una sección de ofertas a campo completo. Switzer se carga desde Fontshare; sin conexión el sitio usa la fuente del sistema.
