BIDS
----
  
BIDS es un estándar de almacenamiento de datos, que mediante una jerarquía de carpetas y nomenclatura específica de archivos, permite la utilización transparente (y supuestamente sencilla) de complicados pipelines de procesamiento de imágenes reunidos en contenedores tipo Docker y/o Singularity que facilitan la reproducibilidad de los resultados. Puede usarse para analizar fMRI, DWI, e imágenes anatómicas.

No es la intención de esta página el repetir lo que ya está dicho de cómo se organizan los datos en BIDS, pues para ésto hay tutorales. Aquí están los tutoriales oficiales, pero una búsqueda en Google revelará muchos más.

Una vez que organices tus datos, revisa que hayas hecho un buen trabajo, validando tu fólder bids mediante el bids validator.

Listo para correr un contenedor? Tenemos instalado Singularity en el cluster del laboratorio! De igual forma, está instalado en el LAVIS!

Como ejemplo, veamos cómo correr fmriprep. Sigue esta liga para un corto tutorial.

PPMI
Para notas sobre cómo bajar datos de PPMI y convertirlos a BIDS, visita aquí.

Convertir tus imágenes pre-clínicas en formato BIDS
Para mayor control y estandarización en la organización de tus imágenes, se recomienda el uso de BIDS. Y también tiene la ventaja de que es muchísimo mas rápido convertir todas tus imágenes que están en el Bruker en formato nifti.

En este tutorial te digo como hacer la conversion utilizando las herramientas de BIDS converter ya englobadas en un script que hará todo el proceso de conversion por ti. Sin embargo hay solo un preparativo previo: tienes que pasar a un directorio todos las carpetas del bruker que desees convertir.

Accede a la ruta del bruker:

ls /misc/bruker7/data02/user/...
Una vez que identificas las imágenes de tu experimento, las moveremos a tu directorio de trabajo (/misc/../..):

cp -r /misc/bruker7/data02/user/mi_usuario/mis_imagenes* /mi/directorio/de/trabajo/

Usa las rutas de acuerdo a tu usuario y el directorio donde almacenas tu información.

Ahora si usaremos el script de abajo que ya engloba las dos funciones de bruker para realizar la conversion bids_helper que generará el archivo .csv de la descripción de tu dataset y bids_convert que hará toda la conversión.

Abre micro o nano en la terminal y haz copy & paste lo siguiente:

#!/bin/bash


module load brkraw/0.3.11


raw_dir=$1

mkdir ${raw_dir}/BIDS
bids_dir=${raw_dir}/BIDS
csv_filename=dataset_description

brkraw bids_helper $raw_dir ${raw_dir}/${csv_filename} -j 


brkraw bids_convert $raw_dir ${raw_dir}/${csv_filename}.csv -o $bids_dir
Ahora cierra el editor, nombra el script como bruker2bids.sh y luego escribe en la terminal: chmod a+x bruker2bids.sh

Listo, ahora usaremos el código de la siguiente manera:

bruker2bids /la/ruta/de/mis/imagenes/crudas/
Modifica la ruta del directorio por la ruta donde tienes guardadas las imágenes crudas que pasaste del bruker.

La organización quedará de la siguiente manera:

raw_dir
   \- bruker_raw_folder                               
   \- bruker_raw_folder
   \- bruker_raw_folder
   .
   .
   .
   .
   \- dataset_description.csv
   \- dataset_description.json
   \- BIDS
       \- README
       \- dataset_description.json
       \- participants.json
       \- participants.csv
       \- sub-001
            \-anat
                \- nii.gz
            \-dwi
                \- .bval
                \- .bvec
                \- nii.gz
            \-fmap
                \- nii.gz
            \-func
                \- nii.gz

       \- sub-002
            .
            .
            .
Pages 105
Tabla de contenidos

Home
Como colaborar en la Wiki
rocket.chat
Resonadores
Bruker
GE
Philips
Bash
Comandos Básicos
Avanzado
Clúster
Organización de datos
Respaldo de datos
Gestión de procesos
Módulos
Uso del clúster
Errores del clúster
Agilizando tu sesión
Procesamiento de Imágenes
Herramientas
FSL
MRtrix3
FreeSurfer
BIDS
Transformación de datos
fMRI
FEAT
fMRI en roedores
Conectividad Funcional Basada en Semilla
DW-MRI
Preprocesamiento humanos.
Preprocesamiento roedores.
Tractografía
Multi-tensor
Registro
FIJI - Análisis histológico
Tensor de Estructura
Herramientas Software
rclone
X2Go
SSH
Git
Anaconda
Otros
markdown
Clone this wiki locally
https://github.com/c13inb/c13inb.github.io.wiki.git
Footer
