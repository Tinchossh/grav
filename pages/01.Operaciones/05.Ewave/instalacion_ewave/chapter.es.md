---
title: 'Instalacion Ewave'
date: '02-06-2019 14:04'
taxonomy:
    category: docs
visible: true
---

### Instalacion Ewave
--------

Procedimiento para realizar la instalacion

* Entrar como administrador  (Dinoadmin)
* Ir a Ejecutar (Ctrl + R)
* \\\operaciones-rb\e$
* Buscamos la carpeta Ewave 3.0 Instalar
* Ewave SA
* Ejecutar el SuiteCinemaSetup.msi

------

* Luego ejecutar ewave_manager.exe
* Crear el servidor:
* Nombre cualquiera (srv-oper por ej.)
* Direccion del servidor 172.17.11.210
* Base de datos ewave
* Usuario: ewaveusr
* Contraseña: ewaveadmin123456

------------

* Copiar del registro hkey_local_machine/software/ewave/ (de una maquina que ya tenga instalado ej. operaciones-rb)
* El trialdays, installdate y el terminalId (puede ser cualquiera por ej. pv12)
* Se lo pega en un txt, y se abre desde la PC que se instalo recién ewave, se cambia el registro con el txt

---------

* Configurar el autologon de Windows en el regedit
* Probar de imprimir una entrada y reembolsarla, en la entrada impresa sale en nro de transacción para reembolsar

-----------

>! Si encuentras algun error o procedimiento desactualizado, avisanos asi lo solucionamos.
