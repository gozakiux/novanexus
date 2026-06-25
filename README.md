# NovaNexus — Landing del Diplomado de Actualización en Psicoterapia

Sitio web (landing page de una sola página) para **NovaNexus**, Centro de Formación de Psicoterapeutas en Lima, Perú. Promociona el **Diplomado de Actualización en Psicoterapia «La Resiliencia del Amor»** (enfoque TENCA) y capta interesados.

- 🌐 **En vivo:** https://gozakiux.github.io/novanexus/
- 📦 **Repo:** https://github.com/gozakiux/novanexus (cuenta GitHub: `gozakiux`)
- 📱 **Contacto del negocio:** WhatsApp **+51 941 658 517** · correo **admision@novanexus.pe**

> Este repo es **independiente**. No tiene relación con modelo.pe ni con otros proyectos. Trabaja solo dentro de esta carpeta.

---

## 1. Qué es / Stack

- **HTML puro, todo en UN archivo** (`index.html`). El CSS va embebido en un `<style>` y el JavaScript en `<script>`. **No hay archivos .css ni .js externos. No hay framework, build, ni backend.**
- Se abre en cualquier navegador o se sirve como estático. Se publica en **GitHub Pages**.
- **Fuentes:** Google Fonts — *Fraunces* (serif display) + *Plus Jakarta Sans* (texto). Se cargan por `<link>`.
- **Formulario:** usa **FormSubmit** (servicio externo, sin servidor) para enviar los datos a `admision@novanexus.pe`, con respaldo a WhatsApp si falla.

### Estructura de archivos
```
novanexus/
├── index.html                      ← TODO el sitio (HTML + CSS + JS embebidos) ~739 líneas
├── assets/
│   ├── novanexus-logo.png          ← logo oficial a color (589×396) — nav, hero
│   ├── novanexus-logo-white.png    ← logo blanco (252×179) — footer
│   ├── brochure-novanexus.pdf      ← brochure del programa (enlazado en el sitio)
│   └── ponentes/
│       ├── baldeon.jpg             ← Dr. José Baldeón (director)
│       ├── linares.jpg             ← Dr. Juan Luis Linares (España)
│       ├── cebeiro.jpg             ← Dr. Marcelo Ceberio (Argentina)
│       └── medina.jpg              ← Dr. Raúl Medina (México)
├── robots.txt                      ← SEO
├── sitemap.xml                     ← SEO
├── .nojekyll                       ← evita el procesado Jekyll en GitHub Pages
├── README.md                       ← este archivo
└── CLAUDE.md                       ← reglas rápidas para el agente (léelo primero)
```

---

## 2. Secciones / funciones de la página

1. **Nav** sticky con blur, logo a color, enlaces ancla y botón WhatsApp. Menú hamburguesa en móvil.
2. **Hero** — logo oficial en tarjeta limpia + titular profesional + 2 CTA + 3 stats.
3. **Ribbon** — banda violeta con la tesis: *«El desamor enferma. El Amor sana.»*
4. **Diplomado** (`#diplomado`) — 4 características + CTA (Inscribirme / **Ver brochure PDF** / Detalles por WhatsApp).
5. **Estructura** (`#estructura`) — modalidad (mixta + Google Classroom) y cómo es la matrícula.
6. **Enfoque** (`#enfoque`) — comparación *El amor que sana* vs *El desamor que enferma* (modelo TENCA).
7. **Plana Docente** (`#docentes`) — Dr. Baldeón (director) + 3 ponentes internacionales **invitados**, con link al perfil de Baldeón.
8. **Misión / Visión** — banda violeta, textos cortos.
9. **Inscripción** (`#inscripcion`) — formulario (Nombre, Apellido, Correo, Celular, Distrito, Profesión u ocupación).
10. **Footer** + **botón WhatsApp flotante** (siempre visible).
- Animaciones de aparición al hacer scroll (IntersectionObserver). Respeta `prefers-reduced-motion`.

---

## 3. La marca (no cambiar sin razón)

