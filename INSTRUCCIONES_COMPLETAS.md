# 📱 Tarjeta Digital Interactiva - Guía Completa

## 🎯 Lo que hemos creado

Una **tarjeta de presentación digital profesional** que:
- ✅ Se abre como "app" en iPhone
- ✅ Muestra tu foto, nombre, puesto, contactos
- ✅ Genera un QR que guarda automáticamente tu contacto
- ✅ Funciona perfectamente en iPhone y Android
- ✅ Usa colores: **Negro profundo + Dorado + Blanco gris claro**

---

## 📦 Archivos Incluidos

- **index.html** → Archivo principal (contiene todo: HTML, CSS, JavaScript)
- **GUIA_RAPIDA.txt** → Pasos en 5 minutos
- **VCARD_EJEMPLO.vcf** → Ejemplo del formato de contacto

---

## 🚀 PASO 1: Crear repositorio en GitHub

### 1.1 Crear nuevo repositorio
1. Ve a https://github.com/new
2. **Nombre del repositorio:** `stiven-quirama-card` (o el que prefieras)
3. **Descripción:** "Tarjeta digital de presentación"
4. **Público** ✓
5. Click en "Create repository"

### 1.2 Cargar el archivo
1. En tu nuevo repositorio, click en "Add file" → "Upload files"
2. Arrastra o selecciona el archivo `index.html` (el que tienes)
3. Commit message: "Agregar tarjeta digital"
4. Click en "Commit changes"

---

## 🌐 PASO 2: Configurar GitHub Pages

### 2.1 Habilitar Pages
1. Ve a **Settings** del repositorio
2. En el menú izquierdo, busca **"Pages"**
3. En "Source", selecciona: **main** (o master)
4. Click en **Save**
5. Espera 2-3 minutos

### 2.2 Tu URL será:
```
https://[tu-usuario-github].github.io/stiven-quirama-card/
```

**Ejemplo:**
```
https://stiven-quirama.github.io/stiven-quirama-card/
```

---

## 📸 PASO 3: Integrar tu Foto

### Opción A: Subir foto a GitHub (RECOMENDADO)

1. **Prepara tu foto:**
   - Tamaño: 400x400px o similar (cuadrada)
   - Formato: JPG o PNG
   - Fondo: Preferentemente uniforme

2. **Sube la foto:**
   - Ve a tu repositorio
   - Click en "Add file" → "Upload files"
   - Selecciona tu foto y nómbrala: `perfil.jpg`
   - Commit

3. **Actualiza index.html:**
   - Abre `index.html` en tu repositorio
   - Click en el lápiz ✏️ para editar
   - Busca esta línea (búscalo por "profile-photo"):
   ```html
   <img src="https://via.placeholder.com/100?text=STIVEN&bg=D4AF37&fc=1A1A1A" alt="Stiven Quirama Orozco" class="profile-photo">
   ```
   - Reemplazala con:
   ```html
   <img src="perfil.jpg" alt="Stiven Quirama Orozco" class="profile-photo">
   ```
   - Commit los cambios

### Opción B: Usar URL externa
Si tu foto está en Google Drive, OneDrive, etc., puedes usar la URL directa:
```html
<img src="https://tu-url-externa/foto.jpg" alt="Stiven Quirama Orozco" class="profile-photo">
```

---

## ⚙️ PASO 4: Personalizar Datos (Opcional)

Si necesitas cambiar algo más, edita el archivo `index.html`:

### Cambiar datos de contacto:
Busca el objeto `contact` en el código JavaScript y actualiza:
```javascript
const contact = {
    name: "Stiven Quirama Orozco",           // Tu nombre
    position: "Responsable de Mantenimiento", // Tu puesto
    company: "Bodegas Care",                  // Empresa
    email: "mantenimiento@bodegascare.com",  // Tu email
    phone: "+34722894100",                   // Tu teléfono
    linkedin: "https://www.linkedin.com/in/stiven-quirama-orozco-690b72265", // LinkedIn
    website: ""  // Página web (cuando esté lista)
};
```

### Cambiar colores corporativos:
Busca las variables CSS:
```css
:root {
    --primary: #1A1A1A;      /* Color principal (Negro) */
    --secondary: #D4AF37;    /* Color secundario (Dorado) */
    --accent: #4A4A4A;       /* Color acento (Gris) */
    --light-bg: #F5F5F5;     /* Fondo claro */
}
```

---

## 🔗 PASO 5: El QR Explicado

### ¿Cómo funciona?

