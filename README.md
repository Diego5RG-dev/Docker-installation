# Docker-installation

**1.Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo**

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/primera.png)

La captura muestra la ejecución del comando docker pull alpine, lo cual tiene como propósito fundamental iniciar la descarga de la imagen base de Linux Alpine desde el Docker Hub o un registro configurado.

**2.Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre**

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/segunda.png)

Para este apartado utilice el comando docker create y le indique que lo hiciera con alpine, sin ponerle un nombre como resultado acabo poniendole al contenedor un nombre por defecto. Respondiendo a la siguiente
pregunta sobre si esta arrancado la respuesta es no, simplemente lo crea no lo arranca.

**3.Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?**

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/tercera.png)

Asi es como cree el contenedor con el nombre de dam_alp1 pero como podemos ver tiene un problema y es que al ser tan ligero y no tener instucciones se cierra automaticamente al iniciarse. Para solucionar esto 
lo que encontre, fue rehacer el contenedor con la coletilla final que se ve en el comando o en su defecto tambien podria haber utilizado el sleep infinity

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/tercera-2.png)

**4.Comprueba que ip tiene y si puedes hacer un ping a google.com**

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/cuarta.png)

Despues de hacer que nuestro contenedor no se cierre automaticamente lo unico que tenemos que hacer seria utilizar el docker exec el cual es un comando para utilizar algun otro comando

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/cuarta-2.png)

Y en este apartado podemos ver como el ping hacia google se realizo correctamente, llegando todos los paquetes.

**5.Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?**

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/quinta.png)

Habiendo creado el correspondiente contenedor ejecutamos el comando "ip a" para saber su direccion ip y mandamos 4 paquetes a nuestro equipo, viendo que estos al estar en la misma intranet se reciben correctamente.

**6.Sal del terminal, ¿que ocurrió con el contenedor?**

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/sexta.png)

Aqui vemos que a pesar de que cerrasemos el contenedor estos siguen abiertos y esto es por la coletilla de que siempre esten activos, asi que si no queremos perder recursos deberiamos cerrarlos cuando dejemos de utilizarlos

**7.¿Cuanta memoria en el disco duro ocupaste?** Y **8.¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.**

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/ultima.png)

Para acabar aqui junte estos dos apartados porque utilizando el mismo comando pueden comprobarse las dos preguntas que nos pide la tarea, el cual es 

    docker stats <nombre-o-id-del-contenedor>
