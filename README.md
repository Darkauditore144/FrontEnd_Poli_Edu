# NEXO 360° — Prototipo funcional (Entrega Previa 2)

Portal de noticias de **educación, tecnología, turismo y comercio**. Prototipo front-end desarrollado para el módulo
*Desarrollo de Front-end* (Politécnico Grancolombiano). Corresponde a la maquetación de alta fidelidad de la Entrega Previa 1.

## Tecnologías
HTML5 semántico · CSS3 (variables, Flexbox, Grid de Bootstrap) · JavaScript · jQuery 3.7.1 · jQuery UI 1.14.1 · Bootstrap 5.3.3 (por CDN) · Ajax/JSON · localStorage.

## Estructura
```
nexo360/
├── index.html        Inicio (noticia destacada, últimas, tendencias, boletín)
├── listado.html      Listado con filtros, búsqueda y mini-CRUD (crear/editar/eliminar)
├── detalle.html      Lectura de una noticia (?id=N), favoritos y relacionadas
├── favoritos.html    Noticias guardadas con filtro por categoría
├── contacto.html     Formulario validado + preguntas frecuentes (Accordion)
├── css/styles.css    Estilos propios
├── js/
│   ├── store.js      Datos: Ajax al JSON, favoritos y CRUD en localStorage
│   ├── ui.js         Plantillas, encabezado, autocompletado, utilidades
│   ├── forms.js      Validación y diálogos (jQuery UI Dialog/Datepicker)
│   ├── pages.js      Controlador de cada página (según <body data-page>)
│   └── noticias-respaldo.js  Copia del JSON para abrir con doble clic (file://)
├── data/noticias.json  Fuente de datos de las noticias
└── img/              Imágenes
```

## Cómo ejecutarlo
1. **Rápido:** abrir `index.html` con doble clic (usa `noticias-respaldo.js` porque el navegador bloquea Ajax en `file://`).
2. **Recomendado:** servidor local, p. ej. extensión *Live Server* de VS Code, o `python -m http.server 8000` y abrir <http://localhost:8000>.
3. **Publicado:** GitHub Pages (Settings → Pages → Branch `main` / root).

Requiere conexión a Internet para cargar las librerías por CDN.

## Funcionalidades
- Noticias renderizadas dinámicamente desde `data/noticias.json` (Ajax `$.getJSON`).
- Favoritos persistentes (localStorage) con contador en el encabezado.
- Formularios con validación en vivo (contacto, boletín y publicación de noticias).
- Mini-CRUD de noticias (crear, leer, editar, eliminar) y botón para restablecer los datos originales.
- Buscador con autocompletado, filtros por categoría, orden y diálogos jQuery UI.
- Diseño responsive y accesible (etiquetas, `aria-*`, foco visible, enlace «Saltar al contenido»).

## Autor
Entrega individual — módulo Desarrollo de Front-end. Tutor: John Olarte Ramos.
