# Visión general del sistema de gestión de monitorios

Este documento resume la estrategia, el alcance funcional y los entregables previos al desarrollo del software para la administración integral de expedientes monitorios.

## Objetivo del producto
Construir una plataforma que permita a administradores de fincas y equipos legales gestionar el ciclo de vida completo de las reclamaciones monitorias contra propietarios con deudas, desde el acuerdo de junta hasta la recuperación o cierre del expediente, garantizando trazabilidad documental, control de costes y cumplimiento normativo.

## Usuarios y perfiles
- **Administrador de fincas**: inicia el expediente, registra acuerdos de junta y coordina las comunicaciones con los propietarios.
- **Equipo jurídico**: prepara escritos judiciales, da seguimiento a las fases procesales, gestiona oposiciones y ejecuciones.
- **Soporte administrativo**: carga documentación, actualiza hitos, registra pagos y comunicaciones.
- **Dirección/Comité**: consulta indicadores y reportes globales.

## Alcance funcional
1. **Gestión de expedientes**
   - Alta de expedientes con datos del deudor, comunidad y deuda certificada.
   - Importación de expedientes históricos con información incompleta, marcando su estado y pendientes.
   - Línea de tiempo que centraliza hitos, documentos y comentarios.

2. **Gestión documental**
   - Almacenamiento en Firebase Storage de actas, certificaciones, burofaxes, escritos judiciales, resoluciones y constancias de pago.
   - Generación automática de documentos a partir de plantillas y datos del expediente.
   - Control de versiones, metadatos y permisos de descarga/visualización.

3. **Comunicaciones y notificaciones**
   - Registro de requerimientos de pago (burofax), constancias de tablón y acuses.
   - Alertas por plazos legales (respuesta burofax, presentación monitorio, ejecución).
   - Integración con servicios de correo y mensajería para avisos internos.

4. **Flujo procesal monitorio**
   - Seguimiento de cada etapa: presentación, admisión, decreto, oposición, ejecución de títulos judiciales, embargos.
   - Registro de costes asociados (nota simple, burofax, tasas, procurador, etc.).
   - Soporte para anexar escritos de personación, oposición, recursos y cierre.

5. **Pagos y conciliaciones**
   - Registro de pagos parciales/totales, con reflejo en el saldo de la deuda.
   - Generación de escritos de desistimiento, archivo o notificación de pago.
   - Control de embargos y distribución de cantidades recuperadas.

6. **Reportes y analítica**
   - Dashboards con indicadores clave: expedientes activos, etapas procesales, tasas de recuperación, tiempos medios.
   - Exportación de informes en PDF/CSV.
   - Segmentación por comunidad, propietario, estado del expediente o antigüedad.

## Requisitos no funcionales clave
- Seguridad y cumplimiento RGPD (encriptación, permisos, registro de accesos, retención de datos).
- Disponibilidad alta y respaldo de documentos críticos.
- Escalabilidad para manejar múltiples comunidades y expedientes concurrentes.
- Auditoría completa de acciones y cambios.

## Entregables previos al desarrollo
1. **Mapa de procesos** documentando cada fase del expediente monitorio.
2. **Modelo de datos** preliminar para Firestore y Storage con esquema de colecciones, subcolecciones e índices.
3. **Diseño de reglas de seguridad** de Firebase (auth, firestore.rules, storage.rules) y plan de roles.
4. **Wireframes** para dashboard, ficha de expediente, generador de documentos y carga de pagos.
5. **Backlog priorizado** con historias de usuario, criterios de aceptación y dependencias.
6. **Plan de despliegue** que cubra entornos (dev, staging, prod) y pipelines de CI/CD.
7. **Estrategia de migración** para expedientes históricos con checklist de datos mínimos.

## Dependencias y riesgos
- Validar disponibilidad de servicios externos (burofax, firma digital, autenticación de usuarios).
- Asegurar cumplimiento legal para almacenamiento de documentación sensible.
- Coordinar la importación de datos históricos para no retrasar el inicio de operaciones.

## Próximos pasos sugeridos
1. Realizar workshops con stakeholders para completar el checklist previo al desarrollo.
2. Documentar procesos y modelos de datos detallados.
3. Crear prototipos UX y validar con usuarios clave.
4. Configurar el proyecto Firebase inicial y definir reglas de seguridad.
5. Preparar plan de proyecto y asignar responsabilidades.

Con estos insumos cubiertos, el equipo podrá iniciar la implementación con claridad sobre objetivos, alcance, riesgos y gobernanza del sistema.
