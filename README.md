# EDT Tucumán – Sitio web

Sitio web inspirado en el perfil de Instagram [@edtucuman](https://www.instagram.com/edtucuman/). Diseño responsive, oscuro y fácil de personalizar.

## Cómo ver el sitio

1. Abrí la carpeta del proyecto.
2. Hacé doble clic en `index.html` para abrirlo en el navegador.

O desde la terminal (en la carpeta del proyecto):

```bash
# Opción 1: con Python
python -m http.server 8000

# Opción 2: con Node (npx)
npx serve .
```

Luego entrá a `http://localhost:8000` en el navegador.

## Estructura del proyecto

- `index.html` – Página principal (inicio, nosotros, galería, contacto).
- `styles.css` – Estilos y diseño responsive.
- `main.js` – Menú móvil y comportamiento del header.

## Personalización

### Textos e información

- **Hero (inicio):** Editá en `index.html` las etiquetas dentro de `.hero-content` (título, subtítulo, botones).
- **Nosotros:** Cambiá el contenido en la sección `#nosotros` (`.about-text`).
- **Contacto:** Actualizá el enlace de WhatsApp en `#contacto`: reemplazá `5493810000000` por el número real (código país + número sin 0 ni 15).

### Galería con fotos de Instagram

No se puede “sacar” el feed automáticamente sin usar la API de Instagram. Podés:

1. **Enlaces a Instagram:** Dejar los ítems de la galería como están (cada uno lleva a [@edtucuman](https://www.instagram.com/edtucuman/)).
2. **Fotos manuales:** Descargar las fotos que quieras de tu perfil y usarlas en el sitio. En cada `.gallery-item` reemplazá el `<div class="gallery-img" style="...">` por:
   ```html
   <img class="gallery-img" src="ruta/a/tu-foto.jpg" alt="Descripción">
   ```
   y en `styles.css` asegurate de que `.gallery-img` tenga `width: 100%; height: 100%; object-fit: cover;` (ya está definido para el div; si usás `<img>`, esa clase aplica igual).

### Colores y tipografía

En `styles.css`, al inicio (`:root`), podés cambiar:

- `--color-accent` y `--color-accent-dim`: color principal (hoy dorado/ámbar).
- `--color-bg` y `--color-surface`: fondos.
- `--color-text` y `--color-text-muted`: textos.

Las fuentes se cargan desde Google Fonts (Outfit y Playfair Display). Si querés otras, cambiá el `<link>` en `index.html` y las variables `--font-sans` y `--font-display` en `styles.css`.

## Publicar en línea

Podés subir la carpeta completa (con `index.html`, `styles.css` y `main.js`) a:

- **GitHub Pages:** creá un repo, subí los archivos y activá Pages en Settings.
- **Netlify / Vercel:** arrastrá la carpeta al sitio o conectá el repo.
- Cualquier hosting que permita archivos estáticos (FTP, cPanel, etc.).

No hace falta instalar nada: es solo HTML, CSS y JavaScript.

## Enlaces

- Instagram: [instagram.com/edtucuman](https://www.instagram.com/edtucuman/)