1. **El QR contiene un vCard (formato estándar de contactos)**
   - Es un código en formato base64
   - Incluye toda tu información de contacto

2. **Cuando alguien escanea:**
   - iPhone: Le pregunta "Añadir contacto" automáticamente ✓
   - Android: Mismo proceso automático ✓
   - Se guarda TODO en su agenda

### ¿Qué incluye el QR?
- Nombre completo
- Puesto/cargo
- Empresa
- Teléfono
- Email
- LinkedIn
- Nota con tu rol

---

## 💾 PASO 6: Usar la Tarjeta

### En tu iPhone:
1. Abre la URL en Safari
2. Click en el botón **Compartir** (↗️)
3. Selecciona "Añadir a pantalla de inicio"
4. Tu nombre + "Card"
5. ¡Listo! Tendrás un ícono en tu pantalla de inicio

### Para compartir con otros:
1. **Escanean tu QR:** Automáticamente les añades como contacto
2. **Botón "Compartir":** Pueden mandar el link por WhatsApp, email, etc.
3. **Botón "Guardar Contacto":** Descarga un archivo .vcf que pueden importar

---

## 🎨 Características Técnicas

### Front-end
- **HTML5** con meta tags optimizados para iPhone
- **CSS3** responsive y moderno
- **JavaScript vanilla** (sin dependencias externas)

### Librerías usadas
- **QRCode.js** (CDN) → Genera códigos QR
- **vCard formato 3.0** → Estándar internacional de contactos

### Compatibilidad
- ✅ iPhone 8+
- ✅ iPad
- ✅ Android 5+
- ✅ Navegadores modernos (Chrome, Firefox, Safari, Edge)

### Funcionalidades
- 📱 Web App (se abre como app)
- 🔗 Links clickeables (email, teléfono, LinkedIn)
- 📤 Botón compartir nativo
- ⬇️ Descarga vCard (.vcf)
- 🎯 QR responsive
- 📸 Foto redonda con borde dorado

---

## 🔍 Verificación

### Probar el QR
1. Abre tu página en un dispositivo
2. Toma una captura de pantalla del QR
3. En iPhone: Abre Fotos → Mira la captura → Toca la notificación del QR
4. En Android: Abre Google Lens o la cámara → Enfoca el QR

### Verificar que funciona
- [ ] La página se carga correctamente
- [ ] La foto aparece
- [ ] Los datos de contacto están correctos
- [ ] El QR se escanea sin problemas
- [ ] Al escanear, ofrece guardar como contacto
- [ ] Los botones funcionan
- [ ] Se ve bien en móvil

---

## 📞 URLs Importantes

**Tu tarjeta en vivo:**
```
https://[tu-usuario].github.io/stiven-quirama-card/
```

**Para actualizar:** 
Edita `index.html` en tu repositorio

**Para agregar foto:**
Sube `perfil.jpg` al mismo nivel que `index.html`

---

## ❓ Solución de Problemas

### El QR no escanea
- ✓ Asegúrate que la pantalla sea clara
- ✓ Usa buena iluminación
- ✓ Aumenta el zoom del QR en tu dispositivo

### La foto no se ve
- ✓ Verifica que el archivo esté en el repositorio
- ✓ Revisa que el nombre coincida exactamente
- ✓ Abre las herramientas de desarrollador (F12) y mira errores

### Los datos no actualizan
- ✓ Haz cambios en `index.html`
- ✓ Commit los cambios
- ✓ Espera 1-2 minutos
- ✓ Recarga la página (Ctrl+Shift+R o Cmd+Shift+R)

### No funciona el compartir
- ✓ El navegador debe estar actualizado
- ✓ Algunos navegadores antiguos no lo soportan
- ✓ Botón de guardar contacto siempre funciona

---

## 🎁 Bonus: Próximas Mejoras

Cuando tengas lista la web de Bodegas Care, puedes:
1. Cambiar `linkedin` por tu sitio web
2. Agregar un campo `website` con la URL
3. Actualizar el color si lo necesitas

---

## 📋 Resumen de Pasos

```
1️⃣  Crear repo en GitHub
2️⃣  Subir index.html
3️⃣  Activar GitHub Pages (Settings → Pages)
4️⃣  Subir tu foto (perfil.jpg)
5️⃣  Editar index.html → cambiar URL de foto
6️⃣  ¡LISTO! Comparte tu URL 🎉
```

---

**¡Tu tarjeta digital está lista! 🚀**

Cualquier pregunta, puedo ajustar colores, datos, o agregar más funcionalidades.