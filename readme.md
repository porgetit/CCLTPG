# CCLTPG
## Documento de Visión y Alcance
### Plataforma de Gestión – Centro Cultural Lucy Tejada
#### Versión 1.0
**Integrantes:** Kevin E. Cardona, David J. T. Osorio, Esteban G. Jiménez

---

## 1. Introducción

El presente documento describe la visión y alcance de la plataforma de gestión del Centro Cultural Lucy Tejada (CCLT), institución cultural adscrita a la Alcaldía de Pereira, Colombia. Este documento establece el acuerdo inicial entre el cliente y el equipo de desarrollo respecto al sistema que se va a construir, delimitando el problema de negocio, los objetivos estratégicos, las características funcionales y no funcionales del sistema, su alcance por releases, los involucrados clave y el entorno de operación esperado.

El contenido del documento es el siguiente:

1. Introducción
2. Contexto de negocio
   - 2.1 Antecedentes
   - 2.2 Frase del problema
   - 2.3 Objetivos de negocio
3. Visión de la solución
   - 3.1 Frase de visión
   - 3.2 Características del sistema
4. Alcance y limitaciones
   - 4.1 Alcance
5. Contexto del sistema
   - 5.1 Resumen de Involucrados
   - 5.2 Diagrama de contexto
   - 5.3 Entorno de operación
6. Información adicional

---

## 2. Contexto de negocio

### 2.1 Antecedentes

El Centro Cultural Lucy Tejada es la principal sede administrativa encargada de promover y gestionar la actividad cultural en Pereira, Colombia. Su misión es fomentar el acceso a la formación artística en áreas como danza, música, teatro y artes plásticas, con impacto directo en cientos de estudiantes, educadores y familias. Actualmente, el centro no cuenta con una plataforma propia para la gestión académica y administrativa, dependiendo de la plataforma de la Alcaldía de Pereira para el registro de estudiantes, matrículas y administración básica.

### 2.2 Frase del problema

La dependencia de una plataforma externa (Alcaldía de Pereira) limita la autonomía operativa del Centro Cultural Lucy Tejada y dificulta una gestión optimizada de estudiantes, programas y clases. La ausencia de un sistema propio impide el seguimiento en tiempo real de asistencia y progreso académico, la generación automatizada de reportes, la visualización de métricas clave mediante dashboards y la centralización de la información de estudiantes y educadores, lo que genera ineficiencias administrativas y restringe la capacidad de toma de decisiones informadas.

### 2.3 Objetivos de negocio

| ID   | Descripción del objetivo de negocio |
|------|--------------------------------------|
| ON-1 | Implementar una plataforma web propia que centralice la gestión de estudiantes, educadores, programas formativos y reportes administrativos del Centro Cultural Lucy Tejada. |
| ON-2 | Automatizar los procesos de registro, matrícula, control de asistencia, evaluación cualitativa y generación de reportes, eliminando la dependencia de sistemas externos y registros manuales. |
| ON-3 | Proveer herramientas de análisis y visualización de datos (dashboards interactivos) que faciliten la toma de decisiones del personal administrativo en tiempo real. |
| ON-4 | Garantizar la seguridad, disponibilidad y escalabilidad del sistema conforme a normativas colombianas de protección de datos (Ley 1581 de 2012 y Decreto 1377 de 2013). |

---

## 3. Visión de la solución

### 3.1 Frase de visión

El sistema **CCLTPG** será una plataforma web integral para el Centro Cultural Lucy Tejada. Permitirá gestionar de forma centralizada y autónoma los procesos académicos y administrativos del centro, incluyendo registro de estudiantes, inscripción en programas formativos, control de asistencia, evaluación cualitativa del desempeño, generación automatizada de reportes y visualización de métricas mediante dashboards interactivos, accesible desde navegadores web y dispositivos móviles.

### 3.2 Características del sistema

