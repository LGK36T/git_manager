# Git Manager

Módulo encargado de la gestión, automatización, estandarización y control de flujos de trabajo de Git, repositorios, versionado y políticas de integración continua dentro del ecosistema.

---

## 📌 Descripción General

**Git Manager** centraliza las herramientas, directrices y scripts para administrar repositorios, ramas, políticas de commit, versionado semántico y flujos de colaboración en Git (como GitFlow, GitHub Flow o Trunk-Based Development). Su propósito es asegurar consistencia, trazabilidad e integridad en el control de versiones a lo largo de todos los proyectos.

---

## 🎯 Objetivos y Responsabilidades

- **Estandarización de Flujos de Trabajo:** Definición y aplicación de estrategias de branching, conventions de commits (Conventional Commits) y políticas de merge.
- **Automatización de Hooks y Calidad:** Configuración de hooks de Git (pre-commit, commit-msg, pre-push) para linting, pruebas automáticas y validación de mensajes.
- **Gestión de Releases y Versionado:** Automatización de generación de tags, changelogs y versionado semántico (SemVer).
- **Sincronización Multi-Repositorio:** Herramientas y scripts para la orquestación, actualización y auditoría de múltiples repositorios y submódulos.
- **Integración con CI/CD:** Sincronización transparente con pipelines de integración y entrega continua (GitHub Actions, GitLab CI, etc.).

---

## 📂 Estructura del Proyecto

```text
git_manager/
├── hooks/               # Scripts y configuraciones de Git hooks
├── templates/           # Plantillas de issues, PRs y mensajes de commit
├── scripts/             # Scripts de automatización, sincronización y releases
├── config/              # Configuraciones de linters, commitlint y reglas
├── tests/               # Pruebas de scripts y validadores
├── .gitignore           # Exclusiones de control de versiones
├── CHANGELOG.md         # Historial de versiones y cambios
└── README.md            # Documentación general del módulo
```

---

## 🚀 Inicio Rápido

### Requisitos Previos

- Git (versión 2.30+ recomendada).
- CLI de GitHub (`gh`) o credenciales SSH/HTTPS configuradas.
- Entorno de ejecución para scripts (Bash, Python o Node.js según aplique).

### Configuración

1. Clonar el repositorio:
   ```bash
   git clone <URL_DEL_REPOSITORIO>/git_manager.git
   cd git_manager
   ```

2. Configurar permisos en scripts:
   ```bash
   chmod +x scripts/*.sh hooks/* 2>/dev/null || true
   ```

3. Aplicar hooks locales o utilidades según la guía de desarrollo.

---

## 🔄 Flujo de Trabajo con Git

1. Crear una rama descriptiva para cada funcionalidad o regla nueva:
   ```bash
   git checkout -b feature/nueva-automatizacion
   ```
2. Realizar commits siguiendo la convención de [Conventional Commits](https://www.conventionalcommits.org/).
3. Mantener actualizado el archivo [CHANGELOG.md](file:///home/LGK36T/workspace/skills/git_manager/CHANGELOG.md).
4. Abrir un Pull Request / Merge Request para revisión del equipo.

---

## 📄 Licencia

Este proyecto está bajo los términos y directrices definidos por el equipo de desarrollo.
