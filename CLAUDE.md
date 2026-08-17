# Claude Legal — reglas del proyecto

Equipo de subagentes y skills para trabajo jurídico. Jurisdicción por defecto: **España y Unión Europea**.

## Reglas innegociables

1. **Cero invención.** Ningún agente cita una norma, sentencia, número de recurso o ECLI que no pueda verificar. Si no lo localiza, escribe `NO LOCALIZADO`. Una cita inventada destruye el asunto y la credibilidad del despacho.
2. **Verificación obligatoria.** Ningún documento sale sin pasar por `verificador-citas`. Tiene poder de veto y su veredicto no se negocia por presión de plazo.
3. **Conflictos primero.** `conflict-check` corre antes que cualquier trabajo sustantivo en un asunto nuevo.
4. **Plazos siempre.** En cuanto aparece una fecha relevante, entra `plazos-procesales`. Un plazo perdido no se recupera.
5. **Datos protegidos.** Nada sale del entorno sin pasar por `anonimizador`. Secreto profesional y RGPD.
6. **Fecha de corte.** Todo entregable indica la fecha hasta la que se ha verificado la normativa.
7. **Revisión humana.** Todo output es trabajo preparatorio. Requiere revisión y asunción por letrado colegiado. No es asesoramiento jurídico.
8. **Hechos no supuestos.** Lo que no te han dicho se marca `[PENDIENTE: ...]`. Nunca se rellena con lo que parece razonable.

## Flujo estándar

```
(caso entrante) triaje-asuntos → conflict-check → legal-orchestrator → [especialistas en paralelo]
                                              → contradictor → verificador-citas → entrega
```

## Estructura

- `agents/` — 45 subagentes. Copiar a `.claude/agents/` (proyecto) o `~/.claude/agents/` (global).
- `skills/` — 10 skills. Copiar a `.claude/skills/`.
- `commands/` — 8 comandos slash con los flujos completos. Copiar a `.claude/commands/`.

## Nota sobre el número de agentes activos

El orquestador decide a quién delegar leyendo el campo `description`. Con 44 candidatos cargados a la vez, el enrutado se degrada. Mantén activo el núcleo y carga los verticales según el asunto.

**Núcleo recomendado (13):** legal-orchestrator, triaje-asuntos, legal-researcher, verificador-citas, conflict-check, contract-drafter, contract-reviewer, redline-negotiator, contradictor, compliance-officer, plazos-procesales, anonimizador, plain-language.
