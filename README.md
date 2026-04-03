# Crown Caps Soccer — Assets Repository

Repositorio de backup y versionado de todos los assets del juego **Crown Caps Soccer**.

## Estructura

```
assets/
├── models/           # Modelos 3D (.glb, .gltf, .fbx)
│   └── players/      # Modelos de jugadores
├── kits/             # Texturas de equipaciones (PNG/WebP)
├── balls/            # Texturas de balones
├── textures/         # Texturas generales (terreno, HDR, etc.)
│   ├── fields/       # Superficies de campo
│   ├── environment/  # HDRI y entorno
│   └── ui/           # Elementos de interfaz
└── audio/            # Efectos de sonido y música
```

## Cómo sincronizar

Desde el servidor de desarrollo (.110), ejecutar:

```bash
cd /var/www/ccs
bash scripts/sync-assets.sh backup
```

Para restaurar assets al servidor:

```bash
bash scripts/sync-assets.sh restore
```

## Servidor primario

Los assets de trabajo están en `/var/www/ccs/public/` en `192.168.50.110`.
Backup local del servidor: `/home/aaubets/ccs-assets/`

## Nota importante

Los modelos 3D (`public/models/`) están en `.gitignore` del repo principal
para no contaminar el historial de código con archivos binarios grandes.
Este repositorio es la fuente de verdad para esos assets.
