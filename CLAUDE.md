# CLAUDE.md — NovaNexus (léeme primero)

Proyecto: landing page de **NovaNexus** (Centro de Formación de Psicoterapeutas, Lima). **Lee `README.md`** para el detalle completo. Esto es el resumen operativo.

## Qué es
- **Un solo archivo `index.html`** con HTML + CSS (`<style>`) + JS (`<script>`) embebidos. Sin framework, sin build, sin backend. Más `assets/` (logos, fotos de ponentes, brochure PDF) y archivos SEO.
- Hosting: **GitHub Pages** → https://gozakiux.github.io/novanexus/ · repo `github.com/gozakiux/novanexus`.
- Repo independiente: **no mezclar con modelo.pe ni otros proyectos.**

## Reglas que NO se rompen
1. **CSS `clamp()`/`calc()`: SIEMPRE espacios alrededor de `+` y `-`.** `clamp(2rem, 1rem + 2vw, 3rem)`, nunca `clamp(2rem,1rem+2vw,3rem)` (es inválido y anula la regla → rompió TODO el espaciado una vez).
2. **Logo oficial y LIMPIO**, sin distorsión, sin sol/medallón/anillos. Es horizontal (589×396): no meterlo en círculos.
3. **Estética premium clara, NADA de look IA**: sin halos de colores, pastillas de vidrio, emojis, fuentes manuscritas ni frases vacías. Fraunces + Plus Jakarta Sans. Paleta crema/dorado/violeta.
4. **Copy profesional/posgrado**: "te **capacitamos** y entrenamos" (no "te acompañamos"). Matrícula = "Apertura de convocatoria / Incorporación al inicio del programa / Cierre de admisiones".
5. **No revelar la cadencia** comercial (en público: "convocatoria abierta · cupos limitados").
6. **Ponentes (Linares, Ceberio, Medina) = INVITADOS** de seminarios complementarios; **Dr. Baldeón = director permanente**. La marca pública es **solo NovaNexus** (ignorar "SENDAS").
7. **WhatsApp +51 941 658 517** en todo (botón verde `btn-wa`) + correo **admision@novanexus.pe**.
8. **Español con tildes RAE** correctas (revisar siempre; Claude omite tildes).

## Flujo
1. Editar `index.html`. 2. Verificar local (`npx serve . -l 3003`; en Claude Code, `preview_*`, y **verifica por DOM/`preview_eval`** porque los screenshots son inestables). 3. `git add -A && git commit && git push`. 4. GitHub Pages despliega solo (~20s–2min); sondea con `curl ...?v=$(date +%s) | grep`. 5. Recargar con **Ctrl+Shift+R** (caché).

## Pendiente
- **Activar FormSubmit**: el primer envío manda un correo de confirmación a admision@novanexus.pe que hay que clickear una vez, o los leads no llegan.
