# Nombre del Proyecto #
Evaluación Mapas ACG

# Descripción
Este proyecto es una aplicación para Android sobre Mapas Concetados a una api de google que 
implementa un analisis de seguridad contra vulnerabilidades que se puedan presentar en este proyecto.

## Vulnerabilidades Identificadas

- Permisos:
  * com.example.evaluacionacg_a0p.DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION
  no está identifico en la referencia de Android.

- Receivers Exportados:
  * Receiver accesible externamente: El receptor de difusión androidx.profileinstaller.ProfileInstallReceiver
  está protegido por un permiso. Si este permiso es normal o peligroso, una app maliciosa podría tener acceso.

- Análisis del archivo manifest:
  * Compatibilidad: La aplicación soporta versiones de android de 7.0
  hacia adelante lo que podría exponerla a vulnerabilidades sin parches.
  * Depuración habilitada: android:debuggable está en true, lo que permite que depuraciones externas
  se puedan conectar a la aplicación en dispositivos.
  * Backup habilitado: android:allowBackup=true permite que los datos se puedan copiar
  mediante ADB, exponiendo información sensible.

- Certificados de Firma de Apliación:
  * Modo depuración: La aplicación está firmada mediante un certificado
  para depuración, lo que la hace insegura para producción.
  * SHA1 vulnerable: La aplicación utiliza el algoritmo SHA1 para firmar,
  que es vulnerable a ataques de colisión de hash.

## Mejoras Implementadas
- Protección de Receivers: La aplicación usa permisos para proteger receptores de difusión,
  aunque la revisión de permisos es necesaria para asegurar su nivel de seguridad.

## Documentación
- [Best Practices](best_practices.md)
- [Security Tips](security_tips.md)
- [Security Improvement Program](security_improvement_program.md)
## Cómo Ejecutar la Aplicación de Forma Segura
1. Clonar el repositorio
2. Importar en Android Studio y asegurarse de configurar la firma de producción
3. Verificar permisos y ajustar el Manifest según las recomendaciones de seguridad
## Reporte de Vulnerabilidades realizadas se encuentra en el archivo `vulnerability_report.pdf`.
