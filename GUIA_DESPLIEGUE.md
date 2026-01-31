# 🚀 GUÍA RÁPIDA DE DESPLIEGUE - C³ CONSULTORÍA

## ⏱️ MÉTODO MÁS RÁPIDO (2 MINUTOS) - NETLIFY DROP

### Pasos:
1. **Descarga** la carpeta `c3-consultoria-web` completa a tu ordenador
2. **Ve a:** https://app.netlify.com/drop
3. **Arrastra** la carpeta completa a la ventana del navegador
4. **¡LISTO!** Tendrás una URL como: `https://nombre-aleatorio.netlify.app`

### Para personalizar el dominio:
- Crea cuenta en Netlify (gratis)
- Reclama el sitio
- Cambia el nombre del dominio en configuración

---

## 🏆 MÉTODO PROFESIONAL (5 MINUTOS) - VERCEL + GITHUB

### Paso 1: Crear cuenta en GitHub (si no tienes)
1. Ve a: https://github.com/signup
2. Crea tu cuenta gratuita

### Paso 2: Crear repositorio
1. Click en el botón **"+"** arriba a la derecha → **"New repository"**
2. Nombre: `c3-consultoria-web`
3. Descripción: `Sitio web C³ Consultoría Estratégica`
4. Marca como **"Public"** (o Private si tienes GitHub Pro)
5. Click en **"Create repository"**

### Paso 3: Subir archivos
**Opción A - Interfaz web (más fácil):**
1. En tu repositorio, click **"uploading an existing file"**
2. Arrastra TODOS los archivos de la carpeta `c3-consultoria-web`
3. Escribe un mensaje: "Primer commit - sitio web C³"
4. Click **"Commit changes"**

**Opción B - Línea de comandos (si sabes usar Git):**
```bash
cd c3-consultoria-web
git init
git add .
git commit -m "Primer commit - sitio web C³"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/c3-consultoria-web.git
git push -u origin main
```

### Paso 4: Desplegar en Vercel
1. Ve a: https://vercel.com/signup
2. Click **"Continue with GitHub"**
3. Autoriza a Vercel
4. Click **"Add New Project"** o **"Import Project"**
5. Busca tu repositorio `c3-consultoria-web`
6. Click **"Import"**
7. Click **"Deploy"** (no cambies nada)
8. **¡LISTO EN 30 SEGUNDOS!**

### Tu sitio estará en:
- URL automática: `https://c3-consultoria-web.vercel.app`
- Puedes cambiarla en Settings → Domains

---

## 🔧 CONFIGURACIÓN POST-DESPLIEGUE

### 1. Configurar Make.com (IMPORTANTE)

Los cuestionarios necesitan que configures los webhooks de Make.com:

**Archivos a editar:**
- `cuestionarios/autonomos-sin-trabajadores.html`
- `cuestionarios/autonomos-con-trabajadores.html`
- `cuestionarios/pyme-basic.html`

**En cada archivo, busca (Ctrl+F):**
```javascript
const MAKE_WEBHOOK_URL = 'https://hook.us1.make.com/TU_WEBHOOK_AQUI';
```

**Reemplaza con tu webhook real de Make.com**

**Para obtener tu webhook:**
1. Ve a Make.com (make.com)
2. Crea un nuevo escenario
3. Añade trigger "Webhooks" → "Custom webhook"
4. Copia la URL que te da
5. Pégala en los archivos HTML

### 2. Dominio personalizado (OPCIONAL)

**Si quieres:** `www.c3consultoria.com` en lugar de `c3-consultoria-web.vercel.app`

**En Vercel:**
1. Ve a tu proyecto → Settings → Domains
2. Añade tu dominio personalizado
3. Configura los DNS según las instrucciones

**Costo:** El dominio cuesta ~10-15€/año (en Namecheap, GoDaddy, etc.)
**El hosting en Vercel sigue siendo GRATIS**

---

## ✅ CHECKLIST FINAL

- [ ] Archivos subidos a GitHub o Netlify
- [ ] Sitio desplegado correctamente
- [ ] Webhooks de Make.com configurados
- [ ] Sitio probado en móvil y desktop
- [ ] Enlaces de cuestionarios funcionando
- [ ] Formulario de contacto probado

---

## 🆘 PROBLEMAS COMUNES

### "Mi página no carga"
- Verifica que `index.html` esté en la raíz del repositorio
- No debe estar dentro de ninguna carpeta

### "Los cuestionarios dan error 404"
- Verifica que la carpeta `cuestionarios/` esté en la raíz
- Los nombres de archivo no deben tener espacios ni caracteres especiales

### "El formulario no envía datos"
- Configura correctamente los webhooks de Make.com
- Verifica que la URL del webhook sea correcta
- Abre la consola del navegador (F12) para ver errores

---

## 📞 SOPORTE

**María Jesús Camino Cerdán**
- Email: camino.chus@gmail.com
- Teléfono: +34 610 750 098

---

**¡ÉXITO CON TU DESPLIEGUE! 🚀**
