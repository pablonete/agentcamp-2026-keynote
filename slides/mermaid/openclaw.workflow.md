```mermaid
flowchart LR
	A[fotos-from-onedrive] --> C[HDDs]
	B[sd-to-hdd] --> C
	C --> D[Digikam]
	D --> F[photos-triage]
	F -->|commit| D
	D -->|publish| G[photo-open]
	D -->|3*| E[OneDrive]
	C --> H[Movistar Cloud]
```