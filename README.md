# Git Manager (AI Agent Skill)

Skill especializada para guiar a los agentes de Inteligencia Artificial al interactuar con Git, gestionar repositorios, aplicar Conventional Commits, estructurar ramas y preservar la integridad del historial.

---

## 📌 ¿Qué es este Skill?

**Git Manager** define el conjunto de reglas, validaciones previas y convenciones que los agentes de IA (como Antigravity, Claude Code, Cursor, Copilot, etc.) deben respetar al manipular repositorios Git. Su objetivo es evitar comandos destructivos no deseados, commits desordenados o fugas de archivos sensibles.

La especificación completa del comportamiento del agente se encuentra en [SKILL.md](file:///home/LGK36T/workspace/skills/git_manager/SKILL.md).

---

## 🎯 Directrices que impone a la IA

- **Conventional Commits:** Mensajes estructurados (`feat:`, `fix:`, `refactor:`, `test:`, `chore:`, `docs:`).
- **Commits Atómicos:** Un cambio lógico autocontenido por commit sin mezclar refactorizaciones accidentales.
- **Protección de Ramas:** Flujo claro de ramas (`main`, `dev`, `feature/*`, `fix/*`) sin commits directos a ramas protegidas.
- **Validación Pre-Commit:** Inspección obligatoria de `git status` y `git diff` antes de confirmar cambios.
- **Seguridad y Prohibición de Force Push:** Bloqueo terminante de `push --force` en ramas principales y exclusión de secretos.

---

## 📂 Contenido del Repositorio

```text
git_manager/
├── SKILL.md             # Instrucciones principales para el agente de IA
├── CHANGELOG.md         # Historial de cambios del skill
├── LICENSE              # Licencia de código abierto (MIT)
├── README.md            # Documentación y descripción del skill
└── .gitignore           # Exclusiones de control de versiones
```

---

## 🚀 Uso e Integración

### En Google Antigravity / Asistentes IA
Coloca este repositorio dentro del directorio de skills de tu espacio de trabajo:
```bash
.agents/skills/git_manager/
# o ~/.gemini/antigravity-cli/skills/git_manager/
```
El agente descubrirá automáticamente el archivo `SKILL.md` y aplicará estas pautas de control de versiones en cada comando Git que proponga o ejecute.

---

## 📄 Licencia

Este proyecto está bajo la licencia [MIT](file:///home/LGK36T/workspace/skills/git_manager/LICENSE).
