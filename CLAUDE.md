# CLAUDE.md — DIY Yard Pro

> Este archivo es el contexto principal del proyecto para Claude Code.
> Léelo completo antes de hacer cualquier cambio al codebase.

---

## 🌱 Qué es este proyecto

**DIY Yard Pro** (`diy-yard-pro.com`) es un blog de landscaping y hardscaping DIY dirigido a propietarios de casas en EE.UU. que quieren hacer sus propios proyectos exteriores sin contratar un profesional.

El propietario del sitio (**Arturo**) tiene más de 10 años de experiencia profesional en landscaping y hardscaping. El contenido está escrito desde esa perspectiva — consejos reales de alguien que ha hecho el trabajo de campo, no teoría de internet.

**Objetivo del negocio:** generar ingresos pasivos a través de:
1. **Affiliate marketing** — Amazon Associates, Home Depot, Lowe's
2. **Google AdSense** — display ads en los artículos
3. **Newsletter** — captura de emails con MailerLite para email marketing futuro

El sitio está deployado en **Netlify** via **GitHub** (push automático desde el repo).

---

## 🏗️ Stack técnico

- **HTML/CSS/JS puro** — sin frameworks, sin WordPress, sin build step
- **Netlify** — hosting y deploy automático desde GitHub
- **GitHub Desktop** — workflow de control de versiones
- **MailerLite** — newsletter y captura de emails
- **Google Analytics 4** — ID: `G-K663C48D8T`
- **Google AdSense** — Publisher ID: `ca-pub-2556661491647206`
- **Amazon Associates** — programa de afiliados principal

No hay Node.js, no hay npm, no hay webpack. Todo es HTML estático.

---

## 📁 Estructura del proyecto

```
diy-yard-pro/
├── index.html                          # Homepage principal
├── CLAUDE.md                           # Este archivo
│
├── assets/
│   ├── css/
│   │   ├── main.css                    # Estilos de la homepage
│   │   └── article.css                 # Estilos compartidos de todos los artículos
│   ├── js/
│   │   └── main.js                     # JavaScript general (mínimo)
│   └── images/                         # Imágenes del sitio
│
├── articles/                           # Todos los artículos del blog
│   ├── stone-patio-construction.html
│   ├── low-maintenance-landscaping.html
│   ├── budget-backyard-makeover.html
│   ├── garden-walkway-construction.html
│   ├── raised-garden-beds.html
│   ├── outdoor-lighting-design.html
│   ├── retaining-wall-construction.html
│   ├── lawn-care-basics.html
│   ├── garden-bed-edging.html
│   └── complete-mulching-guide.html
│
├── privacy-policy.html
├── terms-of-service.html
├── sitemap.xml
├── robots.txt
├── netlify.toml
└── _redirects
```

> **Regla crítica:** NUNCA escribas CSS inline en los artículos. Todo el CSS va en `assets/css/article.css`. Los artículos solo tienen `<link rel="stylesheet" href="../assets/css/article.css">`.

---

## ✅ Estado actual del proyecto

### Artículos completos (con diseño profesional + SEO completo)
1. **Stone Patio Construction** — artículo flagship, el más completo, con product cards de Amazon
2. **Low-Maintenance Landscaping** — guía de plantas y diseño
3. **Budget Backyard Makeover** — transformación económica
4. **Garden Walkway Construction** — caminos decorativos
5. **Raised Garden Beds** — huertos elevados
6. **Outdoor Lighting Design** — iluminación exterior con comparativas

### Artículos adicionales (creados, pueden necesitar revisión de diseño)
7. Retaining Wall Construction
8. Lawn Care Basics
9. Garden Bed Edging
10. Complete Mulching Guide

### Infraestructura completada
- ✅ `main.css` y `article.css` externos (no CSS inline)
- ✅ Google Analytics en todos los artículos
- ✅ Google AdSense integrado
- ✅ Open Graph tags (Facebook/LinkedIn previews)
- ✅ Schema.org JSON-LD markup (SEO estructurado)
- ✅ Meta descriptions optimizadas por artículo
- ✅ Canonical URLs en todos los artículos
- ✅ `sitemap.xml` con todos los artículos
- ✅ `robots.txt` configurado
- ✅ `netlify.toml` optimizado
- ✅ Newsletter signup con MailerLite
- ✅ Privacy Policy y Terms of Service
- ✅ Lead magnet PDF: "10 Weekend Projects Under $500"

### Pendiente (lo más urgente)
- ⚠️ **Links de afiliados NO están activos** — los product cards existen pero sin URLs reales de Amazon Associates / Home Depot
- ⚠️ Redes sociales (YouTube, Instagram, Pinterest) no conectadas todavía
- ⚠️ Artículos 7–10 necesitan verificación de diseño para que coincidan con los 6 primeros

---

## 🎨 Design system

### Colores (CSS variables en `article.css` y `main.css`)
```css
--primary: #1a5f3a        /* Verde oscuro — color principal */
--secondary: #2d8659      /* Verde medio */
--accent: #ff6b35         /* Naranja — CTAs y highlights */
--accent-light: #ffa366
--bg-light: #f9fafb
--bg-cream: #fffef9
--text-dark: #1f2937
--text-gray: #4b5563
--text-light: #6b7280
--border: #e5e7eb
--shadow: 0 4px 12px rgba(0,0,0,0.1)
--radius: 12px
```

### Tipografía
- Font principal: `Inter` (Google Fonts)
- Fallback: `-apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`

