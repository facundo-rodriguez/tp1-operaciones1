# TP01 - Operaciones1 — Automatización con Bash
Script que automatiza 3 tareas de administración de sistemas Linux.

## Tareas automatizadas
1. **Backup con timestamp** — copia archivos del directorio actual
2. **Limpieza de archivos viejos** — elimina backups con más de N días
3. **Reporte de salud** — genera informe de CPU, memoria y disco
## Uso
Ejecutar en bash
bash scripts/sistema.sh [directorio_origen] [dias_retencion]
Ejemplos
bash scripts/sistema.sh # usa defaults
bash scripts/sistema.sh /var/log 3 # limpia archivos de más de 3 días
Estructura
devops-TP01/
├── scripts/
│ └── sistema.sh
├── logs/
│ ├── sistema.log
│ └── reporte_FECHA.txt
├── backups/
└── README.md
---
## Paso 5 — Subir a GitHub
Ir a la pagina de github y entrar con la misma cuenta de google con que
verificamos killercoda o tu VM Linux
Ejecutar en bash
cd ~/operaciones1/devops-TP01
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
git init
git add .
git commit -m "TP01: script de automatización bash con backup, limpieza y
reporte"
git branch -M main
apt install gh
gh auth login

? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations on this host? HTTPS
? How would you like to authenticate GitHub CLI? Paste an authentication
token

Tip: you can generate a Personal Access Token here
https://github.com/settings/tokens
The minimum required scopes are 'repo', 'read:org', 'workflow'.
gh repo create devops-TP01 --public
git remote add origin https://github.com/TU_USUARIO/devops-TP01.git
git push -u origin main
----*----*----
