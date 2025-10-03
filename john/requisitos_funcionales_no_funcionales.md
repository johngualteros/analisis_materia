# Requisitos funcionales

| CÓDIGO  | Nombre                | Descripción                                                   | Prioridad | Actor   | Entradas                                            | Salidas                       |
|---------|------------------------|---------------------------------------------------------------|-----------|---------|-----------------------------------------------------|-------------------------------|
| RQF 001 | Registro de usuarios   | Permitir crear una cuenta con email y contraseña.             | Alta      | Usuario | Email, contraseña (nombre opcional)                 | Redirección a Login           |
| RQF 002 | Inicio de sesión       | Autenticar credenciales.                                      | Alta      | Usuario | Email, contraseña                                   | Estado autenticado            |
| RQF 003 | Cierre de sesión       | Finalizar la sesión del usuario.                              | Media     | Usuario | —                                                   | Confirmación de cierre        |
| RQF 004 | Crear recordatorio     | Permitir crear recordatorios con fecha y hora.                | Alta      | Usuario | Título/medicamento, fecha-hora, mensaje (opcional)  | Recordatorio creado (ID)      |
| RQF 005 | Editar recordatorio    | Modificar campos de un recordatorio existente del usuario.    | Media     | Usuario | ID de recordatorio; campos a actualizar             | Recordatorio actualizado      |
| RQF 006 | Eliminar recordatorio  | Eliminar un recordatorio del usuario.                         | Media     | Usuario | ID de recordatorio                                  | Confirmación de eliminación   |

---

# Requisitos no funcionales (por revisar)

| CÓDIGO    | Categoría               | Descripción                                                                 | Prioridad | Criterio de verificación / Métrica                                                                 | Método de prueba                      |
|-----------|-------------------------|-----------------------------------------------------------------------------|-----------|-----------------------------------------------------------------------------------------------------|---------------------------------------|
| RQNF 001  | Usabilidad/Responsividad| La interfaz será responsiva y de fácil navegación en desktop y móvil.       | Alta      | Sin desbordes ni scroll horizontal a ≥360 px; controles táctiles ≥44 px; navegación 100% con teclado | Inspección de UI + pruebas exploratorias |