### Componentes estándar de los artículos
Cada artículo tiene estos bloques en orden:
1. `<header>` — navegación con link de regreso a homepage
2. **Hero section** — imagen de fondo, título H1, breadcrumb, categoría badge, autor, fecha
3. **Quick stats box** — (ej: Difficulty, Time, Cost) — cajita de 3 columnas
4. **Intro paragraph** — por qué importa este proyecto
5. **Materials list** — lista de materiales con costos estimados
6. **Step-by-step** — pasos numerados con `.step-card` components
7. **Pro tips** — cajas `.tip-box` con fondo verde claro
8. **Warning boxes** — `.warning-box` con fondo amarillo para advertencias
9. **Product cards grid** — máximo 6 productos, con imagen, precio estimado, rating y link de Amazon
10. **Ad spaces** — bloques de AdSense posicionados estratégicamente
11. **Related articles** — 3 artículos relacionados
12. **Newsletter CTA** — formulario de MailerLite
13. `<footer>` — links de navegación y legal

---

## 💰 Monetización

### Amazon Associates
- Cuenta activa de Amazon Associates
- **Associate ID: `theart198604-20`**
- Los links deben usar el formato: `https://www.amazon.com/dp/ASIN?tag=theart198604-20`
- Disclosure required: el banner "Affiliate Disclosure" ya está en todos los artículos
- Productos prioritarios por artículo: herramientas, materiales, equipos de landscaping

### Google AdSense
- Publisher ID: `ca-pub-2556661491647206`
- Placement: 1 ad después del intro, 1 ad a mitad del artículo, 1 ad al final
- No saturar — máximo 3 ads por artículo

### Home Depot / Lowe's Affiliates
- Pendiente de activar — los artículos de materiales son ideales para esto

---

## 🚀 Roadmap — Lo que queremos construir

### Fase 1 — Completar la base (AHORA)
- [ ] Activar todos los links de afiliados de Amazon en los 10 artículos
- [ ] Verificar que artículos 7–10 tienen el mismo diseño profesional que 1–6
- [ ] Conectar redes sociales en el footer (YouTube, Instagram, Pinterest)
- [ ] Auditar que todos los artículos tienen Analytics, AdSense, Schema.org y Open Graph

### Fase 2 — Contenido nuevo
- [ ] Artículos nuevos (hay ideas para 15+ más en categorías: patios, walkways, lighting, lawn care, seasonal)
- [ ] Página "About" con historia de Arturo y su experiencia profesional
- [ ] Página de categorías por tipo de proyecto
- [ ] Página de búsqueda del sitio

### Fase 3 — Canal de YouTube / TikTok (en desarrollo)
- [ ] El blog ya tiene suficiente contenido para ser el guión de videos
- [ ] Cada artículo existente = un video potencial
- [ ] Videos enlazan al blog → blog enlaza a videos → sinergia de tráfico
- [ ] Prioridad: YouTube para búsqueda de largo plazo, TikTok/Reels para alcance

### Fase 4 — Optimización y escala
- [ ] SEO técnico avanzado: Core Web Vitals, page speed
- [ ] Minificación de CSS/JS para mejorar performance en Netlify
- [ ] Imágenes optimizadas con formatos modernos (WebP)
- [ ] Página de newsletter con el lead magnet PDF
- [ ] Email sequences automatizadas en MailerLite
- [ ] Posible integración con Pinterest (landscaping tiene tráfico enorme ahí)

---

## 🛠️ Cómo trabajar en este proyecto

### Antes de editar cualquier archivo
1. Verifica que el CSS no está siendo duplicado inline — todo debe ir en `article.css`
2. Cuando modifiques estilos globales, edita `article.css` (afecta TODOS los artículos — eso es intencional)
3. Si agregas un componente nuevo (ej: un nuevo tipo de caja), agrégalo en `article.css` primero y luego úsalo en el artículo

### Al crear un artículo nuevo
1. Copia `articles/stone-patio-construction.html` como template base — es el más completo
2. Actualiza: título, meta description, canonical URL, Open Graph tags, Schema.org JSON-LD
3. Agrega al `sitemap.xml`
4. Agrega a la sección "Related Articles" de artículos relacionados
5. Agrega al grid de la homepage (`index.html`)

### Al activar un link de afiliado
- Formato Amazon: `<a href="https://www.amazon.com/dp/ASIN?tag=TAG" target="_blank" rel="nofollow sponsored">`
- Siempre `rel="nofollow sponsored"` — requerido por Google y por Amazon Associates TOS
- El `target="_blank"` siempre va con `rel="noopener"` por seguridad

### Deploy
```bash
git add .
git commit -m "descripción del cambio"
git push
# Netlify detecta el push y hace deploy automático en ~1 minuto
```

---

## 📌 Notas importantes

- **No cambies el esquema de colores** sin consultar — el verde/naranja es la identidad del sitio
- **No elimines los disclosure banners** de afiliados — son obligatorios legalmente
- **No borres el código de Analytics ni AdSense** de los artículos
- **El sitio no usa WordPress** — todo es HTML estático, no hay base de datos, no hay PHP
- **Audiencia objetivo:** homeowners americanos con casa propia, mayores de 30, que hacen proyectos DIY los fines de semana
- **Tono del contenido:** profesional pero accesible, "un contractor amigo que te da consejos reales"

---

*Última actualización del CLAUDE.md: Mayo 2026*
*Proyecto iniciado: Octubre 2025*