# CAF

!!REQUISITOS!! BLOQUE 1

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

!!!Analisis!!! BLOQUE 2
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
- mostar datos del cliente (nombre, apellido ,correo) (BAJA)
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


!!!!!Diseño!!!!!   BLOQUE 3
-https://www.figma.com/proto/dh1SWCegokJehFH3osoMEx/CAFF--Community-?node-id=2-8&p=f&t=2HMWgnJjmSJCJLOD-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=1%3A2
-Diagrama de flujo:


!!!!Implementacion!!!  BLOQUE 4

-Feature Registro de usuario
-codigo pseint
Descricion del codigo

1. Ingreso y Validación del Nombre
El algoritmo inicia solicitando al usuario que ingrese su nombre. Este paso se encuentra envuelto en una estructura de repetición que se ejecuta hasta que el dato ingresado sea válido. La validación consiste en verificar que el nombre no contenga números ni caracteres especiales como comas, guiones, signos de exclamación, entre otros. Si se detecta alguno de estos caracteres o si el campo está vacío, el sistema muestra un mensaje de error y solicita el nombre nuevamente.


2. Validación del Apellido
La siguiente etapa consiste en el ingreso del apellido, aplicando la misma lógica que con el nombre. El algoritmo revisa carácter por carácter para asegurarse de que no se hayan introducido números ni símbolos, y que el campo no esté vacío.

3. Validación de la Razón Social
El sistema solicita también una "razón social", que podría ser útil si el algoritmo se orienta a usuarios empresariales o comerciales. Se realiza exactamente la misma validación aplicada en nombre y apellido: sin números, sin símbolos, y no vacío.

4. Verificación del Correo Electrónico
Uno de los puntos más elaborados del algoritmo es la validación del correo electrónico. El sistema lee el correo ingresado y realiza varias comprobaciones:

Cuenta cuántas veces aparece el símbolo “@”.

Verifica que haya exactamente uno, ya que más de uno lo invalidaría como correo electrónico.

Asegura que el correo no esté vacío.

Analiza cada carácter para evitar símbolos no permitidos como ¿, =, :, ;, !, y que no haya letras mayúsculas.

Si alguna de estas validaciones falla, se muestra un mensaje de error y se solicita el correo de nuevo.

5. Registro y Confirmación de Contraseña
Posteriormente, el algoritmo pide que el usuario establezca una contraseña y luego la confirme. Esta verificación consiste en comparar los dos valores ingresados. Si no coinciden, se muestra un mensaje de error y se repite el proceso hasta que ambas contraseñas sean iguales. se garantiza la coincidencia.

6. Confirmación de Usuario
Finalmente, el sistema simula un "inicio de sesión" inmediato. Se solicita nuevamente el correo electrónico y la contraseña, y se compara con los datos previamente ingresados. Si ambos coinciden, el algoritmo despliega el mensaje “Bienvenido al sistema”, confirmando que el usuario ha sido registrado correctamente y ha iniciado sesión.

!!Testing!!  BLOQUE 4

-!!Casos de prueba 1!!
Registro de usuario exitoso:

Objetivo:
verificar que el usuario pueda registrarse correctamente con datos validos

Entradas:
Nombre: Jonathan
Apellido: Cardona
Razon social: Riwi
Correo: jon200@gmail.com

Pasos:
ingresar al formulario de registro
completar todos los campos obligatorios
Verificacion de correo electronico por medio de un codigo enviado a este
Posterior a la verificacion sera registrado correctamente

Resultado esperado
El sistema crea el usuario correctamente
se muestra un mensaje de exito o se redirige al login



-!!Casos de prueba 2!!!
Login fallido:

Objetivo:
validar que el sistema no permita el acceso con contraseña incorrecta y muestre un mensaje de error

Entradas:
correo: jon20@gmail.com
Contraseña: Contraseñaincorrecta

Pasos:
ir al formulario de login
ingresar el correo y contraseña

Resultado esperado
El sistema no permite el acceso
se muestra mensaje de error como "Contraseña incorrecta o correo incorrecto"


-!!Casos de prueba 3!!
Validacion de formato de correo electronico en registro

objetivo:
verificar que el campo de correo valide correctamente el formato

Entradas:
correo: jhon20@gmail.com

Pasos:
Abrir el formulario de registro
Ingresar un correo invalido

Resultado:
Se muestra un mensaje de error idicando que el correo no es valido
El registro no se completa


Posibles errores antisipados

-Verificar que los campos se llenen correctamente
-verificar el formato de correo electronico cumpla las condiciones "Debe tener caracter @"
-verificar que inicio de sesion valide el usuario y contraseña registrados "si las credenciales no son validas no habra inicio de sesion"




!!Despliegue mantenimiento!! BLOQUE 5

mantenimiento:
Actualizaciones de contenido: Asegúrese de que los co-working mantengan actualizados sus datos, fotos y tarifas para garantizar que la información que se muestra siempre esté al día.

Actualizaciones de seguridad: Implementar actualizaciones regulares de seguridad en todas las dependencias y realizar auditorías de seguridad.



Despliegue

-Se compra el hosting y el dominio de la pagina en hosting colombia
-Se compran los permisos para subir las apps (play store, AppStore)

Futuras mejoras

-Añadir pago por pse
-login con FaceId
    
