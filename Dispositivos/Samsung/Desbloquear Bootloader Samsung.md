# Desbloqueo de bootloader

Este es el metodo más general para los dispositivos Samsung según mi experiencia para la serie **A**, puede que algunos textos o pasos, botones sean diferentes pero hay que ser muy caido de la mata para no percatarse, leer muchachos. Saludos

- Entra a Ajustes > Acerca del teléfono > Información de software.  
- Toca varias veces el número de compilación (unas 7 veces).  
- Una vez activas las opciones de desarrollo, entra a ellas y activa Depuración ADB y Desbloqueo OEM.  
- Apaga el celular completamente.  
- Presionando Vol+ y Vol- a la vez y continuamente, conecta el cargador a la computadora.  
- Aparecerá una pantalla azul con textos en chino o en inglés. Normalmente es presionar prolongadamente Vol+ en esta pantalla azul y el celular pedirá confirmación (otra vez presionar Vol+ pero solo una vez). Recomiendo traducir lo que salga en pantalla para saber qué hacer exactamente.  
- Se formateará el celular y habría finalizado.

Tenga en cuenta que el bootloader puede no desbloquearse en ese momento. A veces tiene que esperar un momento e incluso 7 días para poder manipular el celular en el modo Download. Recuerde estar conectado a internet después del formateo al desbloquear el bootloader.

## Cosas que suceden a la hora de desbloquear el bootloader 
- Formateo completo (Haz copia de todo mano)
- Aviso de desbloqueo de bootloader al iniciar el celular (Esto es normal)
- Knox se rompe para siempre, después de eso pierdes esa integridad de Samsung (Pero no le di importancia)
- En el modo Download cambian varias cosas y también es importante saber qué sale en esta pantalla:  
  Lo normal es ver OEM LOCK: OFF, Secure Download: Enabled  
  Lo demás es información del teléfono: ID Product, Binary, Current Binary, etc.