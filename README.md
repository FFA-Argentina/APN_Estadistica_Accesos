# Evolución mensual de accesos

Tablero interactivo de accesos a las áreas protegidas de la **Administración de Parques Nacionales** — Dirección Nacional de Uso Público, Dirección de Concesiones.

Período: **agosto 2023 a julio 2026** · 11 dependencias.

## Qué muestra

- **Tickets** emitidos y **días de visita** habilitados (cada ticket multiplicado por los días que da derecho a ingresar).
- **Ingresos netos de comisiones**: el monto que efectivamente queda para la administración. Es el indicador principal del tablero.
- **Comisiones a Tercerizadoras**: la porción del cobro que retienen los agentes de venta. Netos + comisiones = ingreso percibido.
- **Ingresos teóricos**: los días de visita valuados a la tarifa filtro de residente nacional de un día vigente en cada dependencia y período.

Controles: selector de dependencia; categorías de visitante (residentes, no residentes, vehículos y adicionales) combinables y acumulables; series de ingresos seleccionables; modo *acumuladas* o *superpuestas*; tarjetas por dependencia con la métrica elegida; y descarga del CSV de la vista activa.

Las líneas verticales punteadas marcan los cambios de tarifa filtro (P2 a P6).

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
| `.nojekyll` | Marca para GitHub Pages |
| `README.md` | Este archivo |

No hay dependencias ni proceso de compilación. Los gráficos son SVG generados con JavaScript sin librerías externas; lo único que se descarga de la red es la tipografía Archivo desde Google Fonts, con caída a la tipografía del sistema si no hay conexión.

## Compatibilidad

Probado en Chrome, Safari, Firefox y Edge de escritorio, y en Android e iOS/macOS a partir de 360 px de ancho. En pantallas angostas los gráficos se desplazan horizontalmente para conservar la legibilidad de la serie mensual, las tarjetas pasan a una columna y el detalle mes a mes se consulta tocando el gráfico.

El archivo funciona igual abierto localmente con doble clic, sin servidor.

## Fuente

Elaboración propia con información disponible en ReNaRI.