| ID     | Descripción | Prioridad | Objetivo de negocio asociado |
|--------|-------------|-----------|-------------------------------|
| CAR-01 | El sistema debe permitir el registro y gestión de datos personales de estudiantes, incluyendo inscripción en programas formativos con validación de cupos. | Alta | ON-1, ON-2 |
| CAR-02 | El sistema debe permitir a los estudiantes autenticados consultar su matrícula, horarios, grupo, docente asignado, ubicación de salón y progreso académico. | Alta | ON-1, ON-2 |
| CAR-03 | El sistema debe permitir a los educadores gestionar la asistencia de sus grupos y registrar evaluaciones cualitativas por estudiante según indicadores del centro. | Alta | ON-2 |
| CAR-04 | El sistema debe generar reportes automáticos de asistencia, desempeño, matrícula y deserción, exportables en formatos Excel, PDF y CSV. | Alta | ON-2, ON-3 |
| CAR-05 | El sistema debe proveer dashboards interactivos con métricas de matrícula, asistencia, evaluación, programas, distribución geográfica y deserción. | Alta | ON-3 |
| CAR-06 | El sistema debe soportar mínimo 200 usuarios concurrentes sin degradación del rendimiento, con tiempos de respuesta inferiores a 4 segundos en operaciones críticas. | Alta | ON-4 |
| CAR-07 | El sistema debe implementar autenticación segura con MFA, control de acceso basado en roles (estudiante, educador, administrador) y cifrado SSL/TLS. | Alta | ON-4 |
| CAR-08 | El sistema debe garantizar disponibilidad del 99.9%, con plan de recuperación ante desastres (DRP), backups automáticos y tolerancia a fallos por módulo. | Alta | ON-4 |
| CAR-09 | El sistema debe enviar notificaciones automáticas a estudiantes sobre fechas importantes, cambios de horario y actualizaciones de progreso académico. | Media | ON-1, ON-2 |
| CAR-10 | El sistema debe permitir tres niveles de usuario: estudiante, educador y administrador, con permisos diferenciados por rol. | Alta | ON-1, ON-4 |
| CAR-11 | El sistema debe cumplir con estándares de accesibilidad WCAG 2.1 y diseño responsivo compatible con navegadores modernos y dispositivos móviles. | Media | ON-1 |
| CAR-12 | El sistema debe registrar trazabilidad de auditoría: inicios de sesión, creación y modificación de datos, con usuario, fecha y hora del evento. | Alta | ON-4 |

---

## 4. Alcance y limitaciones

### 4.1 Alcance

| Número de release | Tema principal | ID de Características a incluir |
|-------------------|----------------|----------------------------------|
| 1.0 | Funcionalidad base: autenticación, gestión de estudiantes, inscripción en programas, consulta académica y gestión de asistencia por educadores. | CAR-01, CAR-02, CAR-03, CAR-06, CAR-07, CAR-08, CAR-10, CAR-12 |
| 2.0 | Reportes automáticos, dashboards interactivos y notificaciones automáticas. | CAR-04, CAR-05, CAR-09 |
| 3.0 | Accesibilidad, optimización responsiva y compatibilidad extendida. | CAR-11 |

---

## 5. Contexto del sistema

### 5.1 Resumen de Involucrados

| Nombre | Descripción | Responsabilidades |
|--------|-------------|-------------------|
| Director del Centro Cultural Lucy Tejada | Director de operación | - Aprobar visión y alcance del proyecto<br>- Proporcionar acceso a procesos e instalaciones<br>- Aprobar entregas del proyecto |
| Representante del personal administrativo | Representante de usuarios administrativos | - Proporcionar y validar requerimientos administrativos<br>- Validar prototipos de dashboards y reportes<br>- Describir los flujos actuales de gestión |
| Representante de educadores | Representante de usuarios educadores | - Proporcionar requerimientos de gestión de asistencia y evaluación<br>- Validar flujos del módulo de educadores |
| Representante de estudiantes | Representante de usuarios finales | - Validar flujos de inscripción, consulta académica y notificaciones |
| Líder de proyecto | Coordinador técnico | - Coordinar el proyecto y representar al equipo de desarrollo |

### 5.2 Diagrama de contexto

El siguiente diagrama muestra el contexto del sistema, las entidades externas a éste y los flujos de información.

![Diagrama 1]("./media/images/diagrama1.png")

### 5.3 Entorno de operación

El sistema será accesible desde navegadores web. Se deberán soportar los siguientes:

- Google Chrome (última versión estable)
- Mozilla Firefox (última versión estable)
- Microsoft Edge (última versión estable)

Los dispositivos móviles y sistemas operativos siguientes deberán ser soportados:

- Android 14+
- Windows y Linux (escritorio mediante UI web)

El sistema se ejecutará sobre infraestructura con certificado SSL/TLS válido. Se deberá contar con un entorno de pre-producción (staging) que replique condiciones reales de producción para validación de cambios y nuevas funcionalidades antes de su despliegue.

---

## 6. Información adicional

Los criterios de aceptación del proyecto incluyen:

- Plataforma instalada y operativa en el entorno de producción del Centro Cultural Lucy Tejada
- Protocolo de pruebas de aceptación aprobado al 100%, incluyendo pruebas funcionales, de seguridad y de rendimiento
- Cumplimiento verificado con la Ley 1581 de 2012 y el Decreto 1377 de 2013 (protección de datos personales)
- Manual técnico, de administración y de usuario entregado para cada perfil de rol
- Código fuente entregado con documentación interna, bajo control de versiones (Git)
- Manuales de capacitación y sesiones de entrenamiento realizadas para personal administrativo, educadores y estudiantes
