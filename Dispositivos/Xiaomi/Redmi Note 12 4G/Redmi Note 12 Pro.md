# Redmi Note 12 4G (Guía en general) Nota: Si solo quieres los archivos mira el [Solo archivos](https://github.com/Andreslan327/LanDroid/blob/main/Dispositivos/Xiaomi/Redmi Note 12 4G/Tapas/Solo%20archivos%20A235M.md)
<p align="center">
  <img src="https://fdn2.gsmarena.com/vv/pics/xiaomi/redmi-note-12-4g-1.jpg" alt="Xiaomi Redmi Note 12 4G" width="400"/>
</p>

## Detalles:
- **Lanzamiento 2023, 30 de marzo
- **Pantalla:** 6.67", 1080x2400  
- **Procesador:** Snapdragon 685 (2.8GHz)  
- **RAM:** 4GB / 6GB / 8GB  
- **Almacenamiento:** 64GB / 128GB / 256GB (expandible microSD)  
- **Cámaras:** 50MP + 8MP + 2MP
- **Batería: Li-Po 5000 mAh, no extraíble
- **Carga: 33 W por cable 
- **Sistema:** Android 13 (de salida)
- **3.5mm jack: Si
- **Sensores: Huella dactilar (lateral), acelerómetro, giroscopio, proximidad, brújula


## Tener en cuenta antes de hacer cualquier cosa
1. El celular tiene buen desarrollo de Roms y Ports
2. El root en este dispositivo es sencillo y tengo alguno que otro archivo útil para su uso.  
3. Es todo lo más importante que debes de saber ahora, continúa.

## Desbloqueo de bootloader
El teléfono en Miui es fácil de desbloquear pero desde HyperOS se ha complicado. Recuerde hacer copia de seguridad de sus datos y mantener su telefono conectado a datos moviles durante todo el proceso. Empecemos.

Método Mi Community (MIUI/HyperOS)
- Descarga la app de Xiaomi Community desde la Google Play Store.
- Crear una cuenta en dicha app (la cuenta debe de tener al menos 30 días de creada antes de aplicar para el desbloqueo).
-  Cambiar la región de la app a Global.
- Tocar el boton de Aplicar para desbloqueo de bootloader a las 00:00 hora Pekin, China.
- Si está en miui lo mas probable es que le acepten la solicitud y deba esperar algunos dias. Pero en HyperOS solo aceptan 2000 solicitudes diarias.
- si su solicitud no fue aceptada vuelva a intentar el siguiente dia. Buena Suerte

Metodo Mi unlock (Miui/HyperOS)
Este metodo podria funcionar en algunos casos

- instale en windows los respectivos drivers de xiaomi (en linux solo basta con instalar fastboot y adb en la terminal o tienda de software)
- Descargar el programa Mi unlock
- Abrir el programa y conectar su telefono con el modo depuración usb activado
- toque en unlock y si tuvo suerte se desbloqueará o se le avisará cuantos dias debe esperar de lo contrario solo queda intentar el metodo de arriba

Metodo Bypass (solo MIUI y HyperOS 1)

- Descargue el programa HyperSploit desde su github
- Abra el programa y conecte su telefono con el modo depuración usb activado
- Siga las instrucciones del programa y si todo salió bien. El programa el avisará cuantos dias debe esperae
- luego de pasados los dias siga los pasos del metodo Mi Unlock.

### Cosas que suceden a la hora de desbloquear el bootloader 
- Formateo completo (Haz copia de todo mano)

## Firmware oficial

En internet hay muchas páginas que ofrecen el firmware "oficial" de Xiaomi.. A continuación, dejo el enlace directo para el modelo de este teléfono, útil si quieres restaurar el sistema.
IMPORTANTE! ASEGURATE DE QUE EL FIRMWARE SEA EL DE TU MODELO Y REGIÓN.

- https://mifirm.net/model/tapas.ttt#global

Para Flashear el Firmware puedes hacerlo a través de el programa llamado Mi Flash o via adb sideload

También te recomiendo unirte al siguiente grupo de Telegram para información

