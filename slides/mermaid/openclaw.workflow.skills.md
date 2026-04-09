```mermaid
flowchart LR
	A[📱 Móvil] -->|fotos-from-onedrive| C[💾 Disco duro]
	B[📷 Cámara] -->|sd-to-hdd| C
	C --> D[🗂️ DigiKam]
	D -->|photos-triage-start| F[⭐ photos-triage]
	F -->|photos-triage-commit| D
	D -->|photo-open| G[🌐 Publicar]
	D -->|fotos-to-onedrive 3★| E[☁️ OneDrive]
	C -->|photos-to-movistar| H[🎬 Movistar Cloud]
```
