# Librería Neneko — Sitio Web

Sitio web de Librería Neneko. Una sola página HTML, sin dependencias, sin complicaciones.

## 📁 Estructura

```
.
├── index.html          ← El sitio completo (HTML + CSS + JavaScript)
├── package.json        ← Scripts para desarrollo
├── nuevo-logo.png      ← Logo del negocio
├── robots.txt          ← Para buscadores
└── sitemap.xml         ← Mapa del sitio
```

## 🚀 Cómo empezar

### 1. Clonar el repo

```bash
git clone https://github.com/nenekolibreria/libreria-neneko-web.git
cd libreria-neneko-web
```

### 2. Correr localmente

```bash
npm run dev
```

Abrí http://localhost:8000 en tu navegador. Listo.

## 📝 Cambiar datos del negocio

Todo está en **un solo lugar** dentro de `index.html`: la constante `HORARIOS` (está cerca de la línea 2087).

### Horarios

Dentro del `<script>` encontrás:

```javascript
const HORARIOS = [
  { dia: 'Domingo',   bloques: [] },
  { dia: 'Lunes',     bloques: [[720, 1230]] },
  { dia: 'Martes',    bloques: [[720, 1230]] },
  // ... etc
];
```

Los números son minutos desde la medianoche:
- `720` = 12:00 (12 × 60)
- `1230` = 20:30 (20 × 60 + 30)
- `930` = 15:30 (15 × 60 + 30)

**Cambias acá una sola vez** y se actualiza automáticamente en:
- La tabla de horarios de la página
- El cartel de "abierto ahora"
- El JSON-LD para Google

### Ubicación, teléfono, etc.

Están en varios lugares del HTML. Buscá con Ctrl+F:
- `Peña 3102` → ubicación
- `+5491161691209` → teléfono

## 🌐 Publicar en GitHub Pages

1. **Pusheá todo a `main`:**
   ```bash
   git add .
   git commit -m "Contenido inicial"
   git push origin main
   ```

2. **En GitHub**, andá a Settings → Pages
   - Source: Deploy from a branch
   - Branch: `main`
   - Folder: `/ (root)`

3. **Esperá 1-2 minutos** y tu sitio estará en:
   ```
   https://nenekolibreria.github.io/libreria-neneko-web/
   ```

## ✅ Tests (opcional)

Si tenés los tests, corre:

```bash
npm test
```

Verifica que todo esté sincronizado (horarios, colores, etc).

## 🎨 Cambiar colores, logos, etc.

Está todo en `index.html`:
- Colores: dentro del `<style>` (variables `--*`)
- Logo: referencia a `nuevo-logo.png`

## 📱 Cómo funciona

- **Responsive:** se ve bien en celular, tablet y desktop
- **Sin conexión:** el sitio funciona aunque no haya internet
- **Rápido:** carga en menos de 2 segundos
- **SEO:** optimizado para Google

## ❓ Dudas

Cualquier cosa, consultá el archivo original o el comentario en el código.

---

**Última actualización:** Septiembre 2026
