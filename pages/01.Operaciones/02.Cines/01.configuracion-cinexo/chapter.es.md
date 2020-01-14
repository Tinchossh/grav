---
title: 'Configuracion Cinexo'
media_order: '01.png,02.png,03.png,04.png,05.png,06.png,07.png,08.png,09.png,10.png,11.png,12.png,13.png,14.png,15.png,16.png,17.png,18.png,19.png,20.png,21.png,22.png,23.png,24.png'
taxonomy:
    category: docs
---

### Configuracion Cinexo
-------------


Para realizar la instalacion del sistema Cinexo se debe acceder a la carpeta ubicada en la siguiente ruta \\operaciones-rb\Cinexo

Instalar Java (Versión 1.8 para arriba, 32 o 64 bits según el sistema operativo que se esté usando)

Instalar Tray Server (Aplicación de Cinexo para manejo de impresora fiscal)

Instalar QZ Tray (Aplicación Open-Source para control de impresora térmica)

Al finalizar la instalación QZ Tray, tocar botón derecho en el icono verde que aparece al lado del reloj en la barra de tareas y marcar opción "Automatically Start" (Arranque automático)

Instalar Google Chrome

Instalar impresora térmica de entradas. En el caso de ser una Bematech MP4200-TH usar el instalador BemaSetup_MP4K_x64_v4.1.1.exe (64bits) o el LciSetup_LR3K_v4.1.1.exe (32bits)

![A](01.png)

![B](02.png)

![C](03.png)

![D](04.png)


En este paso hay que conectar la impresora térmica, encenderla y tocar “Aceptar”

![E](05.png)



El instalador de impresora completara los pasos y aparecerá una nueva impresora con el nombre “MP-4200 TH”. Probablemente por problemas de bloqueo de firewall de la red de Dinosaurio a los servidores de Microsoft, en este paso la impresora quede “instalando” y no se vea como impresora durante un largo rato (Se ve como “no especificado” dentro del panel de impresoras de Windows, ver paso 12 para llegar a ese panel) hay que esperar que figure correctamente como impresora.

Cambiar el nombre de la impresora térmica de entradas a "caja" y seleccionar driver a “Generic/Text Only” (Los pasos pueden variar según la versión de Windows 10)

*  Abrir panel de control clásico (Win+R, escribir control + enter)
*  En el buscador arriba a la derecha escribir “impresora”
*  Click en “Ver dispositivos e impresoras”
*  Hacer doble click en la impresora recién instalada

![F](06.png)

Cuando se abra la cola de impresión, tocar impresora -> propiedades

![G](07.png)
Cambiar nombre a “Caja”

![H](08.png)

Seleccionar driver “Generic/Text Only” en pestaña “opciones avanzadas”

![I](09.png)

Cerrar sesión dinoadmin e iniciar usuario nuevo con el que se va a facturar (Usuario no administrador)

Copiar el "Tray Server.lnk" (Acceso directo de Tray Server que se crea automáticamente en el escritorio tras instalación) a c$\Users\[USUARIO QUE SE VA A UTILIZAR PARA FACTURAR]\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\ para que se ejecute automáticamente en el arranque

Crear acceso directo en el escritorio a QZ TRay (c$\Program Files\QZ Tray\qz-tray.exe)

Configurar Google Chrome como navegador por defecto en Windows 10 (Puede abrirse aplicación y pedirá solo configurarse a sí mismo como navegador por defecto)

Crear acceso directo a cola de impresión de impresora térmica de entradas en escritorio

![J](10.png)

Detectar el número de puerto COM de impresora fiscal en administrador de dispositivos

![K](11.png)

Abrir preferencias de Tray Server y seleccionar modelo de impresora fiscal y puerto COM en el que se encuentra (Click derecho en icono al lado de reloj)

![L](12.png)

![M](13.png)

Crear accesos directos en escritorio para frontend y backend de sistema Candy y Boletería (Cambiar a IP de servidor local de su sucursal). URLS:

