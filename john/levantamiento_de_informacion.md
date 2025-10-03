# Levantamiento de Información (Workshop)

## Objetivo
Definir los requerimientos funcionales mínimos y validar las necesidades reales de los usuarios para un MVP de recordatorios de medicación, priorizando simplicidad, utilidad y viabilidad técnica dentro de las restricciones de tiempo y equipo.

## Metodología
Sesión remota (audio) con enfoque de Design Thinking en fase de ideación, utilizando facilitación guiada (preguntas estructuradas).

## Participantes
- **Facilitación:** John Alejandro Gualteros García y Angela Michel Pinzón Oliveros (moderación, agenda, toma de notas).
- **Equipo técnico:** John Alejandro Gualteros García, Ángela Michel Pinzón Oliveros.

## Usuarios/Stakeholders considerados
- Pacientes/usuarios finales representativos (perfiles básicos de adherencia).

## Herramientas
- Llamada de audio
- Tablero colaborativo para notas y priorización

## Duración y dinámica
**20 minutos (remoto)** con la siguiente agenda:
1. Apertura y objetivo (2’).
2. Contexto (3’).
3. Ideación guiada / lluvia de ideas (8’).
4. Priorización rápida (4’).
5. Cierre con acuerdos, métricas y próximos pasos (3’).

## Técnicas aplicadas
- Brainstorming

## Hallazgos clave
- El olvido de tomas es el principal motivo de incumplimiento, especialmente en tratamientos prolongados.
- Se valora un historial/estado básico de envíos como confirmación del funcionamiento; no se requiere edición posterior para el MVP.
- La interfaz debe priorizar claridad, rapidez y baja fricción (responsiva, sin distracciones ni sobrecarga visual).

## Decisiones (alcance del MVP)
**Se incluye:**
- CRUD de recordatorios: crear, editar y eliminar con fecha y hor.
- Validaciones mínimas: no permitir fechas pasadas y obligatoriedad de campos esenciales.
- Interfaz web responsiva con navegación simple y lenguaje accesible.

**Se excluye (para fases futuras):**
- Envíos por SMS/WhatsApp.
- Integración con calendarios o sistemas médicos.
- Módulos para familiares/cuidadores y roles avanzados.
- Paneles administrativos complejos.
- Autenticación JWT y persistencia de datos avanzadas.

**Nota de consistencia:** Dado que se excluyen JWT y persistencia avanzada, el MVP opera con un enfoque mínimo de datos y autenticación simplificada. Si en fases posteriores se mantiene registro/login completo, se incorporará una persistencia formal y el esquema de autenticación correspondiente.

## Métricas de éxito
- Onboarding ≤ 3 minutos hasta crear el primer recordatorio.
- ≥ 90% de recordatorios disparan notificación en la hora programada.
- Tiempo de carga inicial ≤ 2 s en conexión estándar.
