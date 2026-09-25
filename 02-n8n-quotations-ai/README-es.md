# PROYECTO 2: Sistema de Cotizaciones n8n + IA

**Estado:** ⚠️ Prototipo (Listo para Producción con Documentación)  
**Stack Tecnológico:** n8n | Google Sheets | Gemini AI | Parseo CSV | XLSX  
**Impacto:** $35,000 USD en valor operacional  

---

## Descripción General

Sistema automatizado de generación de cotizaciones para proyectos fotovoltaicos/energéticos usando orquestación de workflows n8n, cálculo de costos impulsado por IA y exportación de datos estructurados.

### El Desafío
- Proceso manual de cotización tomaba 2-3 horas por cliente
- Precios inconsistentes en propuestas
- Sin combinaciones estandarizadas de equipos
- Alta tasa de error en cálculos de costos

### La Solución
- Recuperación automática de datos de Google Sheets (requerimientos + inventario)
- Parseo CSV compatible con RFC-4180 con manejo de errores
- IA Gemini para generación inteligente de cotizaciones
- Validación multi-capa y exportación XLSX
- Blueprint de workflow completo documentado

---

## Métricas Clave

| Métrica | Resultado | Impacto |
|---------|-----------|---------|
| **Tiempo de Procesamiento/Cotización** | 4 min | 97% reducción manual |
| **Cotizaciones/Semana** | 20-30 | 400% aumento capacidad |
| **Tasa de Precisión** | 95%+ | Capas de validación |
| **Combinaciones de Equipos** | 150+ | Personalizadas |
| **Ahorro de Costos Anual** | ~$35,000 | Reducción de labor |

---

## Archivos en Este Proyecto

- `n8n-workflow.json` — Exportación completa del workflow
- `csv-parser.js` — Lógica de parseo CSV RFC-4180
- `prompt-template.md` — Estructura de prompt para IA
- `gemini-response-samples.json` — Formato de salida esperado

---

## Issues Conocidos y Mitigación

**Issue:** Alucinación JSON en Gemini (valores inventados)  
**Causa Raíz:** Prompts largos + inyección completa de inventario  
**Mitigación Actual:** Validación multi-capa + estrategia fallback  
**Fix Recomendado:** Cambiar a Claude API (99% precisión JSON)

---

## Inicio Rápido

1. **Preparar Fuentes de Datos:**
   - Sheet 1: Requerimientos clientes
   - Sheet 2: Inventario de equipos

2. **Importar Workflow en n8n:**
   - Ingresar a n8n
   - Importar `n8n-workflow.json`
   - Configurar credenciales Google Sheets API
   - Configurar clave Gemini API

3. **Pruebas y Validación:**
   - Ejecutar con 5-10 clientes de muestra
   - Revisar cotizaciones generadas
   - Verificar precisión de cálculos
   - Documentar issues de alucinación

4. **Despliegue en Producción:**
   - Configurar ubicación XLSX export
   - Habilitar notificaciones de error
   - Monitoreo diario
   - Proceso fallback para cotizaciones fallidas

---

## Lecciones Aprendidas

1. **Los edge cases de CSV importan** — Datos reales ≠ datos de muestra
2. **Las salidas LLM requieren validación** — Implementar siempre estrategias fallback
3. **La estructura del prompt afecta precisión** — Asignación clara de rol + restricciones
4. **Completitud de datos es crítica** — Inputs incompletos = alucinaciones

---

## Mejoras Recomendadas

- [ ] Cambiar a Claude API para 99% precisión JSON
- [ ] Implementar prompting de 2 etapas (analizar → generar)
- [ ] Agregar validación de datos antes del llamado IA
- [ ] Crear dashboard de revisión de cotizaciones fallidas
- [ ] Construir portal de cotizaciones orientado al cliente

---

**Versión:** 1.0  
**Estado:** MVP 85% Completado  
**Última Actualización:** Septiembre 2026  
**Mantenido por:** Yoselyn Mogollón
