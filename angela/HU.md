# Historias de Usuario (HU)
 
## HU-01 – Registro de usuarios
**Dado** un usuario no registrado  
**Cuando** ingresa email válido y contraseña con requisitos mínimos y envía el formulario  
**Entonces** se crea la cuenta y se redirige a Login.
 
**Criterios de aceptación**
- Validar formato de email.
- Contraseña con longitud mínima ≥ 8 caracteres.
- Confirmación de contraseña debe coincidir (si aplica).
- Si el email ya existe, mostrar “email ya registrado” y no crear la cuenta.
 
---
 
## HU-02 – Inicio de sesión
**Dado** un usuario registrado  
**Cuando** ingresa email y contraseña correctos  
**Entonces** el sistema autentica y marca al usuario como “autenticado”.
 
**Criterios de aceptación**
- Si las credenciales son inválidas, mostrar error genérico sin revelar qué campo falló.
 
---
 
## HU-03 – Cierre de sesión
**Dado** un usuario autenticado  
**Cuando** selecciona “Cerrar sesión”  
**Entonces** el sistema invalida la sesión y muestra confirmación de cierre.
 
**Criterios de aceptación**
- Token/cookie invalidados para nuevas peticiones.
- Intentar acceder a rutas privadas tras el cierre redirige a Login.
 
---
 
## HU-04 – Crear recordatorio
**Dado** un usuario autenticado  
**Cuando** ingresa título/medicamento, fecha-hora válida (futura) y mensaje opcional  
**Entonces** se crea el recordatorio y se devuelve un ID.
 
**Criterios de aceptación**
- La fecha-hora debe ser futura (según zona horaria del usuario).
- Campos obligatorios: título (y/o medicamento) y fecha-hora.
- Al crear, la notificación queda programada según el canal definido.
 
---
 
## HU-05 – Editar recordatorio
**Dado** un usuario autenticado con un recordatorio propio  
**Cuando** envía cambios válidos (p. ej., nueva fecha-hora, título, mensaje)  
**Entonces** el recordatorio se actualiza y las notificaciones se reprograman.
 
**Criterios de aceptación**
- No permitir editar recordatorios de otros usuarios.
- Cambios inválidos (fecha pasada, campos obligatorios vacíos) rechazan la actualización con mensaje claro.
 
---
 
## HU-06 – Eliminar recordatorio
**Dado** un usuario autenticado con un recordatorio propio  
**Cuando** solicita eliminarlo  
**Entonces** el sistema lo elimina y muestra confirmación.
 
**Criterios de aceptación**
- No permitir eliminar recordatorios de otros usuarios.
- Las notificaciones pendientes asociadas se cancelan.
 
---
 
## HU-07 – Listar mis recordatorios
**Dado** un usuario autenticado  
**Cuando** navega a “Mis recordatorios”  
**Entonces** visualiza una lista de sus recordatorios.
 
**Criterios de aceptación**
- La lista muestra: título, fecha-hora, estado (pendiente, enviado, cumplido).
- Orden por fecha-hora ascendente por defecto.
- Filtros rápidos: “hoy” y “todos”.
- Paginación disponible para listas largas.