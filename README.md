# Portfolio IT Profesional 💼

Portfolio profesional y llamativo diseñado específicamente para profesionales del sector IT. Totalmente responsivo, moderno y con animaciones suaves.

## 🌟 Características

- **Diseño Moderno**: Interfaz limpia y profesional con tema oscuro
- **Totalmente Responsivo**: Se adapta perfectamente a todos los dispositivos
- **Animaciones Suaves**: Efectos visuales atractivos sin afectar el rendimiento
- **Secciones Completas**:
  - Hero con presentación animada
  - Sobre Mí con estadísticas
  - Habilidades técnicas con barras de progreso
  - Proyectos destacados con efectos hover
  - Experiencia profesional con timeline
  - Formulario de contacto funcional
- **Optimizado para SEO**: Meta tags y estructura semántica
- **Performance**: Carga rápida y optimizada

## 🎨 Tecnologías Utilizadas

- HTML5
- CSS3 (Variables CSS, Grid, Flexbox, Animaciones)
- JavaScript Vanilla (ES6+)
- Font Awesome (Iconos)

## 📁 Estructura del Proyecto

```
portfolio-it/
│
├── index.html          # Página principal
├── css/
│   └── styles.css      # Estilos principales
├── js/
│   └── script.js       # JavaScript con funcionalidades
├── assets/
│   └── images/         # Carpeta para imágenes
└── README.md           # Este archivo
```

## 🚀 Instalación y Uso

### Opción 1: Uso Local Directo

1. Descarga o clona el repositorio
2. Abre el archivo `index.html` en tu navegador
3. ¡Listo! El portfolio ya está funcionando

### Opción 2: Servidor Local

Si quieres usar un servidor local:

```bash
# Con Python 3
python -m http.server 8000

# Con Node.js (npx)
npx serve

# Con Live Server (VS Code Extension)
# Click derecho en index.html > Open with Live Server
```

## ✏️ Personalización

### 1. Información Personal

Edita `index.html` y reemplaza:

- **Nombre**: Busca "Tu Nombre" y reemplázalo
- **Rol**: Busca "Desarrollador Full Stack"
- **Descripción**: Personaliza las descripciones en cada sección
- **Redes sociales**: Actualiza los enlaces en la clase `.social-links`
- **Email y contacto**: Actualiza la información en la sección de contacto

### 2. Colores del Tema

Edita `css/styles.css` en la sección de variables CSS (`:root`):

```css
:root {
    --primary-color: #00d4ff;      /* Color principal */
    --secondary-color: #7b2cbf;    /* Color secundario */
    --accent-color: #ff006e;       /* Color de acento */
    /* Modifica según tu preferencia */
}
```

### 3. Proyectos

En `index.html`, busca la sección `.projects-grid` y edita cada `.project-card`:

```html
<div class="project-card">
    <div class="project-image">
        <!-- Cambia el icono o añade una imagen -->
    </div>
    <div class="project-info">
        <h3>Nombre del Proyecto</h3>
        <p>Descripción del proyecto...</p>
        <div class="project-tags">
            <span class="tag">Tecnología 1</span>
            <span class="tag">Tecnología 2</span>
        </div>
    </div>
</div>
```

### 4. Habilidades

Edita las barras de progreso en la sección `.skills`:

```html
<div class="skill-item">
    <div class="skill-info">
        <span>Nombre de la Habilidad</span>
        <span>90%</span> <!-- Porcentaje -->
    </div>
    <div class="skill-bar">
        <!-- Ajusta el width al mismo porcentaje -->
        <div class="skill-progress" style="width: 90%"></div>
    </div>
</div>
```

### 5. Experiencia

En la sección `.timeline`, edita cada `.timeline-item`:

```html
<div class="timeline-item">
    <div class="timeline-dot"></div>
    <div class="timeline-content">
        <div class="timeline-date">2022 - Presente</div>
        <h3>Título del Puesto</h3>
        <h4>Nombre de la Empresa</h4>
        <p>Descripción del rol...</p>
        <ul>
            <li>Logro 1</li>
            <li>Logro 2</li>
        </ul>
    </div>
</div>
```

### 6. Imágenes

Para añadir tu foto de perfil:

1. Guarda tu imagen en `assets/images/`
2. Reemplaza el placeholder en `.about-image`:

```html
<div class="about-image">
    <img src="assets/images/tu-foto.jpg" alt="Tu Nombre">
</div>
```

Para imágenes de proyectos:

```html
<div class="project-image">
    <img src="assets/images/proyecto-1.jpg" alt="Nombre del Proyecto">
    <div class="project-overlay">
        <!-- Enlaces del proyecto -->
    </div>
</div>
```