- **Logo: oficial y LIMPIO, sin distorsión.** Va en una tarjeta blanca simple. ❌ Nada de medallones circulares que lo recorten, soles, anillos ni "licencias creativas" (el cliente lo rechazó: es marca nueva, necesita reconocerse limpia). El logo es **horizontal (589×396)** → no lo metas en círculos.
- **Estética:** premium editorial **claro** (marfil/crema + acento dorado + violeta/azul de marca). Serif protagonista. **NO debe parecer hecho por IA.** ❌ Evitar: degradados morados sobre blanco, halos/auroras de colores, pastillas de vidrio flotantes, anillos punteados, **emojis**, fuentes manuscritas y frases vacías ("formación con alma"). Usa datos concretos.
- **Tipografía:** Fraunces (títulos) + Plus Jakarta Sans (texto). **No** usar Caveat ni otras manuscritas.
- **Paleta (variables CSS en `:root`):** `--cream #f8f3ea`, `--paper #fffdf9`, `--ink #241a3a`, `--violet-700 #3903b6`, `--purple #7b2fbf`, `--blue #2b8fe0`, `--gold #cdaf72` (sobre oscuro), `--gold-ink #7d5e22` (dorado sobre claro, contraste AA 5.4:1), `--violet-ink #170431` (bandas oscuras), `--wa #1fb457` (WhatsApp).
- **Sistema de botones (mantener consistente):** `btn-gold` = acción principal (inscripción) · `btn-wa` = verde, SIEMPRE para WhatsApp · `btn-line` = secundario gris · `btn-brand`/`btn-ink` = variantes.

---

## 4. Reglas de contenido y copy (CRÍTICO — feedback del cliente)

> El cliente (Rod) revisa el copy. Respeta estas decisiones:

- **Audiencia = profesionales de posgrado** (psicólogos/psicoterapeutas) → lenguaje **académico/profesional**, no para pacientes.
  - ✅ "Te **capacitamos** y entrenamos" · ❌ "te acompañamos" (suena a pacientes).
  - Matrícula en términos formales: **Apertura de convocatoria · Incorporación al inicio del programa · Cierre de admisiones**.
