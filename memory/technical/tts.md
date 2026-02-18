# Configuración TTS

> **Motor:** sherpa-onnx  
> **Modelo:** Piper en_US lessac (high)  
> **Fecha instalación:** 2026-02-18  
> **Estado:** ✅ OPERATIVO  
> **Ubicación:** `~/.openclaw/tools/sherpa-onnx-tts/`

---

## Componentes

| Componente | Tamaño | Ubicación |
|------------|--------|-----------|
| Runtime | 27.8 MB | `runtime/` (bin/, lib/, include/) |
| Modelo Piper | 110 MB | `models/vits-piper-en_US-lessac-high/` |

## Notas Técnicas

- TTS completamente local y offline
- Motor ONNX Runtime optimizado
- Sin dependencias de APIs externas
- Voz: Inglés estadounidense (female, lessac)
- Tiempo de síntesis: < 2 segundos

## Variables de Entorno Configuradas

- `SHERPA_ONNX_RUNTIME_DIR`
- `SHERPA_ONNX_MODEL_DIR`

## Prueba de Voz

✅ **2026-02-18** - Mensaje de prueba generado exitosamente:
> "Hola Radulenko. Soy Clawbot. Mi voz local está operativa."

## Uso Disponible

- Storytelling / Narración
- Notificaciones de audio
- Conversión de logs a voz
- Mensajes proactivos personalizados
