# Resultados de MonitorEO-OBSNEV

**<https://monitoreo-obsnev.github.io/resultados/>**

Los análisis de seguimiento que publica el Observatorio de Cambio Global de Sierra Nevada (OBSNEV, Universidad de
Granada) con [MonitorEO](https://github.com/monitoreo-obsnev/monitoreo): un catálogo de informes, cada uno con sus
mapas y gráficos interactivos, sus textos, sus datos y la llamada que produjo cada resultado. Se consulta en el
navegador, sin cuenta de Earth Engine.

Es una web estática servida por GitHub Pages desde la rama `main`. La escribe `monitoreo publish`: no se edita a mano
(ver [Visor de resultados](https://github.com/monitoreo-obsnev/monitoreo/wiki/Visor-de-resultados) en el manual).

## Publicar

Solo publican quienes tienen permiso de escritura en este repositorio; el historial guarda quién publicó qué.

```bash
git clone git@github.com:monitoreo-obsnev/resultados.git ~/resultados    # una vez
monitoreo publish informe.yaml --site ~/resultados                      # o --remove ID para retirar un informe
monitoreo publish --check --site ~/resultados
cd ~/resultados && git add -A && git commit -m "Informe ..." && git push   # en línea en un minuto
```

## Licencias

- **Datos y mapas** (`reports/`, `catalog.json`): [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.es),
  salvo que el `report.json` de un informe diga otra. Se pueden copiar, redistribuir y adaptar para cualquier fin,
  también comercial, citando la fuente como indica cada informe.
- **Código del visor** (`index.html`, `report.html` y `assets/`, salvo `assets/logos/`): parte de MonitorEO, con
  licencia [GPL-3.0-or-later](https://www.gnu.org/licenses/gpl-3.0.html).
- **Logotipos** (`assets/logos/`): de sus instituciones; no se incluyen en esas licencias.
