# Proyecto Integrador — Programación Web Básica (Sesiones 4–7)

Este repositorio contiene el **proyecto integrador** del curso.  
A partir de la **Sesión 4**, trabajaremos sobre **un mismo sitio multipágina** y lo iremos mejorando incrementalmente hasta la **Sesión 7**.

---

## 1) Objetivo del proyecto

Construir un mini-sitio web multipágina con:

- **HTML semántico** (estructura clara y accesible)
- **CSS mantenible** (base reusable, consistencia visual)
- **Contenido enriquecido correcto** (tablas para datos, media embebida con buenas prácticas)
- **Formularios accesibles** (labels, validación HTML5)
- **Responsive** y preparación para publicación (clase 7)

> Regla del curso: **no se “reconstruye” el proyecto cada sesión**.  
> Se agregan capas de mejora con disciplina.

---

## 2) Requisitos (herramientas)

### Obligatorio
- Editor: **VS Code**
- Extensión VS Code: **Live Server**
- Navegador: **Chrome** o **Edge** (para DevTools)

### Recomendado
- Extensión VS Code: **Prettier**
- Conocimientos: uso básico de carpetas/rutas y navegación de archivos.

---

## 3) Cómo ejecutar el proyecto (local)

1. Abre la carpeta `web-basica/` en VS Code
2. Clic derecho sobre `index.html` → **Open with Live Server**
3. Navega entre páginas usando el menú

### Checklist de ejecución
- El sitio abre en una URL tipo: `http://127.0.0.1:5500/`
- **No** estás usando `file://...`
- El CSS se aplica (tipografía/colores se notan)

---

## 4) Estructura esperada del proyecto (estado mínimo)

Al finalizar la **Sesión 4**, el proyecto debe tener:

```txt
web-basica/
  README.md
  index.html
  acerca.html
  recursos.html
  datos.html
  media.html
  contacto.html
  assets/
    css/
      styles.css
    img/
    media/
```

> Nota: `assets/img` y `assets/media` pueden estar vacías por ahora, pero **las carpetas deben existir**.

---

## 5) Contrato de página (NO negociable)

Todas las páginas **deben** cumplir:

### Head mínimo
- `<!doctype html>`
- `<html lang="es">`
- `<meta charset="utf-8" />`
- `<meta name="viewport" content="width=device-width, initial-scale=1" />`
- `<title>...</title>` consistente (ej: `Inicio | Web Básica`)
- `<link rel="stylesheet" href="assets/css/styles.css" />`

### Estructura semántica
- `header`
- `nav`
- `main` con `id="contenido"` (**solo un main por página**)
- `footer`

### Accesibilidad mínima
- Skip link al inicio del body:
  ```html
  <a class="skip-link" href="#contenido">Saltar al contenido principal</a>
  ```
- Foco visible al navegar con teclado (`:focus-visible` en CSS)
- Menú con `aria-current="page"` en el enlace activo (solo uno por página)

---

## 6) Qué debe estar listo HOY (fin de Sesión 4)

### A) CSS base consolidado (un solo archivo)
`assets/css/styles.css` debe incluir como mínimo:

- Tokens en `:root` (colores, spacing, tipografía)
- Reset mínimo (`box-sizing: border-box;` + body sin margin)
- `.container`, `.nav`, `.card`
- Estilos de enlaces + `:focus-visible`
- `skip-link`
- Estilos básicos para tablas y media (`table`, `iframe/video/audio/img`)

### B) Páginas NO vacías
Las 6 páginas deben tener contenido mínimo (aunque sea corto) y un menú funcional.

### C) Verificación con DevTools
- **Network:** `assets/css/styles.css` carga en **200** (no 404)
- **Console:** sin errores
- **Elements:** existen los landmarks (`header/nav/main/footer`)

---

## 7) Reglas de calidad (para todo el proyecto)

### HTML
- No usar tablas para layout (tablas = datos)
- Un `h1` por página
- Enlaces descriptivos (evitar “clic aquí”)
- Imágenes informativas con `alt` útil; decorativas con `alt=""`

### CSS
- Evitar IDs para estilo
- Evitar selectores excesivamente largos
- Entender cascada/especificidad antes de usar `!important` (casi nunca se permite)

---

## 8) Plan hacia la Sesión 7 (hitos por sesión)

### Sesión 4 (actual)
✅ Proyecto desde cero + CSS base reusable + consistencia multipágina

### Sesión 5 (siguiente)
- Construir `contacto.html` con **formularios accesibles**
- `label` correcto, `required`, `type=email`, `textarea`, `fieldset/legend` cuando aplique
- Validación HTML5 y mensajes/estados básicos

### Sesión 6
- **Layout y responsive** (Flex/Grid)
- Ajustes por breakpoints
- Navegación/estructura adaptativa (sin romper accesibilidad)

### Sesión 7
- Preparación final: revisión de calidad, optimización básica (imágenes/rutas), consistencia
- Publicación (o paquete final) + checklist final del sitio
- Entrega final del proyecto integrador

> Importante: cada sesión agrega una capa. No se rehace desde cero.

---

## 9) Troubleshooting (problemas típicos)

### “No se aplica el CSS”
- Verifica que en el `<head>` exista:
  ```html
  <link rel="stylesheet" href="assets/css/styles.css" />
  ```
- Abre DevTools → **Network** → recarga → confirma **200** para `styles.css`
- Si aparece **404**, la ruta está mal o el archivo no existe

### “No funciona el menú / enlaces”
- Confirma que los archivos están en la **misma carpeta raíz** (`index.html`, `acerca.html`, etc.)
- Enlaces deben ser del estilo: `href="acerca.html"`

### “El skip link no aparece”
- Debe estar lo más arriba posible en el `<body>`
- Debe apuntar a `#contenido`
- Prueba con teclado: presiona `Tab` al cargar

---

## 10) Criterio de aprobación del estado actual (Sesión 4)

Se considera “OK” si:

- ✅ Todas las páginas existen y no están vacías
- ✅ Menú navega entre páginas
- ✅ `aria-current="page"` correcto en cada página
- ✅ `styles.css` carga sin 404 y aplica estilos
- ✅ Foco visible + skip link funcional
- ✅ No hay errores en consola

---

## 11) Entrega

- Mantener estructura y nombres de archivos tal cual
- No cambiar rutas sin justificación
- No usar frameworks (todavía)
- Todo debe abrir en navegador con Live Server

---

**Fin del README**
