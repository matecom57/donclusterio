BASH y los Folder's de Trabajo
==============================

Todos los usarios tienen asignado un folder por defecto y es creado cuando se define el usuario.  El folder es identificado por la palabra HOME. En este folder se guardan archivos pequeños y tratar de no exceder su tanmaño de 30MBytes, ya que si se exede se crea un almacenamiento en cortocircuito en el disco donde se guardan todos los HOME's de los usuarios, lo cual genera problemas con Don Clusterio.

Ahora bien, para guardar datos imagen, es decir muchos volúmenes de imagen, estos de podran guardar en los folder's precedidos por el prefijo ```/misc```, es decir, si mi lugar de trabajo es donde se encuentra la maquina ```tournoux```, en esta maquina se tiene dos discos para guardar datos ```tournoux1```y ```tournoux2```. En alguno de  estos discos tendre un folder que me crearon para guardar mis datos imagen, entonces el path absoluto de mi folder para guardar los datos, seria:



```
santosg@penfield:$/misc/tournoux1/santosg/
```

donde **santosg** es el usuario que esta trabajando.

Otro folder de importancia cuando se esta trabajando en el procesamiento y analisis de datos es el folder:

```
/tmp
```

En folder es utilizado por los programas para el procesamiento y análisis de MRI, tambien para guardar archivos temporales. 

