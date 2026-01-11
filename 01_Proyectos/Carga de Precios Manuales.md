
Este es un proceso mensual crítico que debe ejecutarse puntualmente el día 3 de cada mes para asegurar la precisión de las valuaciones.

Hay dos procedimientos para hacer esto:

Procedimiento 1. Carga de precios manuales de Gletir del día 3 al 5 de cada mes. Todo el proceso lo hace Sistemas.

- En este caso hay que obtener el archivo (Excel) de precios de cierre de Gletir con todas las carteras.
- Se carga en la base de datos DATACUSTODIO en la tabla v1.DATA_HOLDINGS
- Se ejecuta por partes el proceso en la base de datos VISIONDB procedimiento SP_AutomatizacionPreciosGletir

Procedimiento 2. Carga de precio manuales de otros custodios (después de terminar Gletir). Los datos los envía la Alicia en Excel, lo carga Sistemas.

- Se obtiene el archivo que manda Alicia
- Se carga en la base de datos VISIONDB en la tabla instrvalor_preciospegados
- Se ejecuta por partes el proceso en la base de datos VISIONDB procedimiento sp_ActualizarPreciosMasivo

Responsables:

- 1 - Administrador
- 59 - Alicia
- 80 - Jorge