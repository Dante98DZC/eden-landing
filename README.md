# Sweet Eden - Dulcería Artesanal

Sitio web responsive para la dulcería Sweet Eden, un negocio pequeño especializado en dulces artesanales.

## Características

- **Diseño moderno y minimalista** con paleta de colores cálidos
- **Completamente responsive** enfocado en dispositivos móviles
- **Catálogo de productos** con categorías, precios y descripciones
- **Sistema de administración** con CRUD completo para productos, noticias y categorías
- **Integración con WhatsApp** para pedidos directos
- **Base de datos en Supabase** para persistencia de datos en tiempo real
- **Subida de imágenes a Supabase Storage** (bucket `product-image`)
- **Autenticación con Supabase Auth**
- **Sección de noticias** para anuncios e información
- **Hero section editable** desde el panel de administración

## Estructura del proyecto

```
eden-landing/
├── index.html    # Archivo principal con la aplicación React
├── base.css      # Estilos CSS modernos y responsive
└── README.md     # Este archivo
```

## Cómo usar

1. **Abrir el sitio**: Abre `index.html` en cualquier navegador moderno
2. **Navegar productos**: Usa las categorías para filtrar los dulces
3. **Hacer pedidos**: Los botones "Pedir" abren WhatsApp con el mensaje pre-llenado
4. **Panel de administración**:
   - Haz clic en "Admin" en la navegación
   - Inicia sesión con tu email y contraseña de Supabase Auth
   - Gestiona productos, noticias y categorías desde el panel

## Funcionalidades del admin

### Productos
- Agregar nuevos productos con nombre, precio, categoría, descripción e imagen
- Subir imágenes directamente desde el dispositivo (se almacenan en Supabase Storage)
- Editar productos existentes
- Marcar productos como "favoritos"
- Marcar productos como "agotados"
- Eliminar productos

### Noticias
- Crear anuncios y noticias con imagen, título y texto
- Editar contenido existente
- Eliminar noticias antiguas

### Categorías
- Crear y eliminar categorías de productos

### Configuración general
- Editar el número de WhatsApp
- Personalizar el Hero: texto, colores e íconos de flotantes

## Tecnologías utilizadas

- **React 18** (via CDN) para la interfaz
- **CSS moderno** con variables CSS y diseño responsive
- **Supabase** como backend:
  - Base de datos PostgreSQL (tablas: `products`, `news`, `categories`, `site_config`)
  - Supabase Auth para autenticación de administradores
  - Supabase Storage para imágenes (bucket público `product-image`)

## Configuración de Supabase

El proyecto requiere las siguientes tablas en Supabase:

- `products` — name, category, price, description, image_url, featured, soldOut, position
- `news` — title, text, date, image_url
- `categories` — name
- `site_config` — key, value

Y el bucket de Storage `product-images` (público) con una policy que permita subidas a usuarios autenticados:

```sql
CREATE POLICY "auth upload" ON storage.objects
  FOR INSERT TO authenticated
  WITH CHECK (bucket_id = 'product-image');
```

## Despliegue

El sitio es completamente estático y puede desplegarse en:

- GitHub Pages
- Netlify
- Cloudflare Pages
- Cualquier servidor web

Solo sube los archivos `index.html` y `base.css`.