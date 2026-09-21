# Examen-Iplacex
1. Descripcion del proyecto:

Este repositorio contiene la arquitectura base para un framework de pruebas automatizadas y entrega continua (CI/CD) desarrollado en Java. Su objetivo principal es estandarizar el ciclo de vida de desarrollo de software (SDLC) mediante la integración de controles de calidad estrictos, pruebas automatizadas y despliegues seguros y controlados en entornos de prueba

2. Explicacion de como ejecutar las pruebas y pipeline:

Ejecución del Pipeline de CI/CD
El pipeline se encuentra automatizado en la nube mediante GitHub Actions y está configurado en el archivo .github/workflows/ci.yml.
Disparadores: Se ejecuta de forma automática ante cada push o Pull Request hacia las ramas main o develop.

Stages del Pipeline:
Build & Unit Tests: Compila el código fuente en Java 17 y ejecuta la suite de pruebas unitarias.
Acceptance Tests: Ejecuta las pruebas de aceptación y verificación funcional.
Staging Deployment: Simula el empaquetado y despliegue del artefacto en el ambiente de prueba.
Rollback Strategy: Mecanismo de resiliencia automatizado (if: failure()) que interrumpe despliegues defectuosos y ejecuta un rollback ante fallos operativos.

3. Evidencias del funcionamiento:

Ejecución Exitosa del Pipeline de CI
Pipeline validando la compilación, pruebas unitarias y análisis estático en la rama develop.

<img width="1088" height="273" alt="image" src="https://github.com/user-attachments/assets/d224d57b-f009-46fe-afc2-db1a8cccd829" />
<img width="1088" height="296" alt="image" src="https://github.com/user-attachments/assets/541a253f-fddc-4738-b63a-888a617bc488" />

Evidencia de Despliegue
<img width="1088" height="298" alt="image" src="https://github.com/user-attachments/assets/07d8dfab-bcf6-4e99-93c8-202c48ace3e1" />
