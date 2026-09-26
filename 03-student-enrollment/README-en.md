# Relational database for a student assistantship program

[Español](README-es.md) · [Inicio / Home](../README.md)

**Tool:** SQL Server.
**Context:** a learning project built after my employment at UNIMET, inspired by processes encountered during my administrative work.

## Challenge
Represent relationships among students, degree programs, benefit programs, assessments, departments and supervisors to support structured queries.

## My contribution and deliverable
Built an 11-table relational database with primary and foreign keys, junction tables and analytical queries. Retained the schema, scripts and a design diagram. I validated the scripts in SQL Server before publication.

## Queries and results
My queries on the original exercise returned 82 students and 37 approved students. These figures belong to that working dataset; they are neither synthetic-demo results nor a measured operational improvement at UNIMET.

The demonstration version I retain locally uses fictional records: 8 students, 16 assessments and 5 students with at least one approval. Distinguishing students from assessments avoids counting one person multiple times.

## Available material
- [SQL project repository](https://github.com/yoselynm2g/Portafolio_Yoselyn/tree/main/Project_2_RelationalDB/Project_2_RelationalDB).
- This portfolio documents the case scope; SQL files are maintained in the dedicated repository.

This later learning project is not presented as a system deployed during my employment. Institutional reporting work is described in [project 4](../04-scholarships-bi/README-en.md).
