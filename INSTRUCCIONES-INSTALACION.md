# 🚀 GUÍA DE INSTALACIÓN - NEXUS CMS

## 📦 Contenido del Paquete

Tu sitio ahora incluye:
- ✅ Página web principal (`index.html`)
- ✅ Panel de administración CMS (`/admin`)
- ✅ Configuración de Netlify CMS
- ✅ Estructura de carpetas para contenido
- ✅ Artículo de ejemplo

## 🎯 PASOS PARA PUBLICAR

### 1️⃣ Preparar el Repositorio en GitHub

**A. Crear cuenta en GitHub** (si no tienes)
   - Ve a https://github.com
   - Crea una cuenta gratuita

**B. Crear nuevo repositorio**
   - Click en "New repository"
   - Nombre: `nexus-site` (o el que prefieras)
   - Marca como **Public**
   - NO añadas README, .gitignore ni license
   - Click en "Create repository"

**C. Subir los archivos**

Opción 1 - Desde la web (más fácil):
1. En tu repositorio, click en "uploading an existing file"
2. Arrastra TODA la carpeta `nexus-cms`
3. Escribe un mensaje: "Initial commit"
4. Click en "Commit changes"

Opción 2 - Con Git (si lo tienes instalado):
```bash
cd nexus-cms
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/nexus-site.git
git push -u origin main
```

### 2️⃣ Conectar con Netlify

**A. Crear cuenta en Netlify**
   - Ve a https://app.netlify.com
   - Regístrate con tu cuenta de GitHub
   - Autoriza el acceso

**B. Importar desde GitHub**
   - Click en "Add new site" → "Import an existing project"
   - Selecciona "Deploy with GitHub"
   - Autoriza a Netlify
   - Busca tu repositorio `nexus-site`
   - Click en el repositorio

**C. Configurar deploy**
   - Build command: (dejar vacío)
   - Publish directory: `.` (punto)
   - Click en "Deploy site"

¡Tu sitio estará online en 1-2 minutos! 🎉

### 3️⃣ Activar el CMS (Panel de Administración)

**A. Habilitar Netlify Identity**
   1. En el dashboard de tu sitio en Netlify
   2. Ve a "Site configuration" → "Identity"
   3. Click en "Enable Identity"

**B. Habilitar Git Gateway**
   1. En la misma sección de Identity
   2. Scroll down hasta "Services"
   3. Click en "Enable Git Gateway"

**C. Configurar registro**
   1. En "Identity" → "Settings and usage"
   2. En "Registration preferences" → Selecciona "Invite only"
   3. Guarda los cambios

**D. Invitarte a ti mismo**
   1. Ve a "Identity" tab
   2. Click en "Invite users"
   3. Escribe tu email
   4. Revisa tu correo y acepta la invitación
   5. Crea tu contraseña

### 4️⃣ Acceder al Panel de Administración

1. Ve a: `https://TU-SITIO.netlify.app/admin/`
2. Inicia sesión con tu email y contraseña
3. ¡Ya puedes gestionar tu contenido! 🎊

## 📝 CÓMO USAR EL PANEL DE ADMINISTRACIÓN

### Añadir un Artículo
1. En el panel, click en "Artículos"
2. Click en "New Artículos"
3. Completa:
   - Título
   - Fecha de publicación
   - Tiempo de lectura (ej: "15 min")
   - Descripción corta
   - Contenido (puedes usar Markdown)
   - PDF adjunto (opcional)
4. Click en "Publish" → "Publish now"

Los cambios se publican automáticamente en 1-2 minutos.

### Añadir un Podcast
1. Click en "Podcasts"
2. Click en "New Podcasts"
3. Completa los campos
4. Sube el archivo MP3
5. Publish

### Añadir un Video
1. Click en "Videos"
2. Completa información
3. Puedes poner URL de YouTube/Vimeo o subir archivo
4. Publish

### Añadir un PDF Descargable
1. Click en "Recursos (PDFs)"
2. Completa información
3. Sube el PDF
4. Publish

## 🎨 PERSONALIZAR EL SITIO

### Cambiar colores
Edita las variables CSS en `index.html` (líneas 11-18):
```css
--accent-cyan: #00fff9;    /* Color principal */
--accent-purple: #9d4edd;  /* Color secundario */
--accent-gold: #ffd60a;    /* Color de acentos */
```

### Cambiar textos del hero
Edita el HTML en la sección `<section class="hero">` (línea ~530)

### Añadir redes sociales
Edita el footer con tus enlaces reales (línea ~700+)

## 🔧 ESTRUCTURA DE ARCHIVOS

```
nexus-cms/
├── index.html              # Página principal
├── admin/
│   ├── index.html         # Panel de admin
│   └── config.yml         # Configuración del CMS
├── articulos/             # Artículos en Markdown
├── media/
│   ├── podcast/          # Archivos de podcast
│   ├── video/            # Archivos de video
│   └── uploads/          # Imágenes subidas
├── recursos/             # PDFs descargables
├── config/
│   └── site.json         # Configuración general
└── netlify.toml          # Config de Netlify
```

## 🆘 SOLUCIÓN DE PROBLEMAS

**Problema: "Page not found" al acceder a /admin**
- Solución: Asegúrate de que los archivos estén en la carpeta `admin/`

**Problema: No puedo iniciar sesión en /admin**
- Solución: Verifica que Git Gateway esté activado en Netlify

**Problema: Los cambios no se reflejan**
- Solución: Espera 1-2 minutos. Netlify necesita reconstruir el sitio

**Problema: "Error loading config.yml"**
- Solución: Verifica que `admin/config.yml` esté correctamente subido

## 🎓 RECURSOS ADICIONALES

- **Documentación de Netlify CMS:** https://www.netlifycms.org/docs
- **Markdown Guide:** https://www.markdownguide.org
- **Soporte de Netlify:** https://answers.netlify.com

## 🚀 PRÓXIMOS PASOS

Una vez que todo funcione:

1. **Personaliza el diseño** editando index.html
2. **Añade tu primer artículo real** desde /admin
3. **Sube tus PDFs, audios y videos**
4. **Conecta un dominio custom** (opcional, ~10€/año)
5. **Comparte tu sitio** con el mundo

---

¿Problemas o dudas? El CMS puede tardar unos minutos en configurarse la primera vez. ¡Paciencia! 💪