**[RedmiNote12 4G Grupo Español](https://t.me/RedmiNote124GNFC)**,

---


## Custom Recovery

Lo primero a hacerse luego de desbloqueado el bootloader es instalar un custom Recocery. Empecemos.

1. Descarga un Custom Recovery para este dispositivo. Aquí te dejo el mas recomendado. De todos modos, haré un apartado de archivos necesarios y útiles para este celular en otro `.md`.
  -[OrangeFox](https://orangefox.download/device/65a5a3287ac2a93129dc9543)

   **Ninguno de estos archivos son míos. Créditos para sus respectivos dueños o modders.**

2. Ingresa al modo Fastboot (con el telefono apagado presiona Volumen Abajo + Botón de encendido)

3.  Para instalsr el custom recovery el metodo varia dependiendo del sistema operativo

a. Metodo Windows

1.  Descarga las herramientas llamadas Platform-Tools

2. Descarga la herramienta Mi Flash para los drivers correspondiente: https://xiaomiflashtool.com/download/xiaomi-flash-tool-20220507

3. Copia el archovo del recovery a la caroeta Platform-Tools

4. Abre el cmd en la caroeta Platform-Tools

5. Conecta tu telefono en modo Fastboot

6. escribe fastboot flash recovery recovery.img y presiona enter

7. Listo

b. Metodo Linux

1. Conecta tu telefono en modo fastboot

2. Abre la terminal de Linux en la carpeta donde tengas el recovery descargado

3.  escribe fastboot flash recovery recovery.img y presiona enter

4. Listo

ADVERTENCIA.

********NO uses el comando fastboot boot o brickearas tu dispositivo.********

## Root

A continuación, te explico los metodos para rootear tu Xiaomi Redmi Note 12 4G. Recuerda hacer esto **solo cuando el bootloader esté completamente desbloqueado y un custom recovery instalado**.

### Métodos:

Root con KernelSU usando un Kernel ya parcheado (Facil)

1. Ingresa al custom recovery (Volumen arriba + Botón de encendido con el telefono apagado)

2.  Una vez dentro del recovery, busca en el almacenamiento interno un kernel ya parcheado que hayas descargado (puedes encontrarlos en el grupo de telegram del redmi note 12 4G)

3. Instala el kernel

4. Reinica el telefono y descarga la app de kernelSU desde su github

5. listo

Root con KernelSU parcheando manualmente

1. Ingresa al custom recovery (Volumen arriba + Botón de encendido con el telefono apagado)

2. Haz un respaldo del init boot y boot 

3. Reinicia el telefono y descarga la app de kernelSU desde su github

4. Instalala y abrela

5. Dentro de la app toca donde dice instalar y la app te dirá si debes parchear Init boot o Boot

6. Busca en el almacenamiento dentro de la carpeta de tu recovery el respaldo del init boot y boot y seleccióna el archivo que la app te haya dicho.

7. Una vez parcheado apaga el telefono y entra al custom recovery

8. Busca el archivo llamado kernelsu patched dentro de la carpeta Download y seleccionalo

9. Instalalo en la partición Init boot o boot dependiendo de cual te haya dicho la app de kernelSU

10. Reinicia y ya deberias tener tu telefono con root

Metodos Magisk

Metodo 1 (Facil)

1. Descarga magisk o una variante como Delta, Alpha, procura que sea un archivo .zip (basta con buscar magisk (nombre de la variente + GitHub)

2. Reiniciar en recovery y flashear el .zip.

3. Iniciar el sistema, aquí puedes esperar a que se instale sola el .apk de cada magisk o hacerlo tu manualmente como si de instalar cualquier aplicación se tratara.

4. Iniciar magisk, en la mayoría de los casos te saldrá un cartel que indica que necesita una instalación adicional, sino aparece esta bien, si aparece solo dar clic en "aceptar" y posterior en la opción que dice " instalación directa, recomendado", el celular se reiniciara y magisk quedara instalado.

Metodo 2 Magisk parcheando boot:

1. Descargar el .apk de cualquier magisk 
2. clic en instalar y escoger "seleccionar y parchear archivo"
3. parchear la boot.img como en el método de KSU
4.  reiniciar en recovery y flashear en la partición boot, sino usas recovery, puedes usar fastboot flash boot.
5. iniciar el sistema y comprobar.


**Nota:** Ninguno de los archivos ofrecidos aquí son míos. Solo los he conservado de otras fuentes. Crédito respectivo para su creador o modder.

# Foro de XDA del dispositivo, por si tienes alguna inquietud: [A23 XDA](https://xdaforums.com/f/redmi-note-12-4g.12753/)

# Nuestro grupo de Telegram puede serte útil: **[Project Roms](https://t.me/projectroms)**