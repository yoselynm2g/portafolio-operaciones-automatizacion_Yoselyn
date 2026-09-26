# Prototipo de cotizaciones con n8n y Gemini

[English](README-en.md) · [Inicio / Home](../README.md)

**Herramientas:** n8n · Google Sheets · Gemini API · nodos JavaScript.
**Estado:** prototipo en desarrollo, iniciado en 2025 y retomado en 2026.

## Reto
Explorar cómo transformar requerimientos de clientes y datos de productos en propuestas de cotización estructuradas.

## Mi aporte
Configuré un flujo con solicitudes HTTP, preparación de datos mediante nodos JavaScript, procesamiento por registros y una llamada a Gemini. El diseño incluye una salida prevista a XLSX.

## Entregable
Un prototipo de flujo y capturas de pruebas que permiten revisar sus etapas y detectar problemas en la entrada y en las respuestas del modelo.

## Aprendizaje y alcance
Las pruebas no produjeron cotizaciones suficientemente consistentes para uso operativo. En una captura aparecen campos sin resolver en el mensaje enviado al modelo, lo que señala un punto de revisión en el mapeo de datos. No se atribuye el problema exclusivamente al plan gratuito de la API.

El flujo no llegó a producción. No se ha acreditado una exportación completa y usable de cotizaciones ni se presentan métricas de ahorro. La revisión actual parte de estructurar mejor los datos de clientes y productos.

El [ejemplo JSON](../02-quotation-sample.json) es una estructura conceptual creada para documentación, no una cotización generada por el prototipo. Las capturas originales se conservan de forma privada porque contienen datos de clientes.
