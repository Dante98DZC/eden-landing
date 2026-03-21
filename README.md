# Sweet Eden - Dulcería Artesanal

Sitio web responsive para la dulcería Sweet Eden, un negocio pequeño especializado en dulces artesanales.

## Características

- **Diseño moderno y minimalista** con paleta de colores cálidos
- **Completamente responsive** enfocado en dispositivos móviles
- **Catálogo de productos** con categorías, precios y descripciones
- **Sistema de administración** con CRUD completo para productos y noticias
- **Integración con WhatsApp** para pedidos directos
- **Almacenamiento local** para persistencia de datos
- **Sección de noticias** para anuncios e información

## Estructura del proyecto

```
eden-landing/
├── index.html          # Archivo principal con la aplicación React
├── base.css           # Estilos CSS modernos y responsive
└── Res/               # Carpeta con imágenes de productos
    ├── IMG-20250808-WA0018.jpg
    ├── IMG-20250811-WA0001.jpg
    └── ... (más imágenes)
```

## Cómo usar

1. **Abrir el sitio**: Abre `index.html` en cualquier navegador moderno
2. **Navegar productos**: Usa las categorías para filtrar los dulces
3. **Hacer pedidos**: Los botones "Pedir" abren WhatsApp con el mensaje pre-llenado
4. **Panel de administración**:
   - Haz clic en "Admin" en la navegación
   - Usuario: `admin`
   - Contraseña: `sweeteden2025`
   - Gestiona productos y noticias desde el panel

## Funcionalidades del admin

### Productos
- Agregar nuevos productos con nombre, precio, categoría, descripción e imagen
- Editar productos existentes
- Marcar productos como "favoritos"
- Eliminar productos

### Noticias
- Crear anuncios y noticias
- Editar contenido existente
- Eliminar noticias antiguas

## Tecnologías utilizadas

- **React** (versión 18) para la interfaz
- **CSS moderno** con variables CSS y diseño responsive
- **LocalStorage** para persistencia de datos
- **WhatsApp API** para integración de pedidos

## Personalización

Para personalizar el sitio:

1. **Cambiar colores**: Modifica las variables CSS en `base.css`
2. **Actualizar productos**: Usa el panel de admin o edita `INITIAL_PRODUCTS` en `index.html`
3. **Cambiar número de WhatsApp**: Busca y reemplaza `18291234567` con tu número real
4. **Agregar imágenes**: Coloca las fotos en la carpeta `Res/` y actualiza las URLs

## Despliegue

El sitio es completamente estático y puede ser desplegado en:
- GitHub Pages
- Netlify
- Vercel
- Cualquier servidor web

Solo sube los archivos `index.html`, `base.css` y la carpeta `Res/`.