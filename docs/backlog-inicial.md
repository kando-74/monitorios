# Backlog inicial y roadmap previo al desarrollo

El siguiente backlog organiza el trabajo pendiente antes de iniciar la implementación. Incluye historias de usuario clave, dependencias y entregables previos.

## Roadmap de alto nivel
1. **Discovery y alineación** (Semana 1-2)
   - Workshops con stakeholders para validar requerimientos y priorizar funcionalidades.
   - Documentación de procesos legales y puntos de dolor actuales.
2. **Diseño funcional y técnico** (Semana 3-4)
   - Modelado de datos, definición de roles y reglas de seguridad.
   - Wireframes y prototipos de UX.
3. **Preparación operativa** (Semana 5)
   - Configuración inicial de Firebase y entornos.
   - Planificación de migración de datos históricos.
4. **Inicio de desarrollo** (Semana 6)
   - Establecer repositorios, pipelines y convenciones de código.

## Historias de usuario prioritarias (previas al desarrollo)

### 1. Como administrador de fincas
- **Quiero** registrar todos los hitos de un expediente desde el acuerdo de junta hasta la ejecución, **para** mantener trazabilidad total.
  - Criterios de aceptación: listado de hitos definidos, campos obligatorios y documentos asociados.
- **Quiero** importar expedientes monitorios históricos con información incompleta, **para** continuar su gestión en la plataforma.
  - Criterios de aceptación: proceso documentado, checklist de datos mínimos, estados especiales para expedientes importados.

### 2. Como abogado
- **Quiero** contar con plantillas preconfiguradas de escritos (monitorio, ejecución, personación), **para** agilizar la preparación de documentos.
  - Criterios de aceptación: inventario de plantillas, metadatos necesarios, proceso de personalización.
- **Quiero** recibir alertas de plazos críticos y fases procesales, **para** no perder vencimientos.
  - Criterios: definición de eventos, canales de alerta, responsables.

### 3. Como responsable de operaciones
- **Quiero** un dashboard con indicadores clave del estado de los expedientes, **para** monitorizar la cartera de deudas.
  - Criterios: métricas a mostrar, fuentes de datos, frecuencia de actualización.
- **Quiero** asegurar que el sistema cumple con RGPD y retención documental, **para** evitar riesgos legales.
  - Criterios: políticas de acceso, retención de datos, auditoría de acciones, encriptación.

## Dependencias y tareas técnicas
- Definir estructura de colecciones y subcolecciones en Firestore (expedientes, hitos, documentos, pagos, auditoría).
- Diseñar reglas de seguridad (Firestore, Storage) basadas en roles y propietarios del expediente.
- Planificar integraciones externas (servicio de burofax, APIs judiciales, correo).
- Establecer nomenclatura de documentos en Storage y metadatos.
- Preparar pipeline de CI/CD (lint, tests, despliegue automático a Firebase Hosting/Functions).

## Documentos y artefactos a producir
- **Mapa de procesos** completo del monitorio (BPMN o diagrama de flujo).
- **Modelo de datos** entidad-relación adaptado a Firestore.
- **Guías de UX** con wireframes y especificaciones de componentes.
- **Checklist de cumplimiento** (RGPD, seguridad, auditoría).
- **Plan de migración** para expedientes existentes.
- **Plan de pruebas** inicial (casos de uso críticos, criterios de aceptación).

## Riesgos y mitigaciones
- **Información incompleta en expedientes históricos** → Crear estados y checklist específicos, capacitar al equipo en la migración.
- **Cambios en normativa** → Establecer revisión legal trimestral y canal de comunicación con asesoría jurídica.
- **Sobrecarga operativa** → Priorizar MVP, automatizar alertas y reportes, definir capacidad del equipo.

## Definición de “listo para desarrollar”
Un módulo o historia estará listo para pasar a desarrollo cuando:
1. Requisitos funcionales y no funcionales documentados y validados.
2. Wireframes/prototipos aprobados por stakeholders clave.
3. Modelo de datos y reglas de seguridad revisados con el equipo técnico.
4. Criterios de aceptación y casos de prueba definidos.
5. Dependencias externas identificadas y planificadas.

Cumplir esta definición de listo asegurará que el equipo pueda comenzar a programar con claridad y sin bloqueos mayores.
