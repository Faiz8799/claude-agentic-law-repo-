---
description: Filtrar casos entrantes — dictamen aceptar/derivar/rechazar con plazos y scoring
argument-hint: [descripción del caso, ruta a carpeta de consultas, o pega los emails]
---

Actúa el flujo de triaje de casos entrantes sobre: $ARGUMENTS

1. Si es una ruta o carpeta, lee todos los documentos que contenga; cada documento o email es un caso candidato.
2. Delega el análisis en el agente `triaje-asuntos` (que a su vez lanza `conflict-check`).
3. Devuelve la tabla-resumen ordenada por urgencia de plazos y scoring, con las fichas individuales debajo.
4. Para cada caso RECHAZADO o DERIVADO, ofrece redactar la carta de no aceptación con advertencia de plazos.
