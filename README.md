# EJ4-HTML - Maquetación Web con HTML + CSS

Proyecto de maquetación web que demuestra el uso de **HTML5** y **CSS3** para crear una página con estructura de contenedores, menú de navegación, banner y cajas de contenido.

---

## Estructura del Proyecto

```
EJ4-HTML/
├── index.html      # Página principal
├── styles.css      # Hoja de estilos
├── img/            # Carpeta de imágenes
└── README.md       # Este archivo
```

---

## Explicación del HTML (`index.html`)

### 1. `<!doctype html>` y `<head>`
Declara el documento como HTML5. En el `<head>` se define:
- **`<meta charset="utf-8">`**: Codificación de caracteres UTF-8 para soportar tildes y ñ.
- **`<title>`**: Título que aparece en la pestaña del navegador.
- **`<link href="styles.css">`**: Vincula la hoja de estilos externa.

### 2. `#contenedor` — Contenedor principal
Es el `<div>` que envuelve **todo** el contenido de la página. Su función es centrar y limitar el ancho del sitio al 90% de la pantalla.

### 3. `#encabezado` — Cabecera
Contiene dos elementos:
- **`<img>`**: Espacio para un logo o imagen de cabecera (200×66 px).
- **`<ul>` — Menú de navegación**: Lista no ordenada con 4 items:
  - `LI1`, `LI2`, `LI3`, `LI4`: Enlaces (`<a>`) que representan las secciones del sitio. Cada `<li>` flota a la izquierda formando un menú horizontal.

### 4. `#banner` — Banner
Un `<div>` vacío que muestra una imagen de fondo via CSS. Ocupa 500px de alto y la imagen se centra sin repetirse.

### 5. `#centro` — Sección central
Contiene **3 cajas** (`class="cajas"`) dispuestas horizontalmente. Cada caja tiene:
- **`<h3>`**: Título de la caja (CONTENIDO 1, CONTENIDO 2, CONTENIDO 3).
- **`<p>`**: Texto de relleno (*Lorem ipsum*) que describe el contenido.

Las 3 cajas flotan a la izquierda (`float: left`) con un ancho del 30% cada una, ocupando juntas aproximadamente el 90% del contenedor.

---

## Explicación del CSS (`styles.css`)

| Regla CSS | Qué hace |
|-----------|----------|
| `* { margin:0; border:0; padding:0; }` | **Reset universal**: elimina márgenes, bordes y rellenos por defecto de todos los elementos. |
| `body { background-color: #000; }` | Fondo negro para toda la página. |
| `#contenedor { margin:auto; width:90%; }` | Centra el contenedor horizontalmente y lo limita al 90% del ancho de la ventana. |
| `#encabezado { background-color:#FFF; height:100px; }` | Cabecera blanca de 100px de alto. La `background-image` permite poner una imagen de fondo. |
| `#encabezado ul { float:right; width:600px; margin-top:20px; }` | El menú se alinea a la derecha del encabezado, con 600px de ancho y separado 20px del borde superior. |
| `#encabezado ul li { display en línea; float:left; width:148px; list-style:none; text-align:center; }` | Cada item del menú: sin viñetas, flotando a la izquierda, 148px de ancho, texto centrado y centrado verticalmente (`line-height: 40px`). |
| `#encabezado ul li a { font:"Arial Black"; text-transform:uppercase; color:#FFF; text-decoration:none; }` | Estilo de los enlaces: fuente Arial Black, todo en mayúsculas, color blanco y sin subrayado. |
| `#banner { height:500px; background-repeat:no-repeat; background-position:center; }` | Banner de 500px de alto. La imagen de fondo no se repite y se centra tanto horizontal como verticalmente. |
| `#centro { background-color:#009; height:320px; }` | Sección central con fondo azul oscuro y 320px de alto. |
| `.cajas { float:left; width:30%; margin:20px 10px 20px 23px; background-color:#000; color:#FFF; }` | Cada caja flota a la izquierda, ocupa el 30% del ancho, fondo negro, texto blanco y márgenes para separarlas entre sí. |
| `p { font:"Times New Roman"; font-size:12px; color:#FFF; text-align:justify; line-height:30px; }` | Párrafos: fuente serif, 12px, texto blanco justificado, con interlineado generoso de 30px. |
| `h3 { font:Tahoma; font-size:18px; color:#F00; text-align:center; text-transform:uppercase; margin-bottom:60px; }` | Títulos de las cajas: fuente Tahoma, 18px, color rojo, centrados, en mayúsculas y con 60px de separación inferior. |
| `#pie { background-color:#000; color:#FFF; text-align:center; height:40px; line-height:30px; }` | Pie de página (opcional): fondo negro, texto blanco centrado, 40px de alto. |

---

## Cómo usar

1. Cloná o descargá el proyecto.
2. Abrí `index.html` en tu navegador.
3. Para modificar estilos, editá `styles.css`.
4. Agregá tus propias imágenes en la carpeta `img/` y referencialas en el CSS con `url(img/tu-imagen.jpg)`.
