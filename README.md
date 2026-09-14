# Banana Claude

Skill de Claude Code para generación, edición y revisión de imágenes con los
modelos Gemini de Google. Instalado como skill de proyecto desde
[AgriciDaniel/banana-claude](https://github.com/AgriciDaniel/banana-claude).

## Uso

Con Claude Code, invoca `/banana` (o el nombre de skill `banana`) para
generar, editar, comparar y revisar assets visuales. Ver
`.claude/skills/banana/SKILL.md` para el flujo completo (brief → prompt →
plan → aprobación → ejecución → revisión de píxeles).

## Requisitos

- Python 3.11+
- Variable de entorno `GEMINI_API_KEY` configurada antes de ejecutar
  generaciones pagadas (nunca se solicita, imprime ni almacena la clave).

## Configuración de la API key

1. Copia `.env.example` a `.env` y completa `GEMINI_API_KEY` con tu clave.
2. Carga la variable en tu shell antes de usar la skill, por ejemplo:
   `export $(grep -v '^#' .env | xargs)` o `export GEMINI_API_KEY=tu_clave`.
3. `.env` está en `.gitignore`: nunca se sube al repositorio.

Si una clave llegó a compartirse por chat, ticket o commit, considérala
comprometida y regenérala en Google AI Studio antes de usarla.

No requiere dependencias de terceros: los scripts usan únicamente la
librería estándar de Python.
