# Índice de Memoria del Sistema Clawbot

> **Estructura optimizada para recuperación rápida y consistencia**  
> **Última actualización:** 2026-02-18

---

## Estructura Jerárquica

```
memory/
├── INDEX.md ← Este archivo - mapa de navegación
├── README.md ← Guía de uso del sistema de memoria
├── YYYY-MM-DD.md ← 📅 Daily logs (raíz, para compatibilidad con agent-daily-planner)
├── projects.json ← 📋 Índice de proyectos activos (agent-daily-planner)
│
├── strategic/ 🎯 Objetivos de largo plazo
│   ├── objectives.md
│   ├── principles.md
│   └── vision.md
│
├── projects/ 📁 Proyectos activos (carpetas ricas por proyecto)
│   └── _template/ ← Plantilla para nuevos proyectos
│       ├── context.md
│       ├── decisions.md
│       └── status.md
│
├── technical/ ⚙️ Stack y decisiones técnicas
│   ├── stack.md
│   ├── apis.md
│   ├── patterns.md
│   └── decisions/
│
├── behavioral/ 👤 Preferencias de Radulenko
│   ├── preferences.md
│   ├── patterns.md
│   └── context.md
│
├── decisions/ 🔀 Decisiones críticas documentadas
│   └── YYYY-MM-DD-{slug}.md
│
├── meta/ 🧠 Evolución del sistema
│   ├── soul-versions/ ← Versiones de SOUL.md
│   │   ├── v1.0-20260217.md
│   │   └── CURRENT -> v1.0
│   ├── evolution.md
│   └── audit.md ← Log de cambios estructurales
│
├── weekly/ 📊 Resúmenes semanales (agent-daily-planner)
│   └── YYYY-Wxx.md
│
├── synthesis/ 🔗 Conocimiento cruzado y refinado
│   ├── learnings.md
│   ├── patterns-systemic.md
│   └── insights.md
│
├── templates/ 📋 Plantillas reutilizables
│   ├── decision.md
│   ├── project-init.md
│   └── session-log.md
│
└── indices/ 🔍 Índices para búsqueda rápida
    ├── topics.json
    ├── people.json
    └── tags.md
```

---

## Cambio Estructural 2026-02-18

**Motivación:** Integración con skill `agent-daily-planner` de ClawHub.

**Antes:** `daily/YYYY-MM-DD.md`  
**Después:** `YYYY-MM-DD.md` (raíz de memory/)

**Impacto:** La skill ahora opera con rutas nativas sin conflicto. Los weekly summaries se almacenan en `weekly/`.

---

## Protocolos de Acceso

### Escritura

| Tipo | Trigger | Destino |
|------|---------|---------|
| Decisión crítica | Post-decisión validada | `decisions/` |
| Preferencia detectada | Confirmación implícita | `behavioral/` |
| Aprendizaje sintetizado | Heartbeat/Reflexión | `synthesis/` |
| Estado de proyecto | Actualización periódica | `projects/{name}/` |
| Plan diario | Inicio de sesión | `YYYY-MM-DD.md` (via agent-daily-planner) |
| Resumen semanal | Domingo/Lunes | `weekly/YYYY-Wxx.md` |

### Lectura

1. **Pre-respuesta:** `strategic/` + `behavioral/` + contexto de proyecto
2. **Post-tarea:** Síntesis → `synthesis/`
3. **Audit:** `meta/audit.md` + `decisions/`
4. **Planificación:** `/plan today` → lee `YYYY-MM-DD.md` anterior

---

## Integración agent-daily-planner

| Comando | Archivo afectado |
|---------|------------------|
| `/plan today` | `2026-02-18.md` |
| `/plan week` | `weekly/2026-W08.md` |
| `/plan ship` | `2026-02-18.md` |
| `/plan block` | `2026-02-18.md` |

**Nota:** Los proyectos ricos siguen en `projects/{nombre}/`. La skill usa `projects.json` como índice ligero.

---

## Rendimiento

- Búsqueda O(1): Índices en `indices/`
- Recuperación contextual: Jerarquía explícita
- Sin duplicación: Links en lugar de copias
- Compresión semántica: Solo conocimiento, no conversación
