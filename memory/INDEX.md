# Índice de Memoria del Sistema Clawbot

> **Estructura optimizada para recuperación rápida y consistencia**  
> **Última actualización:** 2026-02-17

---

## Estructura Jerárquica

```
memory/
├── INDEX.md                 ← Este archivo - mapa de navegación
├── README.md                ← Guía de uso del sistema de memoria
├── 
├── strategic/               🎯 Objetivos de largo plazo
│   ├── objectives.md
│   ├── principles.md
│   └── vision.md
│
├── projects/                📁 Proyectos activos (carpeta por proyecto)
│   └── _template/           ← Plantilla para nuevos proyectos
│       ├── context.md
│       ├── decisions.md
│       └── status.md
│
├── technical/               ⚙️ Stack y decisiones técnicas
│   ├── stack.md
│   ├── apis.md
│   ├── patterns.md
│   └── decisions/
│
├── behavioral/              👤 Preferencias de Radulenko
│   ├── preferences.md
│   ├── patterns.md
│   └── context.md
│
├── decisions/               🔀 Decisiones críticas documentadas
│   └── YYYY-MM-DD-{slug}.md
│
├── meta/                    🧠 Evolución del sistema
│   ├── soul-versions/       ← Versiones de SOUL.md
│   │   ├── v1.0-20260217.md
│   │   └── CURRENT -> v1.0
│   ├── evolution.md
│   └── audit.md             ← Log de cambios estructurales
│
├── daily/                   📅 Notas de sesión (raw)
│   └── YYYY-MM-DD.md
│
├── synthesis/               🔗 Conocimiento cruzado y refinado
│   ├── learnings.md
│   ├── patterns-systemic.md
│   └── insights.md
│
├── templates/               📋 Plantillas reutilizables
│   ├── decision.md
│   ├── project-init.md
│   └── session-log.md
│
└── indices/                 🔍 Índices para búsqueda rápida
    ├── topics.json
    ├── people.json
    └── tags.md
```

---

## Protocolos de Acceso

### Escritura
| Tipo | Trigger | Destino |
|------|---------|---------|
| Decisión crítica | Post-decisión validada | `decisions/` |
| Preferencia detectada | Confirmación implícita | `behavioral/` |
| Aprendizaje sintetizado | Heartbeat/Reflexión | `synthesis/` |
| Estado de proyecto | Actualización periódica | `projects/{name}/` |

### Lectura
1. **Pre-respuesta:** `strategic/` + `behavioral/` + contexto de proyecto
2. **Post-tarea:** Síntesis → `synthesis/`
3. **Audit:** `meta/audit.md` + `decisions/`

---

## Rendimiento
- Búsqueda O(1): Índices en `indices/`
- Recuperación contextual: Jerarquía explícita
- Sin duplicación: Links en lugar de copias
- Compresión semántica: Solo conocimiento, no conversación
