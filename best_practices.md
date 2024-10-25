Best Practices Implementadas
Este documento sirve para detallar las prácticas recomendadas 
implementadas para mejorar la seguridad de la apliacición EvaluacionACG-A0P.

## Cifrado de Datos Sensibles ##

  * Descripción: Todos los datos sensibles se transmiten y almacenan mediante
  algoritmos de cifrado sólidos.
  * Mejora de Seguridad: Protege la información sensible de accesos no
  autorizados en caso de algún robo o intercepción de datos.

## Comunicación Segura Mediante HTTPS ##

  * Descripción: Todas las comunicaciones de red utilizan el protocolo HTTPS
  para garantizar una transmisión de datos segura.
  * Mejora de Seguridad: HTTPS protege contra ataques de intermediarios (MITM),
  asegurando que los datos no sean interceptados ni modificados en tránsito.

## Validación y Sanitización de Entradas ##

  * Descripción: Todas las entradas del usuario son validadas y sanitizadas
  para evitar ataques de inyección de código y SQL.
  * Mejora de Seguridad: La validación de entradas ayuda a prevenir inyecciones
  maliciosas que pueden comprometer la integridad de la aplicación y la base de datos.
