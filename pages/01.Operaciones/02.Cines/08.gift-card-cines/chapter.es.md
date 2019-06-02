---
title: 'Procedimiento Gift Card Cines'
media_order: 'TiServices_v1.7a-Manual_de_Usuario.pdf,TiServices_v1.7-Manual_de_Instalacion.pdf'
date: '02-06-2019 13:08'
taxonomy:
    category: docs
---

### Procedimiento Gift Card Cines
-------
Se adjunta extracto de email de Matias

Les paso los manuales del sistema de cobro de GC en el cine. 
El problema que tienen es que la caja por x causa deja de validar contra el servidor, esto hace que no te permita ingresar. 

:-------------:La base está en el **Sqlcluster2**
Usuario **tprusr** y **tpradmin123456**
La base es **TiServices**.
Como pueden ver en la tabla terminales hay una que se llama terminacines1 esa es la que esta puesta.
En ip guarda el de la PC que se dio de alta.
Para volver a asignarlo deben poner NULL ese campo, es decir set ip = NULL
De esta forma podrán ingresar de nuevo esa PC con el mismo número de terminal. 
Tienen una tabla que es de usuarios en donde sale el nivel y el pass de cada uno. 
**Miren las tablas pero no toquen nada.** :-------------:

--------

Se adjuntan manuales de instalacion(del sistema en si) y de Usuario del sistema web

[pdfjs=TiServices_v1.7a-Manual_de_Usuario.pdf]

----------

[pdfjs=TiServices_v1.7-Manual_de_Instalacion.pdf]

----------

>! Si encuentras algun error o procedimiento desactualizado, avisanos asi lo solucionamos.



