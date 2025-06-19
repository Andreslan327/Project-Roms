# info\_extra.md

Este archivo es una extensión del repositorio principal **LanDroid**.

Aquí vas a encontrar información importante que **debes tener en cuenta antes de hacerte preguntas**, además de datos sobre tipos de dispositivos, problemas comunes al modificar, y otras cosas clave que no siempre se explican en los hilos o tutoriales.

---

## 📌 ¿Qué tipo de dispositivos son más fáciles de modificar?

* **Xiaomi/Redmi/Poco**: Generalmente fáciles, tienen buen soporte en foros. Solo es cuestión de desbloquear el bootloader y listo.
* **Samsung**: Algunos modelos son muy modificables, pero otros (como los de operadoras) vienen con bloqueos fuertes. Odin ayuda, pero no siempre hay ROMs o recoverys disponibles.
* **Motorola**: Se pueden modificar, pero hay menos comunidad activa últimamente. Depende del modelo.
* **Huawei/Honor**: En la mayoría de casos, casi imposibles. Bootloader bloqueado y sin forma oficial de abrirlo.
* **OPPO/Realme/Vivo**: Muchos modelos están muy limitados. Bootloaders cerrados, sin TWRP, sin root, poca documentación.

Para tener mucha más informacion sobre algunas marcas mira aquí:

*

---

## 🚫 Cosas que te pueden impedir modificar un celular

* Bootloader bloqueado sin forma de desbloquearlo
* Seguridad de arranque (AVB, dm-verity) sin métodos para desactivarla
* Particiones firmadas o protegidas (como en algunos Samsung o Huawei)
* Falta de soporte de la comunidad (sin TWRP, sin ROMs, sin root probado)
* Procesadores MediaTek (MTK) sin soporte, si no hay una herramienta confiable

---

## 🛠 Archivos que casi siempre necesitas para modificar

* `boot.img` limpio (de la ROM oficial) para parchear con Magisk
* `vbmeta.img` para desactivar verificaciones
* `recovery.img` para flashear TWRP o similar
* ROM original en caso de necesitar restaurar todo

---

## 🔗 Sobre los enlaces y archivos que se comparten

* Todos los enlaces que se comparten aquí vienen de XDA, NeedROM, páginas oficiales, o fuentes ya probadas
* Aun así, **debes verificar siempre que los archivos coincidan con tu modelo exacto** (código de región, chip, versión, etc.)
* Si algo sale mal por flashear un archivo que no es, no hay forma de recuperarlo desde aquí. Es tu responsabilidad.

---

## 📚 Recomendación general

Antes de modificar cualquier dispositivo:

1. Revisa si tiene soporte en foros (XDA, 4PDA, etc.) Yo estoy tratando de meter varios celulares aquí, y si no está aquí, busca en XDA, sino, no hay soporte seguro.
2. Verifica que se puede desbloquear el bootloader
3. Consigue todos los archivos primero y verifica su compatibilidad
4. Haz copia de seguridad de tu información
5. Lee experiencias de otros usuarios con el mismo modelo

---

Este archivo se irá actualizando con más detalles según lo necesite el proyecto.
