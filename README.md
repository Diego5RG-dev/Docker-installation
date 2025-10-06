## Docker-installation
---
1.Descarga la imagen "alpine" SIN ARRANCARLA y comprueba que está en tu equipo
---

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/primera.png)

La captura muestra la ejecución del comando `docker pull alpine`, lo cual tiene como propósito fundamental iniciar la descarga de la imagen base de Linux Alpine desde el Docker Hub o un registro configurado.

---
2.Crea un contenedor sin ponerle nombre. ¿está arrancado? Obtén el nombre
---
![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/segunda.png)

Para este apartado utilicé el comando docker create y le indiqué que lo hiciera con alpine. Sin ponerle un nombre, como resultado acabó poniéndole al contenedor un nombre por defecto.

Respondiendo a la siguiente pregunta sobre si está arrancado, la respuesta es no; simplemente lo crea, no lo arranca.

---
3.Crea un contenedor con el nombre 'dam_alp1'. ¿Como puedes acceder a él?
---
![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/tercera.png)

Así es como creé el contenedor con el nombre de dam_alp1, pero como podemos ver, tiene un problema y es que, al ser tan ligero y no tener instrucciones, se cierra automáticamente al iniciarse.

Para solucionar esto, lo que encontré fue rehacer el contenedor con la coletilla final que se ve en el comando, o en su defecto, también podría haber utilizado el `sleep infinity`.

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/tercera-2.png)

---
4.Comprueba que ip tiene y si puedes hacer un ping a google.com
---

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/cuarta.png)

Después de hacer que nuestro contenedor no se cierre automáticamente, lo único que tenemos que hacer sería utilizar el comando `docker exec`, el cual se usa para ejecutar algún otro comando dentro del contenedor.

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/cuarta-2.png)

Y en este apartado podemos ver cómo el `ping` hacia Google se realizó correctamente, llegando todos los paquetes.

---
5.Crea un contenedor con el nombre 'dam_alp2'. ¿Puedes hacer ping entre los contenedores?
---

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/quinta.png)

Habiendo creado el correspondiente contenedor, ejecutamos el comando `ip a` para saber su dirección IP y mandamos cuatro paquetes a nuestro equipo, viendo que estos, al estar en la misma intranet, se reciben correctamente.

---
6.Sal del terminal, ¿que ocurrió con el contenedor?
---

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/sexta.png)

Aquí vemos que a pesar de que cerrásemos el contenedor, estos siguen abiertos, y esto es por la coletilla de que siempre estén activos. Así que, si no queremos perder recursos, deberíamos cerrarlos cuando dejemos de utilizarlos.

---
7.¿Cuanta memoria en el disco duro ocupaste?** Y 8.¿Cuanta RAM ocupan los contenedores? ¿Hay algún comando docker para saber esto?.
---

![alt text](https://github.com/Diego5RG-dev/Docker-installation/blob/main/recursos-Docker/ultima.png)

Para acabar, aquí junté estos dos apartados porque, utilizando el mismo comando, pueden comprobarse las dos preguntas que nos pide la tarea, el cual es:

    docker stats <nombre-o-id-del-contenedor>
