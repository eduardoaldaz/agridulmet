# Agridulmet — Guía rápida

## ¿Qué es esto?

Un sitio web completo, profesional y bilingüe para tu negocio de exportación de frutas.
Es **100% estático** — no necesita base de datos, PHP, ni nada especial.

## Estructura

```
tropicfruit/
├── index.html      ← El sitio web (NO lo toques si no sabes HTML)
├── content.json    ← ✏️ ESTE ARCHIVO es el que editas para cambiar textos
├── images/         ← 📸 Aquí van tus imágenes
│   ├── hero.jpg          (imagen principal del banner, 1920x1080)
│   ├── banana.jpg        (foto del banano, 800x600)
│   ├── platano.jpg       (foto del plátano, 800x600)
│   ├── pina.jpg          (foto de la piña, 800x600)
│   ├── nosotros.jpg      (foto de la empresa, 800x600)
│   ├── galeria-1.jpg     (foto galería 1, 800x600)
│   ├── galeria-2.jpg     (foto galería 2)
│   ├── galeria-3.jpg     (foto galería 3)
│   ├── galeria-4.jpg     (foto galería 4)
│   ├── galeria-5.jpg     (foto galería 5)
│   ├── galeria-6.jpg     (foto galería 6)
│   ├── og-image.jpg      (imagen para redes sociales, 1200x630)
│   ├── favicon.png       (icono del navegador, 32x32)
│   └── logo.png          (logo, opcional)
└── README.md       ← Este archivo
```

## Cómo editar el contenido

### Cambiar textos

1. Abre `content.json` con cualquier editor de texto (Notepad, VS Code, etc.)
2. Busca el texto que quieres cambiar
3. Cámbialo. Siempre hay dos versiones: `"es"` (español) y `"en"` (inglés)
4. Guarda el archivo
5. Sube el archivo actualizado a tu hosting

**Ejemplo — cambiar el título principal:**

```json
"titulo": {
  "es": "Tu nuevo título aquí",
  "en": "Your new title here"
}
```

### Cambiar imágenes

1. Prepara tu imagen nueva (JPG, PNG o WebP)
2. Ponle el MISMO nombre que la imagen que quieres reemplazar
3. Cópiala a la carpeta `images/`
4. Sube todo a tu hosting

### Cambiar datos de contacto

En `content.json`, busca la sección `"empresa"`:

```json
"empresa": {
  "nombre": "Agridulmet",
  "whatsapp": "593412345678",     ← Tu número SIN + ni espacios
  "email": "tu@email.com",
  "telefono": "+593 4 123 4567",
  "direccion": { "es": "Guayaquil, Ecuador", "en": "Guayaquil, Ecuador" }
}
```

### Agregar/quitar un producto

En `content.json`, busca `"productos" > "lista"` y copia/pega el bloque de un producto existente. Cambia los textos y el nombre de la imagen.

### Agregar fotos a la galería

Agrega un nuevo objeto en `"galeria" > "imagenes"`:

```json
{ "src": "images/galeria-7.jpg", "texto": { "es": "Nueva foto", "en": "New photo" } }
```

Y sube la imagen `galeria-7.jpg` a la carpeta `images/`.

---

## Cómo subir el sitio (hosting)

### Opción 1: Hosting barato ($2-5/mes)

Funciona con **cualquier hosting** (Hostinger, Namecheap, GoDaddy, HostGator, etc.):

1. Compra el hosting + dominio
2. Entra al panel de control (cPanel)
3. Abre el "Administrador de archivos"
4. Ve a la carpeta `public_html`
5. Sube TODO el contenido de esta carpeta ahí
6. ¡Listo! Tu sitio ya está online

### Opción 2: GRATIS con GitHub Pages

1. Crea cuenta en github.com
2. Crea un repositorio nuevo llamado `tupagina`
3. Sube todos los archivos
4. Ve a Settings > Pages > selecciona "main" branch
5. Tu sitio estará en `tunombre.github.io/tupagina`
6. Puedes conectar tu dominio propio (gratis)

### Opción 3: GRATIS con Netlify

1. Ve a netlify.com y crea cuenta
2. Arrastra la carpeta `tropicfruit` completa al dashboard
3. ¡Publicado! Te da una URL tipo `tupagina.netlify.app`
4. Puedes conectar tu dominio propio (gratis)

---

## Formulario de contacto

El formulario envía los datos directamente por **WhatsApp**. 
Cuando alguien lo llena y presiona "Enviar", se abre WhatsApp con toda la info formateada lista para que tú la recibas. 

No necesita servidor, PHP, ni configuración adicional.

---

## Tamaños recomendados de imágenes

| Imagen | Tamaño ideal | Formato |
|--------|-------------|---------|
| hero.jpg | 1920 x 1080 px | JPG (comprimida) |
| Productos | 800 x 600 px | JPG o WebP |
| Galería | 800 x 600 px | JPG o WebP |
| og-image.jpg | 1200 x 630 px | JPG |
| favicon.png | 32 x 32 px | PNG |

**Tip:** Comprime tus imágenes en [tinypng.com](https://tinypng.com) antes de subirlas. El sitio cargará más rápido.

---

## ¿Necesitas ayuda?

Si necesitas cambiar algo más complejo (colores, estructura, agregar secciones), 
busca un freelancer en Fiverr o un conocido que sepa HTML básico. 
El código es limpio y bien organizado.
