# CAF

!!REQUISITOS!!

1.
Problematica que soluciona: problemas de necesidad de espacios laborales y/o conferencias (CAF)
Publico: indepente,pymes,empresas.

  2.
Epica:
gestion de cuenta de usuairio
gestion de reserva
Proceso de pago seguro

3.
Funcinalidades claves:
gestion de cuenta de usuairio: egistro de usuario login (ALTA)
gestion de reserva: detalles de la reserva (ALTA)
Proceso de pago seguror: confimacion de la reserva (ALTA)   

!!!Analisis!!!

1.
Registro de usuario y login

- crear formulario de registro con campos: nombre,apellido ,razon social ,correo,contraseña  (MEDIA)
- validad campos del formulario (formato de correo, contraseña segura) (BAJA)
- crear un formulario de inicio de sesion (login) (MEDIA)
- autenticacion del usuario (coreo y contraseña) (ALTA)
- mostrar mensaje de error si los datos son incorrectos (BAJA)
- implementar recuperacion de contraseña (MEDIA)
- redireccionar al usuario al dashboard o hombe despues del login (BAJA)

2.
Detalles de la reserva

- crear interfaz para mostrar resumen de la reserva(fecha,horarios,servicio reservado) (ALTA)
- mostar datos del cliente (nombre ,correo,telefono) (BAJA)
- mostrar precio total y desglose de costos (impuesto y descuentos) (MEDIA)
- permitir edicion o confirmacion de ciertos campos si aplica (BAJA)
- validar que todos los datos estén completos antes de continuar (BAJA)
- agregar opción para cancelar o modificar reserva si esta en borrador (ALTA)
- mostrar politica de cancelacion o termino de cancelaciones (BAJA)

3. 
Confirmacion de a reserva

-mostrar pantalla de "reserva confirmada" con resumen final  (BAJA)
-generar codigo o numero de reserva (MEDIA)
-enviar correo de informacion al usuario con los detalles (MADIA)
-registrar la reserva en base de datos(con estado: confirmada) (ALTA)
-activar notificaciones push o sms si estan disponibles (ALTA)
-opcion para descargar comprobante o agragar al calendario (MEDIA)
-registrar evento de reserva en el panel de administracion (si aplica) (ALTA)

!!!Restriciones tecnicas!!!

1. el sistema debe funcionar en todos los dispositivos
2. el equipo solo tiene conocimiento en figma y pseint

 !!!Restriciones de negocio!!!
 
1. el proyecto debe entregarse en menos de 24 horas
2. debe cumplirse ciertas normativas establecidas por el teamlider

    
