# Publicar la app de Stock en GitHub Pages (como PWA instalable)

Tenés 6 archivos en la carpeta `pwa_stock`:
`index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`.
**Todos van juntos, en la raíz del repo** (sin carpetas adentro).

---

## 1. Crear el repo nuevo
1. En GitHub: **New repository**.
2. Nombre: por ejemplo `stock` (será parte de la URL).
3. Public. (GitHub Pages gratis necesita repo público).
4. Create repository.

## 2. Subir los 6 archivos
- En el repo: **Add file → Upload files**.
- Arrastrá los 6 archivos (NO una carpeta — los archivos sueltos).
- **Commit changes**.

## 3. Activar GitHub Pages
1. En el repo: **Settings → Pages**.
2. En "Source" elegí **Deploy from a branch**.
3. Branch: **main**, carpeta **/(root)**. Save.
4. Esperá 1–2 minutos. Arriba te muestra la URL publicada, algo como:
   `https://TU_USUARIO.github.io/stock/`

## 4. Abrir e instalar
1. Entrá a esa URL desde Chrome o Edge.
2. Va a aparecer el botón **⤓ Instalar app** arriba (o el ícono de instalar
   en la barra de direcciones). Hacé clic → Instalar.
3. Queda como app con su ícono, en ventana propia, en cada computadora.

## 5. Conectar a tu planilla (una vez por PC)
- Clic en **⚙ Conexión**, pegá tu URL de Apps Script (la de siempre,
  termina en `/exec`), **Probar conexión** → **Guardar y conectar**.

---

## Actualizar la app más adelante
Cuando tengas una versión nueva del `index.html`:
1. Subí el archivo nuevo al repo (Add file → Upload → reemplaza).
2. **Importante:** abrí `sw.js`, cambiá `stock-v1` por `stock-v2`
   (subí el número), y commiteá. Eso obliga a las computadoras a tomar
   la versión nueva la próxima vez que abran.

## Notas
- Los datos NO están en GitHub. Viven en tu planilla de Google. GitHub solo
  aloja la "ventana" (la app). Por eso el repo puede ser público sin riesgo:
  no contiene datos del negocio.
- La URL de Apps Script (la `/exec`) NO va en estos archivos; se guarda
  localmente en cada computadora cuando la pegás en ⚙ Conexión. No la subas al repo.
