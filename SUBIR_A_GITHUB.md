# Subir el reporte Retiros y Rezagos a GitHub (link público)

Esta carpeta contiene **reporte_retiros_rezagos.html** listo para subir. Es una copia autocontenida del Daily Report Scorecard Retiros y Rezagos.

---

## Opción A: Usar el repo AI-Reverse-Logistics (recomendado si ya lo tenés)

1. **Abrí una terminal donde tengas Git** (Git Bash, PowerShell con Git en PATH, o CMD con Git).

2. **Cloná el repo** (si aún no lo tenés):
   ```bash
   cd C:\Users\estnari\.cursor\projects\project.cursor\mcp.bigquery
   git clone https://github.com/estefanianari-hue/AI-Reverse-Logistics.git
   ```

3. **Copiá el HTML al repo**:
   ```powershell
   Copy-Item "daily_report_r&r\para_github\reporte_retiros_rezagos.html" -Destination "AI-Reverse-Logistics\reporte_retiros_rezagos.html"
   ```

4. **Entrá al repo, agregá, cometé y subí**:
   ```bash
   cd AI-Reverse-Logistics
   git add reporte_retiros_rezagos.html
   git commit -m "Daily Report Scorecard Retiros y Rezagos - versión para validar formato"
   git push origin main
   ```
   (Si tu rama por defecto es `master`, usá `git push origin master`.)

5. **Link público para compartir** (cargar el HTML en el navegador):
   ```
   https://htmlpreview.github.io/?https://raw.githubusercontent.com/estefanianari-hue/AI-Reverse-Logistics/main/reporte_retiros_rezagos.html
   ```
   Si la rama es `master`, cambiá `main` por `master` en la URL.

---

## Opción B: Repo nuevo solo para este reporte

1. En GitHub: **New repository** (ej. `daily-report-retiros-rezagos`), público, sin README.

2. En tu PC:
   ```bash
   cd C:\Users\estnari\.cursor\projects\project.cursor\mcp.bigquery
   mkdir daily-report-repo
   cd daily-report-repo
   git init
   Copy-Item "..\daily_report_r&r\para_github\reporte_retiros_rezagos.html" .
   git add reporte_retiros_rezagos.html
   git commit -m "Daily Report Scorecard Retiros y Rezagos"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/daily-report-retiros-rezagos.git
   git push -u origin main
   ```

3. Link público:
   ```
   https://htmlpreview.github.io/?https://raw.githubusercontent.com/TU_USUARIO/daily-report-retiros-rezagos/main/reporte_retiros_rezagos.html
   ```

---

## Actualizar el reporte más adelante

Cada vez que quieras refrescar el link con la última versión:

1. Copiá de nuevo el HTML desde `daily_report_r&r\reporte_kpis_pre_post_boceto.html` a `para_github\reporte_retiros_rezagos.html` (o copiá directo al repo).
2. En la carpeta del repo: `git add reporte_retiros_rezagos.html`, `git commit -m "Actualizar reporte"`, `git push`.

Cuando configures la **automatización diaria**, el mismo flujo puede copiar el HTML generado al repo y hacer commit + push para que el link siempre muestre la versión del día.

---

**Nota:** En Cursor no pude ejecutar `git` (no está en el PATH de la terminal). Por eso tenés que correr estos comandos vos en una terminal donde Git funcione.