> Cambiar xx por el octeto de la sucursal

**Frontend Candy**
http://172.xx.2.80/5.0/Candy/front/candy 

**Backend Candy**

http://172.xx.2.80/5.0/Candy/back/candy

**Boleteria**

http://172.xx.2.80/5.0/Boleteria/admin/app/Login.php


Configurar Autogon con el usuario creado para las cajas
**Aplicacion** : Autologon.exe

![N](14.png)

Va a solicitar aceptar los términos y condiciones la primera vez que se ejecuta, dar permisos de administrador, click en “Agree” y completar los datos del usuario creado para caja (Usuario, nombre de dominio “DINOSAURIO” y clave.

Configurar barra de tareas para que siempre muestre todos los iconos

1. Botón derecho sobre el reloj de la barra de tareas - > Configuración de barra de tareas
2. Click en “Seleccionar los iconos que aparecerán en la barra de tareas”

![O](15.png)

3. Activar “Mostrar siempre todos los iconos en el área de notificación”

![P](16.png)

4. Cambiar plan de energía a “Alto Rendimiento” para evitar suspensión de dispositivos USB/PCI Express
	* Abrir panel de control (Win+R, escribir “control” + enter)
	* En el buscador de arriba a la derecha escribir “Energia”
	* Hacer click en la opción “Cambiar la configuración para ahorrar energía”

![Q](17.png)

	* Seleccionar plan “Alto Rendimiento”

![R](18.png)

	* Reiniciar. Si todo funciona correctamente, debe arrancar la computadora, iniciar sesión automáticamente, ejecutar Tray Server y QZ Tray, y quedar dichos iconos en verde en la barra de tareas.
	* Abrir acceso directo de Frontend de Candy en Chrome, y cuando QZ Tray muestre un cuadro de dialogo informando que “Cinexo Soluciones” pide acceso a la impresora, poner que sí y marcar la opción de recordar.


**Errores posibles:**

1. No aparece alguno de los dos iconos en la barra de tareas (Tray Server o QZ Tray). Verificar cual es el que falta y reinstalar inicio automático, en el caso de Tray Server copiando el acceso directo y en el caso de QZ Tray abriendo la aplicación y seleccionando con el botón derecho "Automatically Start"
2. Al ejecutar Tray Server da un error de .dll faltante al iniciar. Reinstalar Tray Server (InstaladorTS.exe), ya que le agrega unas .dll a la carpeta de Java y a veces falla en copiar los archivos.
3. Si no se ejecuta el .JAR de Tray Server al clickear el archivo .lnk (Acceso directo) creado en el escritorio o al querer abrir directamente la aplicación .JAR, ejecutar “Jarfix.exe” con permisos de administrador y queda funcionando.

**Habilitación conexión remota para personal de Cinexo:**
En el caso que el personal de Cinexo les solicite acceso remoto a la computadora, seguir los siguientes pasos para activar RDP:
1. Tocar botón de inicio de Windows
2. Tocar icono de engranaje que sale arriba del icono de encendido
3. Buscar “remoto” en el buscador central que aparece arriba del panel de configuración de Windows
4. Hacer click en configuración de escritorio remoto

![S](19.png)

5. Hacer click en “Habilitar Escritorio remoto”

![T](20.png)

6. Desplazarse con la barra lateral hacia abajo y hacer click en “Seleccione los usuarios que pueden tener acceso remoto a este equipo”

![U](21.png)

7. Click en “Agregar”

![V](22.png)

8. Escribir “soportecinexo” y tocar donde dice “Comprobar nombres” (Si pide usuario y clave para comprobar el nombre usar “oper.sistemas” y la clave correspondiente)

![W](23.png)

9. Debe quedar de la siguiente manera, si queda así, tocar aceptar.

![Y](24.png)

Una vez realizado queda concluido el procedimiento para instalacion de Cinexo. Se deberan probar ambas impresoras.




