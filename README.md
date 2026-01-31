# C³ Consultoría Estratégica - Sitio Web

## 📁 Estructura del Proyecto

```
c3-consultoria-web/
├── index.html                                    # Página principal (landing page)
├── cuestionarios/
│   ├── autonomos-sin-trabajadores.html          # Cuestionario para autónomos sin empleados
│   ├── autonomos-con-trabajadores.html          # Cuestionario para autónomos con empleados
│   └── pyme-basic.html                          # Cuestionario para PYMEs
└── README.md                                    # Este archivo
```

## 🚀 Despliegue Rápido

### Opción 1: Vercel (Recomendado)

1. Ve a [vercel.com](https://vercel.com/signup)
2. Regístrate con GitHub
3. Click en "New Project"
4. Importa este repositorio
5. Click en "Deploy"
6. ¡Listo! Tu sitio estará en: `https://tu-proyecto.vercel.app`

### Opción 2: Netlify

1. Ve a [netlify.com](https://app.netlify.com/signup)
2. Regístrate
3. Arrastra esta carpeta a Netlify Drop
4. ¡Listo! Tu sitio estará publicado

### Opción 3: GitHub Pages

1. Sube este código a GitHub
2. Ve a Settings → Pages
3. Selecciona la rama main
4. ¡Listo! Tu sitio estará en: `https://tu-usuario.github.io/nombre-repo`

## ⚙️ Configuración de Make.com

Los cuestionarios están configurados para enviar datos a Make.com mediante webhooks.

**Archivos que requieren configuración del webhook:**
- `cuestionarios/autonomos-sin-trabajadores.html` (línea ~9586 y ~12380)
- `cuestionarios/autonomos-con-trabajadores.html`
- `cuestionarios/pyme-basic.html`

**Para configurar:**
1. Crea un escenario en Make.com
2. Añade un trigger "Webhook"
3. Copia la URL del webhook
4. Reemplaza `MAKE_WEBHOOK_URL` en cada archivo con tu URL

Busca en el código:
```javascript
const MAKE_WEBHOOK_URL = 'https://hook.us1.make.com/TU_WEBHOOK_AQUI';
```

## 🎨 Características

- ✅ Diseño responsive
- ✅ Branding C³ (colores dorados y tipografía corporativa)
- ✅ Generación de PDFs en el navegador
- ✅ Integración con Make.com para procesamiento de datos
- ✅ Sistema de notificaciones
- ✅ Contador de respuestas en tiempo real

## 📞 Contacto

**María Jesús Camino Cerdán**
- Email: camino.chus@gmail.com
- Teléfono: +34 610 750 098

---

**Fecha de creación:** Enero 2026
**Versión:** 1.0
