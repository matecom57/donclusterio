FSL
---

FMRIB Software Library - FSL
FSL es una libreria open access de herramientas para el análisis de imagenes de resonancia magnética, desarrollada por investigadores de la Universidad de Oxford. Al día de hoy cuenta con una colección extensa para el análisis y procesamiento de imágenes estructurales, pesadas a difusión (DWI) y funcionales (fMRI). La librería FSL no le hace el feo a nadie y la puedes descargar en cualquier sistema operativo Linux, macOS o Windows (bueno, poquito a windows, hay que hacerlo mediante WSL). En este link te dicen como paso a paso.

Herramientas
En esta sección estan las herramientas más utilizadas de FSL y una breve introducción de qué hace.

Imágenes estructurales
  --------------------
  
fsl_anat : si lo que buscas es una manera directa de procesar tus imágenes T1w, esta es una opción. El pipeline tiene la ventaja de que envuelve todas las herramientas de abajo.

BET : esta herramienta elimina todo lo que no sea tejido de cerebro en la imágen, así como las superficies del cráneo.

FAST : realiza una segmentación de los diferentes tejidos del cerbero, ya sea sustancia gris, blanca, liquido cefaloraquídeo, etc.

FIRST : por otro lado, esta herramienta segmenta areas subcorticales.

FLIRT : es una herramienta robusta para registrar imágenes de manera lineal y no lineal con FNIRT.

Imágenes funcionales
--------------------
FEAT : herramienta bastante extensa y robusta para procesar y analizar datos funcionales.

MELODIC : sirve para realizar un análisis de componentes independientes.

  Imágenes difusión
  -----------------
  
  FDT : es una herramienta para el análisis de las DWI y lo puedes correr desde una interfaz gráfica o desde la terminal. Este pipeline incluye eddy, ajuste de tensores y tractografía.

TBSS : esta herramienta proyecta todos los mapas de FA de todos los sujetos de estudio (a partir de un registro no-lineal) en un "esqueleto" de FA promedio.

EDDY : forma parte fundamental del preprocesamiento, ya que corrige tanto el moviemiento del sujetoo como las distorsiones generadas por los cambios en los gradientes de difusion.

TOPUP : a la par de eddy, esta herramienta esta diseñada para corregir las distorsiones causadas por las inhomogeneidades del campo magnético. Por ejemplo, si adquirimos las imágenes en una dirección postero-anterior, la imágen resultante tendrá la distorsión notoria en la parte mas anterior (donde parece que la cabeza tiene un chipote gigante).

⭐ Recuerda que si eres miembro de la wiki y usas algunas de estas herramientas puedes colaborar generando nuevas entradas con tus mejores tips!

Manejo de versión de FSL
------------------------

Gracias a los módulos ya no tendrás conflicto entre versiones. Hasta el momento (Abril 2024) hay dos versiones en el Cluster:

```
module avail fsl
```
```
fsl/6.0.7.1
fsl/6.0.7.4
```

Lo unico que tienes que hacer es elegir la version con la que quieras trabajar y mandarla a llamar con module load. Como sugerencia, realiza tus análisis siempre con una misma versión.

Algunos tips del uso de FSL
---------------------------

Región de Interés: fslroi: Extrae una región de interés (ROI region of interest) de una imagen.

Mapas cuantitativos: fslstats: Extraer valores de un mapa cuantitativo.

Reorientar imágenes: Para visualizar las imágenes de forma habitual.

Quitar volúmenes de un archivo niffti

Transformar una máscara (espacio estándar-atlas) al espacio del sujeto (fMRI).

