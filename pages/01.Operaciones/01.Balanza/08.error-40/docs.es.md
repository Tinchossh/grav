---
title: 'Error 40'
media_order: 'i-Label.png,Scalenet.png'
date: '29-05-2019 15:24'
taxonomy:
    category:
        - docs
---


------------
En el caso de que una balanza presente este error se deberá:

#### Borrar la Ram
------------
* Apagar la Balanza con la tecla “1” apretada (si no se suelta la tecla la balanza no prendera). En el visor aparecerá el mensaje **PRUEBA**.
* Bajar 2 veces con la flecha hasta que se muestre el mensaje **borrado ram** se confirma con la tecla enter. Dentro de esta opción se deberá hacer tres cosas:
	* **Borra Sram** para borrar esto se deberá apretar dos veces la tecla cero , la que tiene escrito CERO no el numero. Luego bajar con la flecha a la opción siguiente.
	* **borra conf** también se borra con la tecla que dice CERO apretándola dos veces y  se baja con la flecha.
	* **borra dato prueba** se borra igual que los anteriores.
Este procedimiento borra todo lo que tiene en memoria al balanza por lo tanto hay que reconfigurarla.

#### Configuración del formato de etiquetas
------------

1. Ingresar en la balanza con 6000 + MODO y bajar con las flechas ,una vez hasta llegar a **formato de etiq** e ingresar con la tecla enter.
2. Configurar lo siguiente:

------------

 |  Papel corto | Papel largo  									 |
 | :------------ | :------------								 |
 |  Formato: 27 (etiqueta corta) | Formato: 25 (etiqueta larga)  |
 | Largo +  60   |  Largo =  146 								 |

[Ver Formatos de Etiquetas](http://localhost/grav/es/balanza/cambiar-formato)

* Ancho = 0 
* Sens etiq = 73
* Continuo = 0
* Comercio = 1
* Títulos = 1
* Sensor de desp = 1

#### Configuración de código de Barra.
------------
* Con 6000 + Modo bajamos 2 veces con la flecha ingresar en la opción **cód. Barra** y configuar los siguientes parametros: 

* Pref. Eam = 002
* Pref. 10 dig = 4949
* Tipo cód. Barra = 1
* Tipo UPC = 28
* cód. Fab = 5

#### Configurar Red
------------
Configuración/ Ethernet
* Gateway 172.17.12.1 (Depende de en que sucursal te encuentres)
* Mascara  255.255.255.0
* Configuración Gateway

#### Configuración de la Tecla X (por) en balanzas VECTRA
------------
1-	entrar con 9000 + Modo ingresar a la opción tecla dir y Entrar.
2-	Opción prefijar y presionar Entrar.
3-	Y presionar la siguientes teclas “4”, “Avanzar”, “0” y la tecla que deseo que sea la tecla de multiplicación. Por lo general elegimos la letra “L”, presionar MODO, MODO

Para enviar el formato de etiqueta a las balanzas luego de el borrado de la ram,

Se transmiten las 3 solapas
1. labels
2. logos
3. field titles

[I-Label](i-Label.png)

[Scalenet](Scalenet.png)



------------

>>>Si encuentras algun error o procedimiento desactualizado, avisanos asi lo solucionamos.