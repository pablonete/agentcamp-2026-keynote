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

Member of 
- ~~MalagaDnug~~ DotNetMalaga 
- OpenSouthCode
- AzureMalaga 
- MalagaAI 
## @pablonete

<!-- footer: Agentcamp 2026 -->
<!-- paginate: true -->
# <!--fit--> And those videos, where will they go?

![w:700](images/saeteros.png)

Bizcocho - [Saetero](https://youtube.com/clip/Ugkx5vroDIDXbeAZQISZT3JM7ktYtkY8ZMBF)

# Amateur Photographer
DSLR, mobile, 360... and videos

Adobe Lightroom catalogs
Thousands of photos on HDDs since 2007

Google Photos 👎

<!-- 
I enjoy shooting more than editing
Frustrated librarian, I love archiving

I used Google Photos while it was free
but never saw it as a replacement, not mine
Dynamic collections FTW
-->

# Previous Workflow
Photos from multiple sources
Cameras (from SD cards)
Mobile phones (via OneDrive)
I use an inbox and then export the 3* ones to OneDrive

![w:800](mermaid/lightroom.workflow.jpg)

# Tagging
<!--
- Rating:
	- 2 stars: day
	- 3 stars: month
	- 4 stars: year
	- 5 stars: best ever
- GPS is not ideal
	- Doesn't come from DSLR, 360...
	- Hard to search
-->
- Rating: 2*, 3*, 4*, 5*
- Tags
	- People, pets
	- `Beach`, `Cycling`, `Basketball`, `Football`, `Sunrise`, `Selfie`
- Location by hierarchy:
	- Country > Province > City > Place

# Bottlenecks
- Ingestion (slow import)
- Tagging, multiple steps
- Rating review 🌟
- Requires time at the computer
- Editing, even basic: levels, crop, horizon-level
## Me

# Stuck
<!-- 
	Repulsive licensing model
	I'm a captive user
	More and more blocked in 2025, going backwards
	I even stopped taking photos to avoid growing the snowball
	Months going back and forth on how to leverage AI in my workflow
-->
- Adobe is killing Lightroom $ $ $
- New Insta360 that didn't fit in

- I need to leverage AI
- The idea of changing scares me, so I decide to draw up a plan

# Everything starts with a Repo
<!--
serve my photos via web and catalog and edit
From an always-on PC (low power!)
-->
I draw up a plan with Copilot
- PLAN.md
- Issues
- Project board
# MiniPC
<!--
N5095A
My kid returned it to me because it couldn't play Youtube
Shortly after starting, a U-turn
/giphy Car leaving highway
I tried Darktable and wasn't convinced (plus it doesn't support videos)
-->
I reclaim a written-off MiniPC
Celeron N5095A
Does more than I expected

![bg right](images/openclaw-telegram-desktop-btop-fullscreen.jpg)

# Omarchy
Modern & Opinionated Linux

![w:600](images/dhh-tweet.png)
<sub>https://x.com/dhh/status/2020156016629797193?s=20</sub>


![bg right](images/omarchy-screenshot.jpg)

# OpenClaw
It had to be open-source
The OS of agentics?
Complex security model
But it still has risks
![bg right](images/openclaw-screenshot.jpg)

<!-- 
Things change very fast, OpenClaw is a jolt. Anthropic turned off the tap this week and it disrupts what a lot of people are doing. Pros and cons of being OpenSource. Long live OpenSource, it's the only way to do this — a company couldn't launch a product like OpenClaw

I've had this for a month and when I think about giving the keynote I say "how am I going to teach anyone anything". I don't claim this will be an in-depth talk. I don't even have answers to questions — I can only answer about what I've done, not about how OpenClaw works, its model is not simple (security model, Chrome model, agent model). It's not trivial. I've learned the minimum I needed to make progress.
-->

