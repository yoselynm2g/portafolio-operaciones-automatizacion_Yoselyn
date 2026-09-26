# Base de datos relacional para un programa de ayudantías

[English](README-en.md) · [Inicio / Home](../README.md)

**Herramienta:** SQL Server.
**Contexto:** proyecto de aprendizaje construido después de mi empleo en UNIMET, inspirado en procesos que conocí durante mi trayectoria administrativa.

## Reto
Representar las relaciones entre estudiantes, carreras, programas, evaluaciones, departamentos y supervisores para consultar la información de forma estructurada.

## Mi aporte y entregable
Construí una base relacional de 11 tablas, con claves primarias y foráneas, tablas de unión y consultas de análisis. Conservé el esquema, los scripts y un diagrama de diseño. Validé los scripts en SQL Server antes de su publicación.

## Consultas y resultados
El ejercicio original produjo 82 estudiantes y 37 aprobados según mis consultas. Estas cifras pertenecen a ese conjunto de trabajo; no representan resultados de la demostración sintética ni una mejora operativa medida en UNIMET.

La versión de demostración que conservo localmente utiliza datos ficticios: 8 estudiantes, 16 evaluaciones y 5 estudiantes con al menos una aprobación. Diferenciar estudiantes de evaluaciones evita contar varias veces a una misma persona.

## Material disponible
- [Repositorio del proyecto SQL](https://github.com/yoselynm2g/Portafolio_Yoselyn/tree/main/Project_2_RelationalDB/Project_2_RelationalDB).
- En este portafolio se documenta el alcance del caso; los archivos SQL se mantienen en el repositorio específico.

Este desarrollo posterior no se presenta como un sistema implantado durante mi empleo. El trabajo institucional de reportes se describe en el [proyecto 4](../04-scholarships-bi/README-es.md).
