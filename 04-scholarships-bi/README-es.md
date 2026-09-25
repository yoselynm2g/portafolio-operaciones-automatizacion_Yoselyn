# PROYECTO 4: Becas e Inteligencia de Negocio

**Estado:** ✅ Producción  
**Stack Tecnológico:** Excel | Google Sheets | Power BI | SQL  
**Organización:** Universidad Metropolitana (779 estudiantes únicos)  
**Impacto:** $55,000 USD en valor operacional

---

## Descripción General

Sistema de consolidación de datos e BI que unificó 5 bases de datos de becas separadas en una única fuente de verdad con dashboards en tiempo real para análisis de costos, validación de beneficios y toma de decisiones estratégicas.

### El Desafío
- 5 sistemas separados rastreando becas de estudiantes (datos fragmentados)
- 779 estudiantes únicos en múltiples programas
- Reconciliación manual tomaba 8 horas/mes
- Sin visibilidad de costos totales de becas por programa
- Beneficios/descuentos aplicados de forma inconsistente

### La Solución
- Consolidación de 5 fuentes de datos en base datos Google Sheets unificada
- Reglas de validación comparando descuentos esperados vs. aplicados
- Dashboards Ejecutivo, Programa y Carrera
- Análisis de costos por estudiante, programa y carrera
- Reportes mensuales automatizados a liderazgo

---

## Métricas Clave

| Métrica | Resultado | Impacto |
|---------|-----------|---------|
| **Estudiantes Consolidados** | 779 únicos | 100% visibilidad |
| **Completitud de Datos** | 98% | Excepciones mínimas |
| **Tasa Error Validación** | 2.1% | 27 issues identificados |
| **Visibilidad Costos** | +100% | Presupuestación exacta |
| **Documentación Excepciones** | 100% | Cumplimiento normativo |
| **Tiempo Reporte Mensual** | 1 hora | Antes 8 horas |

**Valor Anual: ~$55,000 USD (labor + calidad decisiones)**

---

## Estructura Base de Datos

```
Base Datos Maestra (Google Sheets)
├── ID Estudiante | Nombre | Carrera
├── Programa(s) | Fecha Ingreso | Estado
├── Descuento Esperado % | Descuento Aplicado %
├── Monto Beneficio (USD) | Tipo Renovación
└── Estado Validación (VERDE/AMARILLO/ROJO)

Tabla Referencia
├── Estudiante → Programa(s) → Descuento Esperado
├── Razones Excepciones (Aprobaciones Consejo)
└── Calendario Renovación
```

---

## Componentes de Dashboard

**Dashboard Ejecutivo:**
- Costo total becas
- Distribución por programa
- Costo promedio por estudiante
- Tendencias mes a mes

**Dashboard Programa:**
- Tasas participación
- Costo por programa
- Presupuesto vs. real
- Tendencias ingreso

**Dashboard Carrera:**
- Participación por carrera
- Costo total por carrera
- Tendencias carrera-específicas
- Tasas excepciones por carrera

---

## Sistema de Validación

**Códigos de Estado:**
- **VERDE** — Esperado = Aplicado (sin issues)
- **AMARILLO** — Excepción documentada (Aprobación Consejo)
- **ROJO** — Flag de error (requiere resolución inmediata)

**Datos Ejemplo (25 estudiantes):**
- 23 casos VERDE (92%)
- 2 casos AMARILLO (8%) — Excepciones documentadas
- 0 casos ROJO (cumplimiento mantenido)

---

## Archivos en Este Proyecto

- `students-database-sample.xlsx` — Estructura base con 25 registros
- `benefits-validation-rules.md` — Lógica comparación descuentos
- `executive-dashboard-sample.xlsx` — Template BI y fórmulas

---

## Proceso Reporte Mensual

**Semana 1:**
1. Exportar nuevos ingresos de cada sistema
2. Estandarizar formatos y limpiar datos
3. Cargar en base datos maestra
4. Ejecutar chequeos validación

**Semana 2:**
1. Resolver excepciones (flags ROJO)
2. Documentar aprobaciones (status AMARILLO)
3. Actualizar tablas referencia

**Semana 3:**
1. Generar dashboards
2. Preparar reporte ejecutivo
3. Destacar excepciones y tendencias

**Semana 4:**
1. Presentar a Finanzas y Bienestar Estudiantil
2. Archivar para cumplimiento
3. Cerrar mes

---

## Lecciones Aprendidas

1. **Consolidación de datos abre decisiones** — Fuente única > 5 sistemas desconectados
2. **Validación en ingreso previene problemas** — Flag excepciones temprano
3. **Visibilidad en dashboard impulsa adopción** — Gente usa herramientas cuando ve ROI
4. **Documentación excepciones asegura cumplimiento** — Cada caso AMARILLO tiene aprobación

---

## Próximos Pasos

- [ ] Agregar analytics predictiva (pronóstico demanda becas)
- [ ] Automatizar notificaciones Finanzas en excedencias
- [ ] Construir gestión ciclo renovación
- [ ] Crear calculadora beneficios orientada estudiante
- [ ] Implementar dashboards comparación año a año

---

**Versión:** 1.0  
**Última Actualización:** Septiembre 2026  
**Mantenido por:** Yoselyn Mogollón
