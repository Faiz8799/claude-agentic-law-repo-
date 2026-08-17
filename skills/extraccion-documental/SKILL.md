---
name: extraccion-documental
description: Conversión de documentación jurídica en PDF o escaneada a datos estructurados para due diligence y revisión masiva. Úsala cuando haya que analizar volumen documental y extraer hallazgos de forma sistemática.
---

# Extracción documental

## Proceso
1. **Inventario**: lista todos los archivos con tipo, fecha, partes y estado (firmado / borrador / ilegible).
2. **Clasificación** por área: societario · contratos · laboral · inmobiliario · financiación · IP · litigios · licencias · datos · fiscal.
3. **Extracción** por documento:
   - Partes y firmantes
   - Fecha de firma y de entrada en vigor
   - Objeto
   - Duración, prórroga y preaviso
   - Importes y forma de pago
   - Garantías y avales
   - Cambio de control
   - Exclusividad y no competencia
   - Limitación de responsabilidad
   - Ley aplicable y fuero
   - Anexos referenciados y si están presentes
4. **Cruce**: contrasta lo extraído con el inventario para detectar lo que falta.

## Salida
Tabla estructurada, un documento por fila, con enlace a la ubicación exacta (archivo y página).

## Reglas
- Cita siempre archivo y página. Un hallazgo sin ubicación es inútil.
- Marca **[ILEGIBLE]** y **[NO ENCONTRADO]** de forma explícita. Nunca rellenes huecos con lo que parece razonable.
- Señala los anexos referenciados que no están en el data room: son la laguna más frecuente.
