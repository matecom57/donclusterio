WBienvenido a la documentación de Don Clusterio
===================================

**Don Clusterio** es una red de computadoras que trabajan conjuntamente de manera distribuida y paralela para procesar, analizar y sacar resultados de imagenes de resonancia magnetica estructural y funcional (MRI) principalmente. 

Clusterio optimiza, reduce el tiempo de procesamiento al analizar muchas imágenes. 

Esta red esta fomada de 32 equipos de computo cada uno con el Sistema Operativo UBUNTU-22. La contrucción de Don Clusterio esta implementada principalmente de los paquetes *NFS*, *NIS* y *SGE*. 

Este documento tiene por objetivo en explicar a los uusarios de Don Clusterio en como almacenar sus datos, utilizar heramientas (programas utilitarios) para manejar sus datos eficientemente, y hacer uso de los programas para procesaqar, analizar estadisticamente las imágenes y exportar sus resultados para ser utilizados en sus artículos, tesis o cualquier publicación que desen.

El Instituto cuenta con tres resonadores de resonancia magnética, dos para humanos y uno para animales pequeños. La MRI es una tecnología de imágenes no invasiva que produce imágenes anatómicas tridimensionales detalladas, sin el uso de la radiación dañina. 

Para que un usuario pueda utilizar los recursos y programs de Don Clusterio  es necesario tener dos cuentas, una en la Red Lanirem en el canal `#don_clusterio <https://chat-lanirem.lavis.unam.mx/channel/don_clusterio/>`_ y la otra en Don Clusterio, solicitada a su Jefe inmediato.

Otra documentación que seria ser útil es la de wiki del `Lanirem <https://github.com/lanirem/documentation/wiki/XCP-Preprocessing/>`_

.. note::

   Este proyecto está en desarrollo activo. Cualquier duda, comentario o desea participar en este desarrollo escribirle a ```matecom57@gmail.com```

Contenido
---------

.. toctree::
   :numbered:

   usage
   para_empezar
   bash
   api