- **Producto:** "Diplomado de Actualización en Psicoterapia". Nombre del programa: **«La Resiliencia del Amor»**. Enfoque: **TENCA (Terapia Narrativa Centrada en el Amor)**, "Psicoterapia 2.0 / 4.ª generación". Tesis central: **«El desamor enferma, el Amor sana»**. 3 meses, modalidad mixta (presencial + virtual), aula en Google Classroom, grupos reducidos.
- **Posicionamiento exclusivo:** **NO revelar la cadencia** comercial. (Internamente son ~4 promociones/año, pero en público se dice "convocatoria abierta · cupos limitados", "inicios por convocatoria".) Nunca exponer estrategia interna (LTV, crosselling).
- **Director ≠ ponentes:** el **Dr. José Baldeón** es el director/docente permanente (perfil: https://linktr.ee/doctorjosebaldeon). **Linares, Ceberio y Medina son ponentes INVITADOS de los seminarios que complementan el diplomado, NO docentes permanentes** (los alumnos antes creían que dictaban todo el diplomado). Etiqueta: "Ponentes Internacionales Invitados".
- **Contacto:** WhatsApp **+51 941 658 517** en todos los CTA + botón flotante (`https://wa.me/51941658517`). Correo **admision@novanexus.pe**. ⚠️ **Ignorar "SENDAS / Nuevas Sendas"** que aparezca en documentos viejos del cliente — la marca pública es **solo NovaNexus**.
- **Español:** tildes RAE correctas, "tú" (no voseo), signos de apertura ¿ ¡. Es Perú. (Ver gotcha #7.)

---

## 5. Flujo de trabajo (editar → verificar → publicar)

1. **Editar** `index.html` directamente.
2. **Verificar local** (recomendado): servidor estático en el puerto 3003.
   ```bash
   npx serve . -l 3003 --no-clipboard
   ```
   Abrir `http://localhost:3003`. (En Claude Code, usar las herramientas `preview_*`.)
3. **Publicar:**
   ```bash
   git add -A
   git commit -m "feat/fix: descripción"
   git push            # origin/main → GitHub Pages despliega solo
   ```
4. **Esperar el deploy** (~20s–2min, variable) y abrir el sitio con **Ctrl+Shift+R** (saltarse la caché).

### Verificar que el deploy salió en vivo (sondeo)
```bash
# espera hasta que el HTML en vivo contenga un texto que acabes de cambiar
curl -s "https://gozakiux.github.io/novanexus/?v=$(date +%s)" | grep "tu-texto-nuevo"
# estado del build de Pages:
gh api repos/gozakiux/novanexus/pages/builds/latest
```

---

## 6. ⚠️ COSAS QUE FALLARON (no repetir)

1. **`clamp()` / `calc()` con `+` o `-` SIN espacios = CSS INVÁLIDO.** 🔴 El error más caro.
   - ❌ `clamp(2rem,1rem+2vw,3rem)` → el navegador **descarta la regla entera**.
   - ✅ `clamp(2rem, 1rem + 2vw, 3rem)` → siempre **espacios alrededor de `+` y `-`**.
   - Este bug dejó **TODO el sitio con `padding:0`** (se veía "muy pegado" en todos lados) y los títulos sin escalar, **sin que se notara leyendo el código**. Si algo de espaciado/tamaño "no aplica", sospecha de esto primero.
2. **El formulario (FormSubmit) necesita ACTIVACIÓN única.** El **primer** envío manda un correo de confirmación a `admision@novanexus.pe`; hay que **hacer clic en ese enlace una vez**. Hasta entonces, los leads **no llegan**. (Pendiente de activar por el cliente.)
3. **No sobre-estilizar el logo.** Ya se probó con sol/medallón y el cliente lo rechazó por "distorsión". Mantener el logo oficial limpio en su tarjeta.
4. **El preview/screenshot del entorno es inestable** (timeouts, el server `npx serve` se cae solo). **Verifica por DOM** (`preview_eval` / `preview_inspect` — estilos computados, posiciones, texto) en vez de depender de capturas. Es más fiable.
5. **GitHub Pages tarda variable** en desplegar (visto entre ~15s y ~2min). No asumas que ya está: **sondea el HTML en vivo** con cache-bust (`?v=timestamp`) o revisa el build con `gh api`.
6. **Caché del navegador:** los cambios no se ven sin **Ctrl+Shift+R**. Si el cliente dice "no veo el cambio", casi siempre es caché.
7. **Tildes en español:** Claude tiende a omitir tildes (bug conocido). Revisa el copy visible: educación, formación, práctica, psicología, admisión, sesión, etc.
8. **`<img>` siempre con `width` y `height`** (evita saltos de carga / CLS). Las imágenes actuales ya los tienen.
9. **Saltos de ancla con nav fija:** las secciones tienen `scroll-margin-top:84px` para que el título no quede tapado por la barra sticky. Mantenlo si agregas secciones.
10. **`autocrlf` en Windows:** Git avisa "LF will be replaced by CRLF". Es inofensivo. Se usa `git -c core.autocrlf=false commit` para evitar ruido.

---

## 7. Pendientes / mejoras futuras

- [ ] **Activar FormSubmit** (1 clic en el correo de confirmación) para que lleguen los leads.
- [ ] **Dominio propio** `novanexus.pe` apuntando a GitHub Pages (CNAME + DNS).
- [ ] **Favicon/apple-touch-icon** cuadrado propio (hoy se usa el logo rectangular).
- [ ] Idea del cliente: flujo de **"llamada de admisión"** (agendar una llamada de evaluación en vez de solo dejar datos).

---

## 8. Calidad / accesibilidad (estado actual: ✅ auditado)

- Contraste AA en todo (dorado 5.4:1, violeta 10.2:1, texto suave 6:1, placeholder 4.85:1).
- 1 solo `<h1>`, jerarquía de encabezados correcta, `<main>` + skip-link, landmarks nombrados.
- Imágenes con alt + dimensiones; íconos decorativos con `aria-hidden`; foco visible.
- Responsive verificado (sin overflow horizontal en 375px y desktop). `prefers-reduced-motion` respetado.
- SEO: title/description con keyword local, canonical, Open Graph + Twitter, JSON-LD (EducationalOrganization + Course), robots + sitemap.

### Herramientas/skills útiles para este proyecto
- `redaccion-espanol` (tildes/ortografía), `frontend-design` (diseño), `anthropic-skills:web-design-guidelines` (auditoría), `anthropic-skills:docx` / `pptx` (leer documentos del cliente), `anthropic-skills:pdf` (brochure).

---

*Hecho para NovaNexus. Lima, Perú.*