# Tenacitas is born
Her Gmail (no access to my email)
And her GitHub user
- Not a co-author, [her commits](https://github.com/pablonete/agentcamp-2026-keynote/commits/main/slides)
- No PAT to use my repos on my behalf

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

# Banned
Google deactivated her
Skill `gog` *looked like* a bot
But we appealed and 🥳
![bg right](images/openclaw-telegram-google-account-recovery.jpg)

# The agent and the model

![bg right](images/el-agente-y-el-modelo.jpg)

OpenClaw  agent
orchestrates subagents

I use **Claude Sonnet 4.6** 
via GitHub Copilot

<!-- 
OpenClaw is the runtime: it manages sessions, skills, channels (Telegram, Discord...).
The "brain" is the language model — in my case Claude Sonnet 4.6, accessed for free through GitHub Copilot.
Like swapping the engine of a car: the chassis (OpenClaw) is the same, the engine (model) can be different.
-->
# Model in the cloud
Under maintenance
In 1 month this has happened to me twice
![bg right:30%](images/openclaw-telegram-model-error-explanation.jpg)

# Immich 🛑
Your own Google Photos
self-hosted

Not what I need right now

![bg right](images/immich-screenshot.png)

# digiKam
- Open source 👍
- Face recognition 👍
- Rating and tagging 👍
- Location 👎 (via GPS)

![bg right](images/digikam-screenshot.webp)

# New Workflow

![w:1200](mermaid/openclaw.workflow.png)

# New Workflow Skills

![w:1200](mermaid/openclaw.workflow.skills.png)
# Photo Skills
<style scoped>section { font-size: 32px; }</style>

| Skill                  | Description               |
| ---------------------- | ------------------------- |
| /fotos-from-onedrive   | From Camera roll to Inbox |
| /sd-to-hdd             | From SD card to Inbox     |
| /photos-digikam-backup | Catalog only              |
| /photos-triage-start   | Photos JSON for review    |
| /photos-triage-commit  | Saves review              |
| /photos-triage-search  | Search in DigiKam         |
| /fotos-to-onedrive     | 3* to OneDrive            |
| /photos-to-movistar    | Raw 360 videos            |

# MCPs

| MCP                | Description                                                                                 |
| ------------------ | ------------------------------------------------------------------------------------------- |
| digikam-mcp        | Reads info from sqlite<br>Writes tags, ratings...<br>Search: runs queries<br>Moves folders |
| movistar-cloud-mcp | Uploads files to that cloud                                                                 |

# Scale
1. Chat - improvise
2. Skill - flexible
3. Code - stable

![w:600](images/tweet-matias-3.jpg)
https://x.com/woloski/status/2036251852312903943

<!--
The great thing about skills: they're flexible. While they're running you can be chiming in and changing their behavior on the fly.
-->

# <!--fit--> Walking Tenacitas
Some of my conversations
with OpenClaw on Telegram
# Skills
I can never get them all to show up
![bg right](images/openclaw-telegram-skills-list-commands.jpg)
# /stop
Sometimes it misses easy things
and gets confused
![bg right:30%](images/openclaw-telegram-osp-children-start-bug.jpg)

# /fotos-from-onedrive
Fixes a crashed lockscreen
![bg right:30%](images/openclaw-telegram-hyprlock-crash-fix.jpg)
# /sd-to-hdd
Copying from SD to HDD
![bg right:30%](images/openclaw-telegram-sd-to-hdd-jueves-santo.jpg)
# /sd-to-hdd
Now with event name
![bg right](images/openclaw-telegram-sd-copy-insta360-telegram.jpg)

# Photos Triage
Custom webapp 
For mobile
![bg right:30%](images/photos-triage-seleccion.jpg)
# Photos Triage
Select, rate and tag
each photo
![bg right:30%](images/photos-triage-grid.jpg)
# Photos Triage
Saved as JSON on GitHub
and committed to DigiKam
![bg right:30%](images/photos-triage-detail.jpg)
# Tailscale
Secure tunnel between devices
and publish with HTTPS
![bg right](images/tailscale-screenshot.jpg)

# /photos-triage-search
Skill to search photos
Generates JSON
![bg right:30%](images/openclaw-telegram-photos-search-skill-plan.jpg)
# /fotos-to-onedrive
Including months
Asks for dry-run to validate
![bg right:30%](images/openclaw-telegram-photo-export-digikam-debug.jpg)
# Photo Open
Another custom webapp
For sharing photos
- Public
- Unlisted
![bg right:30%](images/openclaw-telegram-photo-open-share-plan.jpg)
# Movistar Cloud
Discovering the internal API
![bg right:30%](images/openclaw-telegram-movistar-sapi-api-discovery.jpg)
# Movistar Cloud
Solving authentication
![bg right:30%](images/openclaw-telegram-movistar-sapi-jsessionid.jpg)
# Movistar Cloud
Errors with large files
It figured it out: use streaming
![bg right:30%](images/openclaw-telegram-movistar-upload-oom-fix.jpg)
# Movistar Cloud
Don't remember my phone number
I said don't remember it!
![bg right:30%](images/openclaw-telegram-movistar-phone-privacy-fix.jpg)
# Vibe coding
Debugging drag & drop via Telegram

> Vibe-coding is working as a QA fulltime.

<sub>https://x.com/pablonete/status/2036878616961638507</sub>

![bg right:30%](images/openclaw-telegram-drag-drop-clip-debug.jpg)

# Vibe coding
<!-- Low power, enough for low-res, VA-API flipping -->
Leveraging the mini-GPU
for 1080p video encoding

Hulio, what exactly is VA-API?
![bg right:30%](images/openclaw-telegram-video-render-upside-down-fix.jpg)

# Future improvements
- Location from GPS
- Basic editing, automated
- Memory videos
- Auto tagging
- Adding past years
- Publish open-source MCPs and more

# First month retro
- Kid with a new toy
- A thousand ideas
- Very high speed: I forget things
- I'm using 5-10% of OpenClaw and it's wow
- I built all this while reviewing +5500 photos

# Takeaways
- 🦞 OpenClaw: more possibilities the more you use it

- 📷 Photos: plan, execute, iterate, custom

- 📁 Repos: persistence, visibility, coordination

- 🧠 AGENTS.md vs Skill vs Memory

- ⚡ Matias: Chat → Skill → Software

- 👺 Vibe-coding, when do I review the code?

# <!--fit-->Thanks 🦞
<!-- color: red -->

@pablonete

