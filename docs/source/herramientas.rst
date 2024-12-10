Heramientas utilizadas para el Procesamiento y Análisis de Imágenes MRI.
============

Todos los datos que se adquieren de los resonandores de resonancia magnética estan en formato DICOM. Estos datos son transmitidos por red o transportandos en un medio digital para tenerlos en un folder ```/misc/``` de Clusterio. Para que los datos sean procesados y analizados con las herramientas correspondientes, es necesario convertirlo a un formato especial llamado *nifti*. El convertirdor que se utiliza es ```dcm2niix```. A continuación se lista ls herramientas utilizadas para el procesamiento y analisis de la imagenes, esta herramientas dependen del estudio que se desea realizar a un grupo de imagenes.

FSL 
---

FMRIB Software Library es una colección de herramientas muy popular para el procesamiento de imágenes estructurales, funcionales y de difusión. Tmabién cuenta con funciones que incluyen el análisis estadístico de dichas imágenes. :doc:`FSL <./fsl>` es completamente open source y esta bastante bien documentado, en su wiki puedes encontrar toda la información necesaria para empezar a procesar tus imágenes.

MRtrix3
-------

Uno de los favoritos es :doc:`MRtrix3 <./mrtrix3>` que cuenta con una larga colección de herramientas para procesar, visualizar y analizar imágenes sensibles a difusión (DWI). Si bien esta muuuy enfocado a las DWI, muchas herramientas son útiles para manejar imagenes en general. Mrtrix esta tambíen super bien documentado, aquí puedes checar su wiki.

FreeSurfer
----------

Un clásico!, FreeSurfer es de los softwares más utilizados para analizar imágenes de humanos. Dentro de su libreria hay montones de funciones para procesar imágenes estructurales, funcionales y de difusión. Puedes realizar desde registros, hasta tractografía y mapeo funcional. Aquí te dejo su wiki para que lo cheques.

BIDS
----

El Brain Imaging Data Structure es una manera estandarizada de organizar y esrtucturar tus datos de neuroimagen. Es altamente recomendable esta practica, sobre todo ya que facilita el compartir los datos o incluso el análisis. En esta entrada viene información de como utilizar los contenedores en el cluster.

ImageJ
------

ImageJ/FIJI es un software para analizar, procesar, editar y visualizar imágenes de microscopia! Si estas haciendo histología como parte de tu proyecto, este es el software que necesitas. Tiene una cgran antidad de plugins y funciones que te van a permitir hacer una muchos tipos de procesos de manera efectiva. Si bien los comandos de cajon estan muy bien documentados, muchos de los plugins tienen una documentación medio irregular y toca aprender a pura prueba y error. Aquí te dejo el link de su pagina web.

dcm2niixx
---------

Convertidor de imagenes en formato DICOM a formato NIFTI

