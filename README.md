# Aptus · versiones publicadas

Versiones listas para usar de **Gestión de Mantenimiento Planta**. El código fuente es privado; aquí solo llega la app compilada.

| Archivo | Qué es |
|---|---|
| `index.html` | La última versión. Se abre con doble clic en Edge o Chrome, sin instalar nada. |
| `version.json` | Versión, fecha, novedades, huella SHA-256 y firma. La app lo consulta para avisar que hay versión nueva. |
| `versiones/<versión>/index.html` | Cada versión publicada, por si hay que volver a una anterior. |

## Cómo se actualiza la app

1. Al abrir, la app consulta `version.json` (como máximo cada 6 horas; también con **Buscar actualizaciones** en la pantalla de inicio).
2. Si hay una versión nueva, muestra un aviso con sus novedades y el botón **Actualizar**.
3. Descarga `index.html`, verifica la huella y la **firma** con la clave pública que trae la app, guarda la versión anterior en `respaldo-app/` y reemplaza el archivo. Un archivo sin firma válida no se instala.

Este repositorio lo escribe solo la Action **Publicar versión** de `marioser/aptus`, al unir a `main` un cambio con versión nueva. No suba archivos a mano: no tendrían firma válida.

No contiene datos de la empresa.
