---
headingDivider: 1
theme: uncover
class:
  - invert
style: |-
  .columns { display: flex; gap: 1rem; }
  .columns > div { flex: 1 1 0; }
---

# <!--fit--> Keynote
Pablo Núñez
*@pablonete*

![bg left](images/agentcamp-logo.png)


# Pablo Núñez

Software Engineer at GitHub

Miembro de 
- ~~MalagaDnug~~ DotNetMalaga 
- OpenSouthCode
- AzureMalaga 
- MalagaAI 
## @pablonete

<!-- footer: Agentcamp 2026 -->
<!-- paginate: true -->
# <!--fit--> Y esos vídeos, ¿dónde irán?

![w:700](images/saeteros.png)

Bizcocho - [Saetero](https://youtube.com/clip/Ugkx5vroDIDXbeAZQISZT3JM7ktYtkY8ZMBF)

# Fotógrafo aficionado
Reflex, móvil, 360... y vídeos

Adobe Lightroom catalogs
Miles de fotos en HDDs desde 2007

Google Photos 👎

<!-- 
Disfruto más disparando que retocando
Bibliotecario frustrado, me gusta archivar

Usé Google Photos mientras fue gratis
pero nunca lo vi como un reemplazo, not mine
Colecciones dinamicas FTW
-->

# Workflow anterior
Fotos de múltiples fuentes
Cámaras (desde SD)
Móviles (vía OneDrive)
Uso un inbox y luego exporto las 3* a OneDrive

![w:800](mermaid/lightroom.workflow.jpg)

# Etiquetado
<!--
- Rating:
	- 2 estrellas: día
	- 3 estrellas: mes
	- 4 estrellas: año
	- 5 estrellas: best ever
- GPS no es lo mejor
	- No viene de réflex, 360...
	- Difícil buscar
-->
- Rating: 2*, 3*, 4*, 5*
- Tags
	- Personas, mascotas
	- `Playa`, `Bicicleta`, `Baloncesto`, `Fútbol`, `Amanecer`, `Selfie`
- Location por jerarquía:
	- País > Provincia > Ciudad > Lugar

# Cuellos de botella
- Ingestión (volcado lento)
- Etiquetar, varios pasos
- Revisión de ratings 🌟
- Requiere tiempo en el ordenador
- Edición, aunque sea básica: niveles, crop, horizon-level
## Yo

# Atascado
<!-- 
	Modelo de licencia repulsivo
	Soy usuario cautivo
	Cada vez más bloqueado en 2025, voy hacia atrás
	Llego a dejar de tirar fotos por no aumentar la bola de nieve
	Meses dándole vueltas a cómo aprovechar la IA en mi flujo
-->
- Adobe está matando Lightroom $ $ $
- Nueva Insta360 que no encajaba

- Tengo que aprovechar la IA
- Me da vértigo cambiar y decido trazar un plan

# Todo empieza con un Repo
<!--
servir mis fotos via web y catalogar y editar
Desde un PC siempre encendido (bajo consumo!)
-->
Trazo plan con Copilot
- PLAN.md
- Issues
- Project board
# MiniPC
<!--
N5095A
Mi crío me lo devolvió porque no reproducía Youtube
Al poco de empezar, volantazo
/giphy Coche salida autovia
Probé Darktable y no me convenció (además no soporta vídeos)
-->
Recupero MiniPC desahuciado
Celeron N5095A
Hace más de lo que pensaba

![bg right](images/openclaw-telegram-desktop-btop-fullscreen.jpg)

# Omarchy
Modern & Opinionated Linux

![w:600](images/dhh-tweet.png)
<sub>https://x.com/dhh/status/2020156016629797193?s=20</sub>


![bg right](images/omarchy-screenshot.jpg)

# OpenClaw
Tenía que ser open-source
¿El SO de la agéntica?
Modelo complejo de seguridad
Pero sigue teniendo riesgos
![bg right](images/openclaw-screenshot.jpg)

<!-- 
Las cosas cambian muy rápido, Openclaw es una sacudida. Anthropic ha cerrado el grifo esta semana y trastoca lo que mucha gente está haciendo. Pro y contra de ser OpenSource. Viva el OpenSource, es la única forma de hacer esto — una empresa no podría lanzar un producto como Openclaw

Llevo un mes con esto y cuando me planteo hacer la keynote digo "cómo le voy a enseñar yo a nadie". No pretendo que sea una charla en profundidad. No tengo ni siquiera para resolver dudas — solo puedo resolver sobre lo que yo he hecho, no sobre cómo funciona Openclaw, su modelo no es sencillo (modelo de seguridad, modelo de Chrome, modelo de agentes). No es trivial. Yo he conocido lo mínimo que he necesitado para ir haciendo progresos.
-->

# Nace Tenacitas
Su Gmail (no acceso a mi email)
Y su GitHub user
- No co-author, [sus commits](https://github.com/pablonete/agentcamp-2026-keynote/commits/main/slides)
- No PAT para usar mis repos en mi nombre

<div class="columns">
<div>
Pablonete 

![w:300](images/github-mosaic-pablonete.png)

</div>
<div>
Tenacitas

![w:300](images/github-mosaic-tenacitas.png)

</div>
</div>

# Baneada
Google la desactivó
Skill `gog`  *parecía* un bot
Pero apelamos y 🥳
![bg right](images/openclaw-telegram-google-account-recovery.jpg)

# El agente y el modelo

![bg right](images/el-agente-y-el-modelo.jpg)

OpenClaw  agente
orquesta subagentes

Uso **Claude Sonnet 4.6** 
vía GitHub Copilot

<!-- 
OpenClaw es el runtime: gestiona sesiones, skills, canales (Telegram, Discord...).
El "cerebro" es el modelo de lenguaje — en mi caso Claude Sonnet 4.6, accedido gratis a través de GitHub Copilot.
Como cambiar el motor de un coche: el chasis (OpenClaw) es el mismo, el motor (modelo) puede ser otro.
-->
# Modelo en la nube
Under maintenance
En 1 mes esto me ha pasado 2 veces
![bg right:30%](images/openclaw-telegram-model-error-explanation.jpg)

# Immich 🛑
Tu propio Google Photos
auto-hospedado

No es lo que necesito ahora

![bg right](images/immich-screenshot.png)

# digiKam
- Open source 👍
- Face recognition 👍
- Rating and tagging 👍
- Location 👎 (via GPS)

![bg right](images/digikam-screenshot.webp)

# Nuevo Workflow

![w:1200](mermaid/openclaw.workflow.png)

# Nuevo Workflow Skills

![w:1200](mermaid/openclaw.workflow.skills.png)
# Skills de fotos
<style scoped>section { font-size: 32px; }</style>

| Skill                  | Descripción               |
| ---------------------- | ------------------------- |
| /fotos-from-onedrive   | Del Camera roll al Inbox  |
| /sd-to-hdd             | De la tarjeta al Inbox    |
| /photos-digikam-backup | Catálogo sólo             |
| /photos-triage-start   | JSON de fotos para review |
| /photos-triage-commit  | Graba review              |
| /photos-triage-search  | Busca en Digikam          |
| /fotos-to-onedrive     | 3* a OneDrive             |
| /photos-to-movistar    | Raw 360 videos            |

# MCPs

| MCP                | Descripción                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------------- |
| digikam-mcp        | Lee info de sqlite<br>Escribe tags, ratings...<br>Search: ejecuta queries<br>Mueve carpetas |
| movistar-cloud-mcp | Sube archivos a esa nube                                                                    |

# Escala
1. Chat - improvisa
2. Skill - flexible
3. Código - estable

![w:600](images/tweet-matias-3.jpg)
https://x.com/woloski/status/2036251852312903943

<!--
Lo bueno de los skills: son flexibles. Mientras se ejecutan puedes estar opinando y cambiándole el comportamiento sobre la marcha.
-->

# <!--fit--> Paseando a Tenacitas
Algunas de mis conversaciones
con Openclaw en Telegram
# Skills
Nunca consigo que salgan todos
![bg right](images/openclaw-telegram-skills-list-commands.jpg)
# /stop
A veces no ve cosas fáciles
y se lia
![bg right:30%](images/openclaw-telegram-osp-children-start-bug.jpg)

# /fotos-from-onedrive
Arregla el lockscreen caído
![bg right:30%](images/openclaw-telegram-hyprlock-crash-fix.jpg)
# /sd-to-hdd
Volcando de la SD al HDD
![bg right:30%](images/openclaw-telegram-sd-to-hdd-jueves-santo.jpg)
# /sd-to-hdd
Ahora con nombre de evento
![bg right](images/openclaw-telegram-sd-copy-insta360-telegram.jpg)

# Fotos Triage
Custom webapp 
Para el móvil
![bg right:30%](images/photos-triage-seleccion.jpg)
# Fotos Triage
Seleccionar, rating y tags
en cada foto
![bg right:30%](images/photos-triage-grid.jpg)
# Fotos Triage
Guardado en JSON en GitHub
y commitado a DigiKam
![bg right:30%](images/photos-triage-detail.jpg)
# Tailscale
Túnel seguro entre dispositivos
y publicar con HTTPS
![bg right](images/tailscale-screenshot.jpg)

# /photos-triage-search
Skill para buscar fotos
Genera Json
![bg right:30%](images/openclaw-telegram-photos-search-skill-plan.jpg)
# /fotos-to-onedrive
Incluyendo meses
Pide dry-run para validar
![bg right:30%](images/openclaw-telegram-photo-export-digikam-debug.jpg)
# Foto Open
Otra custom webapp
Para compartir fotos
- Public
- Unlisted
![bg right:30%](images/openclaw-telegram-photo-open-share-plan.jpg)
# Movistar Cloud
Descubriendo la API interna
![bg right:30%](images/openclaw-telegram-movistar-sapi-api-discovery.jpg)
# Movistar Cloud
Resolviendo la autenticación
![bg right:30%](images/openclaw-telegram-movistar-sapi-jsessionid.jpg)
# Movistar Cloud
Errores con archivos grandes
Se dio cuenta: usa streaming
![bg right:30%](images/openclaw-telegram-movistar-upload-oom-fix.jpg)
# Movistar Cloud
No recuerdes mi teléfono
¡Que no lo recuerdes!
![bg right:30%](images/openclaw-telegram-movistar-phone-privacy-fix.jpg)
# Vibe coding
Depurando drag & drop via Telegram

> Vibe-coding is working as a QA fulltime.

<sub>https://x.com/pablonete/status/2036878616961638507</sub>

![bg right:30%](images/openclaw-telegram-drag-drop-clip-debug.jpg)

# Vibe coding
<!-- Bajo consumo, suficiente para low-res, VA-API flipping -->
Aprovechando la mini-GPU
para encoding de video 1080p

Hulio, ¿VA-API qué es lo que es?
![bg right:30%](images/openclaw-telegram-video-render-upside-down-fix.jpg)

# Mejoras futuras
- Location desde GPS
- Edición básica, automatizada
- Memory videos
- Auto tagging
- Añadir años pasados
- Publicar open-source MCPs y más

# Retro primer mes
- Niño con juguete nuevo
- Mil ideas
- Velocidad muy alta: olvido cosas
- Estoy usando 5-10% de OpenClaw y es wow
- He montado esto mientras revisé +5500 fotos

# Takeaways
- 🦞 OpenClaw: más posibilidades cuanto más lo usas

- 📷 Fotos: plan, ejecuta, itera, custom

- 📁 Repos: persistencia, visibilidad, coordinación

- 🧠 AGENTS.md vs Skill vs Memoria

- ⚡ Matias: Chat → Skill → Software

- 👺 Vibe-coding, ¿cuándo reviso el código?

# <!--fit-->Gracias 🦞
<!-- color: red -->

@pablonete


