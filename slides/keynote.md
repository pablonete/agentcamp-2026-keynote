---

---
<!--
headingDivider: 1
theme: uncover
class: 
  - invert
style: |
[]()  .columns { display: flex; gap: 1rem; }
  .columns > div { flex: 1 1 0; }
-->

# Keynote

![bg left](images/agentcamp-logo.png)


# <!--fit--> ¿Esas fotos, dónde irán?
Bizcocho - Saeteros
https://youtube.com/clip/Ugkx5vroDIDXbeAZQISZT3JM7ktYtkY8ZMBF

# Presentación
Software Engineer at GitHub
Member of ~~MalagaDnug~~ DotNetMalaga AzureMalaga OpenSouthCode

<!-- footer: Agentcamp 2026 -->
<!-- paginate: true -->
# Fotógrafo
Nikon D40
Nikon D5500
Sony A6000
Insta360 X3

Fotógrafo compulsivo

Lightroom
# 
Disfruto más disparando que retocando
Bibliotecario frustrado, me gusta archivar

# Catálogos
Miles de fotos en HDDs desde 2007
Usé Google Photos mientras fue gratis
pero nunca lo vi como un reemplazo, not mine

# Workflow
Fotos de múltiples fuentes
Cámaras (desde SD)
Móviles (vía OneDrive)
Y VIDEOS!
Todo entra en (nuevas) donde esperan que las catalogue
Y luego exporto las 3* a OneDrive

# Etiquetado
- Rating
	- 2 estrellas: día
	- 3 estrellas: mes
	- 4 estrellas: año
	- 5 estrellas: best ever
- Tags
	- Personas. Face recognizition
	- Mascotas. No face recognition
	- `Playa`, `Bicicleta`, `Senderismo`
	- `Baloncesto`, `Fútbol`, `Unicaja`, `MálagaCF`
	- `Amanecer`, `Atardecer`, `Selfie`
	- `Fotografía`: artística (o simplemente no privada, se puede publicar)
	- `Semana Santa`: cofradías + trono + cristo|virgen
- Location
	- GPS no es lo mejor
		- No viene de réflex, 360...
		- Difícil buscar
	- Prefiero jerarquía: País > Provincia > Ciudad > Lugar

# Cuellos de botella
Muchos
- Ingestión (volcado lento)
- Etiquetar, varios pasos
- Revisita de ratings
- Requiere tiempo de foco en el ordenador
- Edición, aunque sea básica: niveles, crop, horizon-level

# Atascado
En 2025 estuve muy bloqueado
Lightroom OFF
	Modelo de licencia repulsivo
	Soy usuario cautivo
Distraido con la Insta360 que no encajaba en mi flujo
Llego a dejar de tirar fotos por no aumentar la bola de nieve

# Entre-veo la luz
Meses dándole vueltas a cómo aprovechar la IA en mi flujo
Carlos es testigo
Sé que tengo que abandonar Lightroom
Llevaba meses usándolo sólo para Reflex
Me da vértigo cambiar y decido trazar un plan
/giphy Formulas flying

# Necesito un Repo para planificar
Usar GitHub como persistencia para interacciones con IA usando MD
Escribo plan para usar Immich, tu propio Google Photos
La idea es servir mis fotos via web de forma privada
Desde un PC siempre encendido (bajo consumo!)
Y ya me caliento para usar un agente IA que me ayude
dhh vendiendo que lo primero que instala en un PC es LLM

![w:400](images/dhh-tweet.png)
https://x.com/dhh/status/2020156016629797193?s=20

# MiniPC Celeron
Decido ponerlo en un Linux ligero
	Recupero MiniPC abandonado
		Mi crío me lo devolvió porque no reproducía Youtube
	Instalo Omarchy (no tan ligero pero wow)
Al poco de empezar, volantazo
/giphy Coche salida autovia
Me paso a digiKam
	Face recognition 👍
	Rating and tagging 👍
	Location 👎 (via GPS)
Probé Darktable y no me convenció (además no soporta vídeos)

# Nace Tenacitas
Instalo OpenClaw y le creo Gmail y GitHub user
- No co-author
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

# Skills de fotos

| Skill                 | Descripción                               |
| --------------------- | ----------------------------------------- |
| fotos-from-onedrive   | Descarga fotos del Camera roll al Inbox   |
| sd-to-hdd             | Copia fotos/videos de la tarjeta al Inbox |
| photos-digikam-backup | Copia el catálogo de Digikam              |
| photos-triage-start   | Genera 1 o más JSON de fotos en el Inbox  |
| photos-triage-commit  | Escribe rating & tags a fotos del Inbox   |
| photos-triage-search  | Busca fotos en Digikam                    |
| fotos-to-onedrive     | Exporta fotos 3* a OneDrive               |
| photos-to-movistar    | Backup videos 360 a Movistar Cloud        |
Se apoyan en algunos MCP

| MCP                | Descripción                                            |
| ------------------ | ------------------------------------------------------ |
| digikam-mcp        | Lee info de fotos, escribe atributos y ejecuta queries |
| movistar-cloud-mcp | Consulta y sube archivos a esa nube                    |

# Test columns

<div class="columns">
<div>

## One

</div>

<div>

## Two

</div>
</div>

# TODO

Nuevas fotos a (inbox)
Empiezo a usar Digikam para etiquetar y rating, pero veo el cuello de botella
Puedo hacer una web? Digikam usa una BD sqlite
Empieza la magia
Creo un PoC puzzle de alguna foto mía, para resolverlo desde el móvil
Primer photo-triage


