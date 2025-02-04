
# Ejercicio con Vagrant y VM con VirtualBox
#
#


## En el siguiente ejercicio vamos a crear una máquina virtual utilizando Vagrant. 


* Un vagrantfile
* El box de vagrant que vamos a utilizar, en caso de no haberlo realizado, en una carpeta de nuestro equipo ejecutamos la instrucci

![Screenshot_3](https://user-images.githubusercontent.com/96561825/172915951-8a0ee064-7ec2-4c64-8995-64fe7b36f68a.png)

#
#

# Instrucciones
#
#

## Ejercicio 1 - De forma individual ejecutamos los siguiente pasos:

***1)*** En una carpeta de nuestro equipo vamos a proceder a crear un archivo, el cual denominaremos vagrantfile (sin extensión)

#
***2)*** Dentro de ese Vagrantfile pegaremos este texto (recomendamos usar un editor de texto avanzado, por ejemplo Notepad++)

![Screenshot_2](https://user-images.githubusercontent.com/96561825/172915897-3d782871-1d9e-491e-b990-61b428b3c72e.png)


Allí observamos en la línea 8 que definimos “server” como nombre de nuestra VM.


#
***3)*** Una vez que tenemos nuestro Vagrantfile guardado, procedemos a iniciar la instanciación de la misma, con el comando


![Screenshot_5](https://user-images.githubusercontent.com/96561825/172916579-65ab2995-8b31-402c-80a5-c2647889fa81.png)



Es probable que un momento nos liste todos nuestros adaptadores de red , seleccionamos el correspondiente al de nuestra conectividad principal.
Pasados unos minutos, tendremos nuestra VM instanciada con Vagrant disponible, para verificarlo ejecutamos 

![Screenshot_6](https://user-images.githubusercontent.com/96561825/172916619-da137c01-ad86-4755-9e3b-c83d8142e36c.png)

y deberíamos obtener lo siguiente:

![Screenshot_7](https://user-images.githubusercontent.com/96561825/172916645-b3559617-a2bd-46e8-a067-506a02606022.png)


#
***4)*** Ahora nos vamos a conectar a la instancia, para ello , en la misma carpeta donde instanciamos la VM, ejecutamos la sentencia

![Screenshot_8](https://user-images.githubusercontent.com/96561825/172916680-6c07520f-c763-45fe-a6d4-97dee3ddbfb7.png)


Ello nos conectara a la instancia, por defecto y al no haber configurado usuarios, nos conectaremos con el usuario “vagrant”, pero podremos cambiar a root usando “su”; la contraseña por defecto para dicho usuario es “vagrant”

![Screenshot_9](https://user-images.githubusercontent.com/96561825/172916693-82729364-68be-4f9f-b033-16c1921c934e.png)

SECUENCIA DE CONEXIÓN A LA VM


#
***5)*** Una vez allí dentro,debemos obtener la ip de la VM, en este caso vamos a tener 3 adaptadores de red, nos interesa la número 3
#

***a)*** Una vez dentro de la VM, instalamos el paquete apache2, para ello usamos la instrucción “apt-get install apache2” como usuario root.
#

***b)*** Finalmente, realizamos la misma prueba que la clase anterior, accediendo desde un navegador web a la página por defecto del Apache2.

![Screenshot_10](https://user-images.githubusercontent.com/96561825/172916720-2904a925-ea9a-45bd-b898-57f55492b8e9.png)


#
#
#
## Ejercicio 2 - De forma individual ejecutamos los siguiente pasos:


Ya vimos como Vagrant nos redujo sustancialmente la instanciación de una VM, pero aún hubo pasos como la instalación de Apache2 que lo hicimos de manera personalizada, es por ello que en esta parte de la ejercitación nos abocaremos a modificar algunos aspectos del Vagrantfile que harán más autónoma la instalación de paquetes y el cambio de algunas configuraciones.

***1)*** En primer lugar, y como propósito de la prueba, vamos a destruir nuestra VM, con la siguiente sentencia:


![Screenshot_11](https://user-images.githubusercontent.com/96561825/172916768-bf40618e-a8d7-4b08-ae38-57ef1070e173.png)



De esta manera se forzará el cierre de la VM y la destrucción de la misma.



***2)*** Modificaremos nuestro Vagrantfile, en primer lugar agregaremos las instrucciones para instalar el apache2, insertamos lo siguiente a partir de la linea 12 (antes del penultimo end)

![Screenshot_12](https://user-images.githubusercontent.com/96561825/172916787-ee84943e-62af-4993-8a46-374327983e5b.png)

Luego validamos nuestro Vagrantfile y si esta todo OK, la iniciamos

![Screenshot_13](https://user-images.githubusercontent.com/96561825/172916825-9236e0fd-4e59-4e08-8021-330ea6c7ab5a.png)


Nos conectamos a nuestra VM y allí nuevamente consultamos por la IP con “ip address”, accedemos en nuestro navegador a dicha IP y veremos que ya se nos muestra por la pantalla de Apache2 por defecto, con lo cual las instrucciones que le agregamos al Vagrantfile se ejecutaron correctamente.


#
#
## Con toda la mesa de trabajo debatan sobre las siguientes preguntas y contestarlas en conjunto:

* Tanto para el ejercicio 1 como para el ejercicio 2, describan con tus palabras lo que acaban de hacer.
* Describan con sus palabras cuál es la utilidad que se imaginan implementando Vagrant como herramienta.
* Determinen, de manera aproximada, cuánto tiempo demoraron en instanciar una VM con VirtualBox y luego esa configuración similar con Vagrant.
* Modifiquen una vez más el Vagrantfile, creen un HTML en sus máquinas (de manera sencilla, sino pueden tomar el código completo de este HTML) , nombrarlo como index.html, guardarlo en la misma carpeta que el Vagrantfile y luego agregamos las siguientes líneas

![Screenshot_14](https://user-images.githubusercontent.com/96561825/172916848-6585dfca-2c96-497a-aac0-3cf48e872e41.png)


#
#

Ahora averiguar la IP de la VM, navegan y ¿qué ven como página de inicio?

#
#
#
#
#
Seguimos en el [Día 23](day23.md)
