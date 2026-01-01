# 🚀 NEXUS CON JEKYLL - GUÍA DE INSTALACIÓN

## ✨ ¿Qué tiene este paquete?

Ahora tu sitio usa **Jekyll**, un generador estático que:
- ✅ Lee automáticamente los archivos `.md` del CMS
- ✅ Genera páginas HTML al instante
- ✅ Se actualiza solo cuando publicas desde `/admin`
- ✅ Es reconocido automáticamente por Netlify
- ✅ Mantiene tu diseño cyber-místico intacto

## 📦 CONTENIDO

```
nexus-jekyll/
├── _config.yml          # Configuración de Jekyll
├── _layouts/            # Plantillas de diseño
├── _posts/              # Tus artículos (se crean desde /admin)
├── _podcast/            # Tus podcasts
├── _video/              # Tus videos
├── _recursos/           # Tus PDFs
├── admin/               # Panel CMS
├── assets/              # CSS y archivos
├── index.html           # Página principal
├── Gemfile              # Dependencias Ruby
└── netlify.toml         # Config Netlify
```

## 🎯 INSTALACIÓN PASO A PASO

### 1️⃣ Subir a GitHub

**Opción A - Arrastar archivos (más fácil):**
1. Ve a tu repositorio en GitHub
2. Click en "Add file" → "Upload files"
3. Arrastra TODA la carpeta `nexus-jekyll` (el contenido, no la carpeta)
4. Commit: "Actualización a Jekyll"

**Opción B - Reemplazar todo:**
1. Borra el contenido actual del repo (o crea uno nuevo)
2. Sube todos los archivos de `nexus-jekyll`

### 2️⃣ Conectar con Netlify

Si ya tienes el sitio en Netlify:
1. Netlify detectará automáticamente que usas Jekyll
2. Reconstruirá el sitio (2-3 minutos)
3. ¡Listo!

Si es nuevo:
1. Login en Netlify
2. "Add new site" → "Import from GitHub"
3. Selecciona el repositorio
4. **Build command**: `jekyll build`
5. **Publish directory**: `_site`
6. Click "Deploy"

### 3️⃣ Activar el CMS

**A. Habilitar Identity:**
- Site configuration → Identity → "Enable Identity"

**B. Habilitar Git Gateway:**
- Identity → Services → "Enable Git Gateway"

**C. Invitarte:**
- Identity tab → "Invite users"
- Pon tu email
- Acepta invitación en correo
- Crea contraseña

### 4️⃣ ¡Publicar contenido!

Ve a: `https://tu-sitio.netlify.app/admin/`

**Para crear un artículo:**
1. Click en "Artículos"
2. "New Artículos"
3. Completa:
   - Título
   - Fecha
   - Tiempo de lectura
   - Descripción
   - Contenido (usa Markdown)
   - PDF (opcional)
4. Click "Publish" → "Publish now"

**En 2-3 minutos aparecerá en tu web automáticamente** 🎉

## 📝 CÓMO FUNCIONA AHORA

### El flujo automático:

```
1. Publicas en /admin
   ↓
2. Netlify CMS guarda en GitHub
   ↓
3. GitHub notifica a Netlify
   ↓
4. Jekyll genera HTML
   ↓
5. Netlify publica el sitio
   ↓
6. ¡Tu contenido está online!
```

**TODO ES AUTOMÁTICO** - Solo publicas y esperas 2-3 minutos.

## ✍️ ESCRIBIR EN MARKDOWN

El contenido se escribe en Markdown. Aquí van los básicos:

```markdown
# Título grande
## Título mediano
### Título pequeño

**Texto en negrita**
*Texto en cursiva*

[Enlace](https://ejemplo.com)

- Lista item 1
- Lista item 2

1. Lista numerada
2. Segundo item

Código en línea: `codigo aquí`

​```python
# Bloque de código
def funcion():
    return "Hola"
​```
```

## 🎨 PERSONALIZAR

### Cambiar colores:
Edita `/assets/css/style.css` líneas 1-10:
```css
--accent-cyan: #00fff9;    /* Color principal */
--accent-purple: #9d4edd;  /* Color secundario */
--accent-gold: #ffd60a;    /* Acentos */
```

### Cambiar textos del hero:
Edita `/index.html` sección hero (línea ~5)

### Añadir redes sociales:
Edita `/_layouts/default.html` en el footer

## 🆘 SOLUCIÓN DE PROBLEMAS

**Problema: El sitio no construye**
- Revisa el log en Netlify → Deploys
- Asegúrate de que todos los archivos estén subidos

**Problema: Los cambios del CMS no aparecen**
- Espera 2-3 minutos (Jekyll tarda en construir)
- Refresca con Ctrl+F5 (limpia caché)
- Revisa en Netlify si hay un deploy en proceso

**Problema: Error 404 en /admin**
- Verifica que la carpeta `admin/` esté en el repo
- Verifica que Git Gateway esté activado

**Problema: No puedo iniciar sesión en /admin**
- Verifica que Identity esté activado
- Verifica que te hayas invitado y aceptado la invitación
- Prueba en modo incógnito (a veces es caché)

## 🎓 RECURSOS

- **Jekyll Docs**: https://jekyllrb.com/docs/
- **Markdown Guide**: https://www.markdownguide.org/
- **Netlify CMS**: https://www.netlifycms.org/docs/

## 🚀 VENTAJAS DE JEKYLL

- ✅ **Super rápido** - genera HTML estático
- ✅ **Sin base de datos** - todo en archivos
- ✅ **Seguro** - no hay backend que hackear
- ✅ **Gratis** - hosting en Netlify sin costo
- ✅ **Simple** - solo Markdown
- ✅ **Versionado** - todo en Git

## 📊 COMPARACIÓN

| Antes (sin Jekyll) | Ahora (con Jekyll) |
|-------------------|-------------------|
| Contenido no aparece | ✅ Aparece automáticamente |
| Editar HTML manualmente | ✅ Panel de administración |
| Subir archivos por FTP | ✅ Todo desde el navegador |
| Sin historial | ✅ Git guarda todo |

## 🎉 SIGUIENTES PASOS

1. **Sube el código** a GitHub
2. **Conéctalo** con Netlify
3. **Activa** Identity + Git Gateway
4. **Publica** tu primer artículo
5. **Comparte** tu sitio con el mundo

---

**¿Dudas?** Revisa los logs en Netlify, casi siempre ahí está la respuesta.

**¡Ahora todo funciona automáticamente!** 🔮✨
