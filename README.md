[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/RI8vnIt_)
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=23334162)
# Mi Blog Personal - TP Semana 1

Página web de blog personal usando **HTML5**, **CSS3** y **Bootstrap 5**.

## 📋 Requisitos

- Navegador moderno (Chrome, Firefox, Safari, Edge)
- Editor de código (VS Code recomendado)
- Git

## 🚀 Cómo abrir el proyecto

1. **Clonar el repositorio**:
   ```bash
   git clone <URL_del_repositorio>
   cd blog-personal
   ```

2. **Abrir en navegador**:
   - **Opción 1**: Doble-click en `index.html`
   - **Opción 2**: Usar Live Server en VS Code (extensión)
   - **Opción 3**: Python server:
     ```bash
     python -m http.server 8000
     # Luego accede a http://localhost:8000
     ```

## 📁 Estructura del proyecto

```
blog-personal/
├── index.html          # Página principal (listado de artículos)
├── about.html          # Página "Acerca de mí"
├── contact.html        # Formulario de contacto
├── assets/
│   ├── styles.css      # Estilos personalizados
│   └── images/         # Carpeta para imágenes (favicon, avatar, etc.)
├── .github/
│   └── workflows/
│       └── validate.yml # Tests automatizados en GitHub Actions
├── .gitignore
└── README.md           # Este archivo

```

## ✅ Criterios de aceptación

- **HTML válido**: Sin errores W3C. Verifica en https://validator.w3.org/
- **Todas las páginas funcionan**: Links internos sin 404
- **Formulario funcional**: 
  - Campos: nombre, email, teléfono (opcional), mensaje
  - Validación HTML5 (`required`, `type="email"`, etc.)
  - Feedback visual (:valid, :invalid estilos)
- **Navbar responsiva**: Funciona en mobile y desktop
- **Bootstrap bien usado**: Sin DIVs innecesarios que Bootstrap ya resuelve
- **CSS limpio**: Sin duplicación, nombres claros
- **Git**: ≥5 commits con mensajes significativos
- **README**: Instrucciones claras (este archivo)

## 🎨 Customización

### Cambiar colores
Edita las variables en `assets/styles.css`:

```css
:root {
    --primary-color: #0d6efd;  /* Cambiar aquí */
    --text-color: #212529;
    --light-bg: #f8f9fa;
}
```

### Agregar artículos
En `index.html`, copia la tarjeta (`.card`) y modifica:
- Imagen: `src="assets/images/article-X.jpg"`
- Título, autor, descripción

### Cambiar tipografía
En `assets/styles.css`, modifica:
```css
body {
    font-family: 'Tu fuente aquí', sans-serif;
}
```

## 🧪 Validación

### Validar HTML localmente
Usa el validator de W3C: https://validator.w3.org/

### Validar CSS
Usa el CSS Validator: https://jigsaw.w3.org/css-validator/

### GitHub Actions
Cada vez que hagas `git push`, se ejecutan tests automáticos. Verifica el estado en la pestaña "Actions" de tu repositorio.

## 💡 Pistas útiles

### 1. **Navbar responsiva**
Bootstrap proporciona `.navbar-collapse` y `.navbar-toggler`. Úsalos para que el menú se oculte en mobile.

### 2. **Grid responsivo**
Para 3 columnas en desktop, 1 en mobile:
```html
<div class="col-12 col-md-4">...</div>
```

### 3. **Formulario accesible**
Cada `<input>` debe tener un `<label>` asociado con `for` y `id`.

### 4. **CSS sobre Bootstrap**
Tu `assets/styles.css` se importa DESPUÉS de Bootstrap, así que tus estilos lo sobrescriben. Usa clases personalizadas (BEM) para no romper componentes Bootstrap.

## 📚 Recursos

- [Bootstrap 5 Docs](https://getbootstrap.com/docs/5.0/)
- [MDN: HTML](https://developer.mozilla.org/es/docs/Web/HTML)
- [MDN: CSS](https://developer.mozilla.org/es/docs/Web/CSS)
- [W3C HTML Validator](https://validator.w3.org/)

## 🐛 Problemas comunes

| Problema | Solución |
|----------|----------|
| Navbar no responde | Verifica que hayas importado Bootstrap JS al final de `</body>` |
| Estilos CSS no aparecen | Limpia cache (Ctrl+Shift+R) o abre en navegación privada |
| Formulario no valida | Asegúrate de usar atributos `required`, `type="email"`, etc. |
| Bootstrap no carga (CDN) | Verifica conexión a internet o descarga Bootstrap localmente |

---

**Autor**: [Tu nombre]  
**Fecha**: 2026-03-13  
**Estado**: En desarrollo
