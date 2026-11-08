# cicd-vulnerable-demo

> **Aviso:** repositorio **deliberadamente inseguro**, parte del proyecto Cloud Security Assessment. Sirve para demostrar riesgos de CI/CD en GitHub Actions de forma aislada.

## Normas

- **Sin permisos sobre Azure:** no se configuran credenciales, secretos ni identidades con roles. Como mucho, una identidad de prueba sin ningún rol asignado.
- Los secretos que aparecen son **ficticios o canario**: no dan acceso a nada.
- Los workflows de este repositorio no se reutilizan en ningún otro.

## Escenarios previstos

| ID | Escenario |
|---|---|
| GH-01 | Credenciales hardcodeadas |
| GH-02 | Secreto eliminado del código pero presente en el historial de Git |
| GH-03 | Ficheros sensibles versionados (fichero canario) |
| GH-04 | Permisos excesivos en workflows |
| GH-05 | Acciones sin fijar a un SHA |
| GH-06 | Rama principal sin protección |
| CD-01 | Confianza OIDC demasiado amplia (identidad sin roles) |

Los controles del despliegue real (CD-02 a CD-04) se revisan en el repositorio `cloud-security-assessment`, que contiene además la versión corregida (TO-BE).
