# Evolución mensual de accesos

Tablero interactivo de accesos a las áreas protegidas de la **Administración de Parques Nacionales** — Dirección Nacional de Uso Público, Dirección de Concesiones.

Período: **octubre 2023 a septiembre 2026** · 11 dependencias. La comparación interanual usa ciclos completos de doce meses, de octubre a septiembre, contados hacia atrás desde el 30 de septiembre de 2026 (oct 23–sep 24, oct 24–sep 25 y oct 25–sep 26).

## Qué muestra

- **Tickets** emitidos y **días de visita** habilitados (cada ticket multiplicado por los días que da derecho a ingresar).
- **Ingresos netos de comisiones**: el monto que efectivamente queda para la administración. Es el indicador principal del tablero.
- **Comisiones a Tercerizadoras**: la porción del cobro que retienen los agentes de venta. Netos + comisiones = ingreso percibido.
- **Ingresos teóricos**: los días de visita valuados a la tarifa filtro de residente nacional de un día vigente en cada dependencia y período.
- **Valores en dólares**: todos los importes pueden leerse en pesos corrientes o en dólares. Cada importe diario se divide por la cotización del dólar de ese día (blue hasta el 12/12/23 y oficial desde el 13/12/23; fines de semana y feriados toman la última cotización hábil).

Controles: selector de dependencia; filtro de período anual (oct 23–sep 24, oct 24–sep 25, oct 25–sep 26 o el trienio completo; al abrir muestra el último ciclo, y cada indicador y tarjeta agrega en una línea inferior el total del trienio); categorías de visitante (residentes, no residentes, vehículos y adicionales) combinables y acumulables; selector de moneda (pesos o dólares), que se aplica a indicadores, tablas, gráficos, tarjetas y CSV; series de ingresos seleccionables; modo *acumuladas* o *superpuestas*; tarjetas por dependencia con la métrica elegida; y descarga del CSV de la vista activa.

Las líneas verticales punteadas marcan los cambios de tarifa filtro (P2 a P6).

El informe completo en PDF (`Informe_Accesos_trienal_sep26.pdf`) se abre desde el enlace del encabezado y desde «Descargar el informe completo», al pie del tablero.

## Publicar en GitHub Pages

1. Crear un repositorio y subir el contenido de esta carpeta a la rama `main`:

   ```bash
   git init
   git add .
   git commit -m "Tablero de accesos"
   git branch -M main
   git remote add origin https://github.com/USUARIO/REPOSITORIO.git
   git push -u origin main
   ```

2. En el repositorio: **Settings → Pages → Build and deployment**, elegir *Deploy from a branch*, rama `main` y carpeta `/ (root)`. Guardar.

3. En un minuto queda publicado en `https://USUARIO.github.io/REPOSITORIO/`.

El archivo `.nojekyll` evita que GitHub Pages procese el sitio con Jekyll.

## Estructura

| Archivo | Contenido |
| --- | --- |
| `index.html` | Tablero completo: datos, estilos, gráficos y logo institucional embebidos en un único archivo |
| `Informe_Accesos_trienal_sep26.pdf` | Informe de accesos, octubre 2023 – septiembre 2026, enlazado desde el tablero |
| `.nojekyll` | Marca para GitHub Pages |
| `README.md` | Este archivo |

No hay dependencias ni proceso de compilación. Los gráficos son SVG generados con JavaScript sin librerías externas; lo único que se descarga de la red es la tipografía Archivo desde Google Fonts, con caída a la tipografía del sistema si no hay conexión.

## Compatibilidad

Probado en Chrome, Safari, Firefox y Edge de escritorio, y en Android e iOS/macOS a partir de 360 px de ancho. En pantallas angostas los gráficos se desplazan horizontalmente para conservar la legibilidad de la serie mensual, las tarjetas pasan a una columna y el detalle mes a mes se consulta tocando el gráfico.

El archivo funciona igual abierto localmente con doble clic, sin servidor.

## Fuente

Elaboración propia con información disponible en ReNaRI.
