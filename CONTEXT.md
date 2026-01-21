# Contexto Técnico: Sitio Web Emanuela Pau

## Resumen del Proyecto
Sitio web profesional, elegante y multilingüe (Inglés, Italiano, Español) para Emanuela Pau, psicóloga clínica y psicoterapeuta especializada en terapia online para expatriados.

## Arquitectura y Decisiones Técnicas

### 1. Motor del Sitio: Jekyll
- **Versión**: ~> 4.3
- **Hosting Previsto**: GitHub Pages (se ha mantenido la compatibilidad limitando el uso de plugins no estándar).
- **Enfoque Multilingüe**:
  - Implementado mediante **estructura de directorios** (`/en/`, `/it/`, `/es/`).
  - Lógica de plantillas **Liquid** personalizada en `_includes/header.html` y `_layouts` para manejar la navegación y el cambio de idioma sin depender de plugins complejos.
  - Datos de navegación y traducciones centralizados en `_data/navigation.yml` y `_data/translations.yml`.

### 2. Sistema de Diseño (CSS/SCSS)
- **Framework**: Custom CSS (Vanilla SCSS), sin frameworks pesados como Bootstrap o Tailwind para garantizar un diseño ligero y personalizado.
- **Tema**: "Serene Professional".
  - **Colores**: Sage Green (`#5A7D7C`) y Warm Sand (`#D8CFC4`).
  - **Tipografía**: *Playfair Display* (títulos) y *Lato* (cuerpo), cargadas desde Google Fonts.
- **Responsive**: Diseño completamente adaptable mediante Flexbox y Grid.

### 3. Estructura de Archivos Clave
- `_config.yml`: Configuración global y definición de idiomas disponibles.
- `_layouts/`:
  - `default.html`: Estructura base HTML.
  - `home.html`: Diseño específico para la landing page.
  - `page.html`: Diseño estándar con cabecera de título para páginas interiores.
- `_includes/`:
  - `header.html`: Navegación dinámica y selector de idioma.
  - `footer.html`: Pie de página común.
- `assets/`:
  - `css/style.scss`: Hoja de estilos principal.
  - `images/`: Directorio para imágenes (actualmente contiene referencias a `profile_main.png` y `profile_work.png`).

### 4. Contenido
- El contenido está duplicado y traducido manualmente en las carpetas `en/`, `it/`, `es/`.
- Cada página tiene Front Matter definiendo su `layout`, `lang`, `title`, y `subtitle`.

## Estado Actual
- **Estructura**: ✅ Completada.
- **Diseño**: ✅ Implementado.
- **Contenido**: ✅ Creado en los 3 idiomas (Home, About, Services, Contact).
- **Imágenes**: ⚠️ Imágenes generadas pero requieren copia manual a `d:\test_web_manu\assets\images\` debido a restricciones de permisos del entorno local.

## Tareas Pendientes / Próximos Pasos
1. **Integración de Imágenes**:
   - Copiar manualmente `profile_main.png` y `profile_work.png` a la carpeta `assets/images/`.
   - Reemplazar estas imágenes por fotografías reales de Emanuela en el futuro.
2. **Despliegue**:
   - Subir el repositorio a GitHub.
   - Activar GitHub Pages desde la configuración del repositorio.
3. **Mantenimiento**:
   - Para añadir un nuevo idioma, actualizar `_config.yml`, `_data/navigation.yml` y crear la carpeta correspondiente.
