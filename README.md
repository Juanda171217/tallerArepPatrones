# TALLER DE TRABAJO INDIVIDUAL EN PATRONES ARQUITECTURALES

## Juan David Martinez


### Descripción

Este taller consiste en desplegar en AWS con la ayuda de EC2 una aplicación web que por medio de LogService que es un servicio REST recibe una cadena, la almacena en la base de datos y responde con las 10 ultimas cadenas almacenadas y la fecha en la que se almacenaron. Utilizando el framework Spark y desplegada en un contenedor Docker.


### Pre-requisitos

* Java
* Maven
* Docker
* AWS
  
### Funcionamiento

En primer lugar lo que se hizo fue crear 5 instancias de EC2, a 4 se le instalaron java y a 1 Mongo

Aca podemos ver las 5 instancias creadas:

[![awsIn.png](https://i.postimg.cc/TYhpVdKR/awsIn.png)](https://postimg.cc/1fhmPZ0T)

El proceso que se hizo para correr el programa en las distintas instancias fue, copiando la carpeta target comprimida donde se encontraban las clases dentro de nuestra maquina virtual en AWS, se hizo accediendo por el protocolo sftp y luego con el comando put para pasar dicho archivo

[![awsEX.png](https://i.postimg.cc/MH0HTHHw/awsEX.png)](https://postimg.cc/643tb9Cb)

Aca podemos ver cada instancia de EC2 corriendo, una con mongo, tres con el logservice y una con el round robin

[![awsMd.png](https://i.postimg.cc/nrqZkWfG/awsMd.png)](https://postimg.cc/n9V6V0zX)

[![aws3.png](https://i.postimg.cc/tgzxrrpy/aws3.png)](https://postimg.cc/67yqqf81)

[![aws2.png](https://i.postimg.cc/J0FJNGmk/aws2.png)](https://postimg.cc/q68z0BNJ)

[![aws3.png](https://i.postimg.cc/tgzxrrpy/aws3.png)](https://postimg.cc/67yqqf81)

[![aws3.png](https://i.postimg.cc/tgzxrrpy/aws3.png)](https://postimg.cc/67yqqf81)

Aca podemos ver el funcionamiento de la aplicacion

[![awsf.png](https://i.postimg.cc/9FNwK46R/awsf.png)](https://postimg.cc/Xpdvyv74)

