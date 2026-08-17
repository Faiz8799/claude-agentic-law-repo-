---
description: Revisión de contrato con matriz de riesgos y propuesta de redlines
argument-hint: [ruta al contrato] [de qué lado estamos: cliente/proveedor/comprador...]
---

Revisa el contrato: $ARGUMENTS

1. Delega en `contract-reviewer` indicando de qué lado estamos.
2. Aplica la skill `matriz-riesgos`: tabla ordenada por nivel, con impacto económico cuantificado.
3. Para cada riesgo 🔴 y 🟠, pide a `redline-negotiator` la redacción alternativa y la posición de repliegue.
4. Pasa el resultado por `verificador-citas` si se citó normativa.
5. Entrega: resumen ejecutivo (riesgos bloqueantes primero) + matriz + redlines listos para insertar.
