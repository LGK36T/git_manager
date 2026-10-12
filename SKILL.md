---
name: git-manager
description: >-
  Directrices, reglas de flujo de trabajo y buenas prácticas para que los agentes de IA interactúen con Git, repositorios, branches, commits y control de versiones.
---

# Skill: Git Manager para Agentes de IA

Este skill define el protocolo estricto que cualquier agente de IA debe seguir al ejecutar operaciones de control de versiones con Git, asegurando un historial limpio, trazable y seguro.

---

## 🎯 Directrices Principales de Comportamiento

### 1. Convención de Commits (Conventional Commits)
- Todo mensaje de commit debe seguir la estructura:
  ```text
  <tipo>(<alcance opcional>): <descripción concisa en imperativo>
  ```
- Tipos estándar permitidos:
  - `feat`: Nueva funcionalidad o capacidad.
  - `fix`: Corrección de un bug.
  - `docs`: Cambios exclusivos en documentación.
  - `refactor`: Refactorización de código sin alterar comportamiento.
  - `test`: Añadir o modificar pruebas.
  - `chore`: Mantenimiento, dependencias o tareas de build.

### 2. Commits Atómicos y Claros
- Cada commit debe representar un cambio lógico y autocontenido.
- Nunca mezclar refactorizaciones cosméticas masivas con cambios de lógica de negocio o solución de bugs en el mismo commit.

### 3. Estrategia de Ramas (Branching)
- `main`: Rama de producción, estable y protegida.
- `dev`: Rama de desarrollo e integración.
- `feature/<nombre>`: Nuevas características.
- `fix/<nombre>` o `hotfix/<nombre>`: Correcciones urgentes.
- Jamás realizar commits directos sobre ramas principales cuando el flujo exija ramas de feature o revisión.

### 4. Verificación Pre-Commit Obligatoria
- Antes de ejecutar `git commit`, el agente debe:
  1. Revisar `git status` para confirmar exactamente qué archivos se están incluyendo.
  2. Ejecutar `git diff` para validar que no se incluyan archivos basura, logs, secretos o cambios no relacionados.
  3. Asegurar que las pruebas y linters pasen exitosamente.

### 5. Versionado Semántico y Changelogs
- Mantener actualizado el archivo `CHANGELOG.md` registrando adiciones, cambios, correcciones y deprecaciones según [Keep a Changelog](https://keepachangelog.com/).
- Seguir las reglas de [SemVer](https://semver.org/): `MAJOR.MINOR.PATCH`.

---

## 🚫 Acciones Prohibidas para el Agente

- ❌ Ejecutar `git push --force` o `git push -f` en ramas protegidas (`main`, `master`, `dev`).
- ❌ Ejecutar `git reset --hard` sin confirmación explícita del usuario o sin respaldo.
- ❌ Incluir secretos, claves privadas, tokens o archivos `.env` en el área de preparación (`git add`).
- ❌ Mensajes de commit vagos como "cambios", "fix", "update files".
