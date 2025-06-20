# Redmi Note 12 4G (Guía general)

**Nota:** Si solo quieres los archivos, mira el apartado [Solo archivos](https://github.com/Andreslan327/LanDroid/blob/main/Dispositivos/Xiaomi/Redmi%20Note%2012%204G/Solo%20archivos%20Redmi%20Note%2012%20Pro.md)

<p align="center">
  <img src="https://fdn2.gsmarena.com/vv/pics/xiaomi/redmi-note-12-4g-1.jpg" alt="Xiaomi Redmi Note 12 4G" width="400"/>
</p>

## Detalles:

* **Lanzamiento:** 30 de marzo de 2023
* **Pantalla:** 6.67", 1080x2400
* **Procesador:** Snapdragon 685 (2.8GHz)
* **RAM:** 4GB / 6GB / 8GB
* **Almacenamiento:** 64GB / 128GB / 256GB (expandible por microSD)
* **Cámaras:** 50MP + 8MP + 2MP
* **Batería:** Li-Po 5000 mAh, no extraíble
* **Carga:** 33 W por cable
* **Sistema:** Android 13 (de salida)
* **3.5mm Jack:** Sí
* **Sensores:** Huella dactilar (lateral), acelerómetro, giroscopio, proximidad, brújula

## Tener en cuenta antes de hacer cualquier cosa

1. El celular tiene buen desarrollo de ROMs y ports.
2. El root en este dispositivo es sencillo, y tengo algunos archivos útiles para su uso.
3. Es todo lo más importante que debes saber por ahora, continúa.

## Desbloqueo de bootloader

El teléfono en MIUI es fácil de desbloquear, pero desde HyperOS se ha complicado. Recuerda hacer copia de seguridad de tus datos y mantener tu teléfono conectado a datos móviles durante todo el proceso. Empecemos:

### Método Mi Community (MIUI/HyperOS)

* Descarga la app Xiaomi Community desde Google Play Store.
* Crea una cuenta (la cuenta debe tener al menos 30 días de creada).
* Cambia la región de la app a "Global".
* Toca el botón de aplicar para el desbloqueo del bootloader a las 00:00 (hora Pekín, China).
* Si estás en MIUI, es probable que acepten la solicitud y te den una espera de algunos días. En HyperOS solo aceptan 2000 solicitudes por día.
* Si no fue aceptada, vuelve a intentar al siguiente día. Buena suerte.

### Método Mi Unlock (MIUI/HyperOS)

Este método podría funcionar en algunos casos:

* Instala los drivers de Xiaomi en Windows (en Linux basta con tener `adb` y `fastboot`).
* Descarga el programa Mi Unlock.
* Abre el programa y conecta tu teléfono con la depuración USB activada.
* Toca en "Unlock". Si tienes suerte, se desbloqueará, o te indicará cuántos días debes esperar.

### Método Bypass (solo MIUI y HyperOS 1)

* Descarga el programa HyperSploit desde su [GitHub](https://github.com/TheAirBlow/HyperSploit).
* Abre el programa y conecta tu teléfono con la depuración USB activada.
* Sigue las instrucciones. El programa te indicará cuántos días debes esperar.
* Luego sigue los pasos del método Mi Unlock.

**Cosas que suceden al desbloquear el bootloader:** Formateo completo. Haz copia de todo.

## Firmware oficial

En internet hay muchas páginas que ofrecen el firmware "oficial" de Xiaomi. A continuación, dejo el enlace directo para el modelo de este teléfono, útil si quieres restaurar el sistema.

**IMPORTANTE:** Asegúrate de que el firmware sea el de tu modelo y región.

* [MiFirm Redmi Note 12 4G](https://mifirm.net/model/tapas.ttt#global)

Para flashear el firmware debes de usar Mi Flash Tool

Te recomiendo unirte a este grupo:

* **[Redmi Note 12 4G Grupo Español](https://t.me/RedmiNote124GNFC)**

---

## Custom Recovery

Una vez desbloqueado el bootloader, instala un custom recovery. Empecemos:

1. Descarga un recovery compatible:

   * [OrangeFox](https://orangefox.download/device/65a5a3287ac2a93129dc9543)

   **Créditos para sus respectivos autores o modders.**

2. Entra en modo Fastboot (Volumen abajo + Power apagado).

### Instalación:

#### En Windows

1. Descarga Platform-Tools.
2. Instala los drivers desde [Mi Flash Tool](https://xiaomiflashtool.com/download/xiaomi-flash-tool-20220507).
3. Copia el recovery a la carpeta Platform-Tools.
4. Abre CMD en esa carpeta.
5. Conecta el teléfono en Fastboot.
6. Ejecuta: `fastboot flash recovery recovery.img`
7. Listo.

#### En Linux

1. Conecta el teléfono en Fastboot.
2. Abre la terminal donde esté el archivo del recovery.
3. Ejecuta: `fastboot flash recovery recovery.img`
4. Listo.

> **Advertencia:** NO uses `fastboot boot`, podrías brickear tu dispositivo.

## Root

Solo haz esto cuando el bootloader esté desbloqueado y tengas un recovery instalado.

### Root con KernelSU (Fácil)

1. Ingresa al custom recovery (Vol+ y Power apagado).
2. Instala un kernel ya parcheado (lo encuentras en el grupo de Telegram).
3. Reinicia e instala la app KernelSU desde su GitHub.
4. Listo.

### Root con KernelSU (Manual)

1. Ingresa al recovery.
2. Haz backup del `init_boot` y `boot`.
3. Reinicia e instala KernelSU.
4. Dentro de la app, toca en instalar. Te dirá qué partición necesitas.
5. Busca el archivo correspondiente.
6. Parchea y guarda.
7. Vuelve al recovery, flashea el archivo parcheado.
8. Reinicia. Root listo.

### Root con Magisk

#### Método 1 (Fácil)

1. Descarga Magisk o variante (.zip).
2. Reinicia al recovery y flashea.
3. Al iniciar, instala el APK si no se instala solo.
4. Abre Magisk, completa la instalación si lo pide. Reinicia. Listo.

#### Método 2 (Parcheando boot)

1. Descarga Magisk (APK).
2. Selecciona "parchear archivo" y elige el boot.img.
3. Parchea.
4. Flashea por recovery o por fastboot (`fastboot flash boot boot.img`).
5. Reinicia y verifica.

**Nota:** Ningún archivo ofrecido aquí es mío. Todos son de terceros. Crédito a sus autores.

---

## Recursos adicionales

**Esta guía fue posible gracias a @SerExis1 del Grupo de Telegram Proyect Roms, creditos y agradecimientos a él.**

### [Foro XDA Redmi Note 12 4G](https://xdaforums.com/f/redmi-note-12-4g.12753/)
### [Grupo de Telegram: Project Roms](https://t.me/projectroms)
