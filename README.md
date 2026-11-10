# Entendedor · Skill de contexto para Codex y agentes de IA

**Entendedor** ayuda a un agente de IA a retomar tareas, recuperar contexto relevante, conservar tus restricciones y verificar el resultado. Está pensada para peticiones como «sigue con lo anterior», «hazlo como el ejemplo» o «corrige solo esta parte».

La skill guía al agente para identificar qué quieres lograr, buscar el archivo o la conversación pertinente cuando tenga acceso, resolver la tarea con las herramientas disponibles y comprobar el resultado antes de entregarlo.

## Instalar en Codex

Con una versión de GitHub CLI que incluya `gh skill install`, ejecuta:

```sh
gh skill install ma-nucho-pro/entendedor entendedor --agent codex --scope user
```

Para instalarla manualmente, copia la carpeta completa `skills/entendedor` a `~/.agents/skills/entendedor`. Para compartirla en un solo proyecto, usa `.agents/skills/entendedor` dentro del proyecto. Si Codex no la detecta al instante, inicia una sesión nueva. [Documentación de skills de OpenAI](https://developers.openai.com/api/reference/cli)

## Ejemplos de uso

En Codex puedes invocarla con `$entendedor`.

| Si le dices… | La skill orienta al agente a… |
| --- | --- |
| «$entendedor, sigue con el informe anterior y mantén el formato». | Recuperar el informe relevante y conservar el formato acordado. |
| «$entendedor, corrige solo la conclusión». | Identificar la conclusión y aplicar el cambio dentro del alcance indicado. |
| «$entendedor, termina la tarea y revisa que funcione». | Retomar el estado disponible y validar el resultado con una comprobación adecuada. |

## Archivos y alcance

- [Instrucciones de la skill](skills/entendedor/SKILL.md) para recuperar contexto, mantener restricciones y verificar entregas.
- [Guía de referencia](skills/entendedor/references/universal-context-intelligence-playbook.md) con ejemplos y criterios de verificación para tareas complejas.

La recuperación de archivos, conversaciones y otros datos depende del acceso del agente y de las herramientas disponibles en su entorno. El repositorio contiene instrucciones en Markdown y metadatos de interfaz en YAML.

## English summary

Entendedor is a context-recovery and task-continuity agent skill for Codex. It helps agents resume multi-step tasks, interpret references to earlier work, preserve user constraints, and verify results using the tools and permissions available in their environment. The core skill is in Spanish and its extended playbook is in English.
