# Gestor de documentos

Proyecto de la asignatura Arquitectura de Sistemas Computacionales, grupo 641A.

## Problema

Las organizaciones necesitan almacenar, clasificar, consultar y controlar documentos de forma segura. El sistema permitirá centralizar archivos y sus metadatos, facilitar búsquedas y mantener trazabilidad sobre las operaciones realizadas.

## Alcance inicial

- Registrar documentos y sus metadatos.
- Consultar y filtrar documentos.
- Descargar documentos autorizados.
- Controlar el acceso de los usuarios.
- Registrar eventos de auditoría.

## Integrantes

| Nombre | Usuario de GitHub | Rol en el proyecto |
|---|---|---|
| Karen Alexa Caicedo | [kalet17](https://github.com/kalet17) | Desarrollo y arquitectura |

> Este proyecto se desarrolla individualmente. La estudiante pertenece al grupo 641A.

## Estado del proyecto

| Hito | Estado | Tag |
|---|---|---|
| Hito 1 - Requerimientos y arquitectura | En curso | Pendiente |
| Hito 2 - Infraestructura, red, datos y seguridad | Pendiente | Pendiente |
| Hito 3 - Automatización, observabilidad y costos | Pendiente | Pendiente |
| Hito 4 - Sustentación | Pendiente | Pendiente |
| Hito 5 - Dossier final | Pendiente | Pendiente |

## Estructura del repositorio

| Carpeta | Contenido |
|---|---|
| `docs/` | Documentación de arquitectura, requerimientos y decisiones |
| `docs/adr/` | Registros de decisiones arquitectónicas |
| `src/` | Código fuente de la aplicación |
| `infra/` | Configuración de infraestructura, proxy y observabilidad |
| `tests/carga/` | Pruebas de rendimiento |
| `evidencias/` | Capturas e informes de los talleres |
| `.github/workflows/` | Automatizaciones de integración continua |

## Cómo ejecutar

Pendiente. Se documentará durante el Hito 2 cuando se defina la tecnología de ejecución.

## Seguridad

- Nunca se deben subir contraseñas, tokens, llaves ni credenciales reales.
- Las variables requeridas se documentan en `.env.example`.
- Los valores locales deben almacenarse en un archivo `.env`, excluido mediante `.gitignore`.

## Flujo de trabajo

- Trabajar en una rama diferente de `main`.
- Crear commits pequeños con mensajes descriptivos.
- Incorporar cambios mediante pull requests.
- Revisar los archivos modificados antes de aprobar cada incorporación.

## Notas

- En Windows se recomienda trabajar desde `C:\dev\` y utilizar Git Bash.
- Después de clonar, ejecutar `git config core.hooksPath .githooks` si se implementa el reto opcional.

