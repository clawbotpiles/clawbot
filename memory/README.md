# Sistema de Memoria Clawbot

> **Arquitectura:** Jerárquica semántica  
> **Optimización:** Máxima velocidad de recuperación + mínima redundancia  

---

## Propósito
Esta estructura permite al sistema:
- **Recordar** lo importante sin acumular conversación cruda
- **Recuperar** contexto relevante en tiempo O(1) mediante índices
- **Evolucionar** mediante versionado y auditoría
- **Proteger** información sensible con jerarquía de acceso

---

## Flujo de Datos

```
Conversación → Síntesis → Almacenamiento → Índice → Recuperación
     ↓              ↓             ↓            ↓           ↓
  Temporal      Persistente   Estructurado   Rápido    Contextual
```

---

## Convenios de Nomenclatura

- **Fechas:** ISO-8601 (YYYY-MM-DD)
- **Slugs:** kebab-case (ej: `nueva-estructura`)
- **Decisiones:** `YYYYMMDD-{slug}.md`
- **Diarios:** `YYYY-MM-DD.md`
- **Versiones:** `v{N.M}-{YYYYMMDD}.md`

---

## Seguridad

| Nivel | Ubicación | Acceso |
|-------|-----------|--------|
| Público | `synthesis/`, `technical/patterns` | Cualquier agente |
| Interno | `projects/`, `decisions/` | Agente coordinador |
| Sensible | `behavioral/`, credenciales | Memoria volátil únicamente |

---

## Mantenimiento

- **Diario:** Log de sesión en `daily/`
- **Semanal:** Revisar índices, compactar daily logs
- **Mensual:** Revisar sintetizaciones, actualizar strategic/
- **Trimestral:** Revisión estructural completa

---

**Creado:** 2026-02-17  
**Versión estructura:** 1.0
