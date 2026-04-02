Data Lakehouse Laboratory (Delta Lake + Spark)

Este proyecto es un laboratorio de datos local diseñado bajo la Medallion Architecture (Bronze, Silver, Gold), utilizando Delta Lake como formato de tabla y PySpark para el procesamiento.

Arquitectura Actual (v1.0.0)

Actualmente, el proyecto utiliza una arquitectura optimizada que conecta directamente a los metadatos:
  - Motor de Procesamiento: PySpark (Spark 3.5.5).
  - Formato de Tabla: Delta Lake.
  - Catálogo de Metadatos: Hive Metastore conectado a MySQL.
  - Almacenamiento: MinIO.
  - Consulta SQL: Trino (conectado al catálogo Hive Metastore de MySQL).

Historial de Versiones y Evolución

Este repositorio mantiene un registro de la evolución de la infraestructura:
  - v1.0.0 (Legacy): 

Configuración del Entorno

Para replicar este laboratorio, asegúrate de contar con:
  - Docker & Docker Compose (puertos 3306 para MySQL y 9000 para MinIO).
  - Driver JDBC: Descargar mysql-connector-j-9.5.0.jar para el contenedor de Trino.
  - Variables de Entorno: Configurar las credenciales de S3 (AWS_ACCESS_KEY_ID y AWS_SECRET_ACCESS_KEY).
