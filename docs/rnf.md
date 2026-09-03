# Requerimientos no funcionales

| # | Atributo | Métrica | Umbral | Condición de carga | Verificación | Consecuencia si no se cumple |
|---|---|---|---|---|---|---|
| RNF-01 | Rendimiento | Percentil 95 del tiempo de respuesta de consultas | Menor o igual a 2 segundos | 100 usuarios concurrentes consultando documentos | Prueba de carga con JMeter | Los usuarios experimentan demoras y disminuye la productividad |
| RNF-02 | Disponibilidad | Porcentaje mensual de disponibilidad del servicio | Mínimo 99,5 % | Operación continua, excluyendo mantenimientos programados | Monitoreo y reporte mensual | Los usuarios no pueden consultar ni administrar documentos |
| RNF-03 | Seguridad | Porcentaje de operaciones protegidas que requieren autenticación y autorización | 100 % | Acceso a carga, consulta, descarga y eliminación de documentos | Pruebas de seguridad y revisión de permisos | Puede producirse acceso, modificación o divulgación no autorizada de información |

## Escenarios completos

### Escenario 1 - Rendimiento de consultas

- **Fuente:** Usuario autenticado.
- **Estímulo:** Realiza una consulta de documentos utilizando filtros de nombre, categoría o fecha.
- **Artefacto:** API de consulta y base de datos del gestor documental.
- **Entorno:** Operación normal con 100 usuarios concurrentes.
- **Respuesta:** El sistema valida la autorización, procesa los filtros y devuelve los resultados paginados.
- **Medida:** El percentil 95 del tiempo de respuesta debe ser menor o igual a 2 segundos.

### Escenario 2 - Disponibilidad

- **Fuente:** Sistema de monitoreo.
- **Estímulo:** Detecta que una instancia del servicio no responde.
- **Artefacto:** Servicio backend del gestor documental.
- **Entorno:** Operación normal.
- **Respuesta:** La plataforma registra la falla y mantiene disponible el servicio mediante una instancia saludable.
- **Medida:** Disponibilidad mensual mínima de 99,5 %.

### Escenario 3 - Protección de documentos

- **Fuente:** Usuario autenticado sin permisos sobre un documento.
- **Estímulo:** Intenta consultar o descargar el archivo.
- **Artefacto:** API de documentos y servicio de almacenamiento.
- **Entorno:** Operación normal.
- **Respuesta:** El sistema rechaza la solicitud, no revela el contenido y registra el intento en la auditoría.
- **Medida:** El 100 % de los accesos no autorizados debe ser rechazado y auditado.