## 📱 Características Responsivas

El portfolio está optimizado para:

- **Desktop**: > 968px
- **Tablet**: 768px - 968px
- **Mobile**: < 768px
- **Small Mobile**: < 480px

## 🎯 Funcionalidades JavaScript

### Activadas por Defecto:

- Navegación sticky con efecto scroll
- Menú hamburguesa responsive
- Links de navegación activos según scroll
- Contador animado de estadísticas
- Animaciones de aparición al hacer scroll
- Efecto typing en código del hero
- Smooth scrolling
- Animación de barras de progreso
- Efecto tilt en tarjetas de proyectos
- Botón scroll to top

### Opcionales (comentadas):

Para activar funciones opcionales, descomenta en `js/script.js`:

```javascript
// Efecto de rastro del mouse
createTrailEffect();
```

## 🔧 Personalización Avanzada

### Agregar Nuevas Secciones

1. Añade el HTML en `index.html`
2. Crea los estilos en `css/styles.css`
3. Actualiza la navegación
4. Añade funcionalidad en `js/script.js` si es necesario

### Cambiar Animaciones

Las animaciones están definidas en `css/styles.css`:

```css
@keyframes nombreAnimacion {
    0% { /* estado inicial */ }
    100% { /* estado final */ }
}
```

### Integrar Formulario de Contacto

El formulario actualmente muestra un mensaje en consola. Para conectarlo a un backend:

1. Edita `js/script.js` en la sección de Form Handling
2. Reemplaza el `console.log` con una llamada fetch/axios:

```javascript
contactForm.addEventListener('submit', async (e) => {
    e.preventDefault();

    const formData = {
        name: document.getElementById('name').value,
        email: document.getElementById('email').value,
        subject: document.getElementById('subject').value,
        message: document.getElementById('message').value
    };

    try {
        const response = await fetch('tu-api-endpoint', {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: JSON.stringify(formData)
        });

        if (response.ok) {
            showNotification('Mensaje enviado exitosamente!', 'success');
            contactForm.reset();
        }
    } catch (error) {
        showNotification('Error al enviar el mensaje', 'error');
    }
});
```

## 🌐 Deployment

### GitHub Pages

1. Sube el proyecto a GitHub
2. Ve a Settings > Pages
3. Selecciona la rama main
4. ¡Tu portfolio estará en línea!

### Netlify

```bash
# Arrastra la carpeta del proyecto a netlify.com
# O usa Netlify CLI:
netlify deploy --prod
```

### Vercel

```bash
# Instala Vercel CLI
npm i -g vercel

# Deploy
vercel
```

## 📋 Checklist de Personalización

- [ ] Cambiar nombre y título
- [ ] Actualizar descripción personal
- [ ] Añadir enlaces a redes sociales
- [ ] Subir foto de perfil
- [ ] Actualizar estadísticas
- [ ] Personalizar habilidades y porcentajes
- [ ] Añadir proyectos reales con enlaces
- [ ] Actualizar experiencia laboral
- [ ] Configurar información de contacto
- [ ] Añadir imágenes de proyectos
- [ ] Probar formulario de contacto
- [ ] Verificar responsive en todos los dispositivos
- [ ] Optimizar imágenes
- [ ] Actualizar meta tags para SEO

## 💡 Tips

1. **Imágenes**: Usa imágenes optimizadas (< 200KB) para mejor rendimiento
2. **Colores**: Mantén un esquema de color consistente (2-3 colores principales)
3. **Contenido**: Sé conciso pero informativo
4. **Proyectos**: Muestra tus mejores 4-6 proyectos
5. **Actualización**: Mantén tu portfolio actualizado regularmente

## 🐛 Solución de Problemas

### Los iconos no se muestran
- Verifica la conexión a internet (Font Awesome se carga desde CDN)
- O descarga Font Awesome localmente

### Las animaciones no funcionan
- Asegúrate de que JavaScript está habilitado
- Verifica la consola del navegador para errores

### El diseño se ve roto en móvil
- Limpia la caché del navegador
- Verifica que el viewport meta tag esté presente

## 📄 Licencia

Este proyecto es de código abierto y está disponible para uso personal y comercial.

## 🤝 Contribuciones

¡Las mejoras son bienvenidas! Si tienes sugerencias:

1. Fork el proyecto
2. Crea una rama para tu feature
3. Commit tus cambios
4. Push a la rama
5. Abre un Pull Request

## 📧 Contacto

Para preguntas o sugerencias, contáctame a través de las redes sociales en el portfolio.

---

**Desarrollado con ❤️ para la comunidad IT**

¡Buena suerte con tu portfolio! 🚀
