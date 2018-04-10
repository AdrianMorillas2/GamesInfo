# GamesInfo :cat:
:blush::gun:

Indice
=================
- [Fase 1](#fase-1)
  * [Descripcion de la web](#descripcion-de-la-web)
  * [Entidades principales](#entidades-principales)
  * [Servicio Interno](#servicio-interno)
- [Fase 2](#fase-2)
  * [Diagrama de Navegacion](#diagrama-de-navegacion)
      - [Pantalla de inicio sin usuario](#pantalla-de-inicio-sin-usuario)
      - [Pantalla de inicio con usuario](#pantalla-de-inicio-con-usuario)
      - [Pantalla de Registro de Nuevo Usuario](#pantalla-de-registro-de-nuevo-usuario)
      - [Calendario de Eventos](#calendario-de-eventos)
      - [Evento](#evento)
      - [Lista de Juegos](#lista-de-juegos)
      - [Juego](#juego)
      - [Lista de Compa�ias](#lista-de-compa-ias)
      - [Compa�ia](#compa-ia)
      - [Perfil](#perfil)
      - [Perfil modificado](#perfil-modificado)
      - [Listas de Juegos](#listas-de-juegos)
      - [Nueva Lista de Juegos](#nueva-lista-de-juegos)
      - [A�adir Juego a una Lista](#a-adir-juego-a-una-lista)
      - [Articulo](#articulo)
    + [Pantalla de administrador](#pantalla-de-administrador)
  * [Diagrama de Entidad-Relacion](#diagrama-de-entidad-relacion)
  * [Diagrama UML de Entidades](#diagrama-uml-de-entidades)
  * [Diagrama de clases](#diagrama-de-clases)
- [Fase 3](#fase-3)
  * [Instrucciones para desplegar la aplicacion](#instrucciones-para-desplegar-la-aplicacion)
    + [1.- Inicializacion de Ubuntu](#1--inicializacion-de-ubuntu)
    + [2.- Elaboracion del jar](#2--elaboracion-del-jar)
    + [3.- Arranque de los jar](#3--arranque-de-los-jar)
    + [4.- Inicio de pagina web](#4--inicio-de-pagina-web)
  * [Servicio interno de correos](#servicio-interno-de-correos)
      - [Pantalla de relleno de datos](#pantalla-de-relleno-de-datos)
      - [Pantalla de recibo de correo](#pantalla-de-recibo-de-correo)
      - [Pantalla de usuario previamente registrado](#pantalla-de-usuario-previamente-registrado)
- [Fase 4](#fase-4)
  * [Instalacion de Vagrant](#instalacion-de-vagrant)
    + [1.- Instalacion de Ubuntu](#1--instalacion-de-ubuntu)
    + [2.- Configuracion del vagrantfile](#2--configuracion-del-vagrantfile)
    + [3.- Inicializacion](#3--inicializacion)
    + [4.- Division de Servicios](#4--division-de-servicios)
      - [4.1.- Maquina Virtual de Base de Datos](#41--maquina-virtual-de-base-de-datos)
      - [4.2.- Maquina Virtual de Servicio Interno](#42--maquina-virtual-de-servicio-interno)
      - [4.3.- Maquina Virtual de Servicio Web](#43--maquina-virtual-de-servicio-web)
  * [Instrucciones para la instalacion de HAProxy para Servicio Web](#instrucciones-para-la-instalacion-de-haproxy-para-servicio-web)
    + [1.- Instalacion PPA](#1--instalacion-ppa)
    + [2.- Actualizacion del sistema](#2--actualizacion-del-sistema)
    + [3.- Instalacion de HAProxy](#3--instalacion-de-haproxy)
    + [4.- Generacion de Certificado SSL](#4--generacion-de-certificado-ssl)
    + [5.- Configuracion de HAProxy](#5--configuracion-de-haproxy)
    + [6.- Inicio de HAProxy](#6--inicio-de-haproxy)
    + [7.- Inicio de HAProxy en Navegador Web](#7--inicio-de-haproxy-en-navegador-web)
  * [Instrucciones para la instalacion de HAProxy para Servicio Interno](#instrucciones-para-la-instalacion-de-haproxy-para-servicio-interno)
    + [1.- Instalacion PPA](#1--instalacion-ppa-1)
    + [2.- Actualizacion del sistema](#2--actualizacion-del-sistema-1)
    + [3.- Instalacion de HAProxy](#3--instalacion-de-haproxy-1)
    + [4.- Configuracion de HAProxy](#4--configuracion-de-haproxy)
    + [5.- Inicio de HAProxy](#5--inicio-de-haproxy)
    + [6.- Inicio de HAProxy en Navegador Web](#6--inicio-de-haproxy-en-navegador-web)
  * [Instrucciones para la instalacion de HAProxy para Bases de datos](#instrucciones-para-la-instalacion-de-haproxy-para-bases-de-datos)
    + [1.- Instalacion PPA](#1--instalacion-ppa-2)
    + [2.- Actualizacion del sistema](#2--actualizacion-del-sistema-2)
    + [3.- Instalacion de HAProxy](#3--instalacion-de-haproxy-2)
    + [4.- Configuracion de HAProxy](#4--configuracion-de-haproxy-1)
    + [5.- Configuracion de mysql](#5--configuracion-de-mysql)
    + [6.- Estructuracion de Servidores de Bases de Datos en Maestro-Esclavo](#6--estructuracion-de-servidores-de-bases-de-datos-en-maestro-esclavo)
      - [6.1.- Servidor Maestro](#61--servidor-maestro)
      - [6.2.- Servidor Esclavo](#62--servidor-esclavo)
    + [7.- Inicio de HAProxy](#7--inicio-de-haproxy)
    + [8.- Inicio de HAProxy en Navegador Web](#8--inicio-de-haproxy-en-navegador-web)
  * [Instalacion e Implementacion de Hazelcast](#instalacion-e-implementacion-de-hazelcast)
    + [1.- Instalacion de Hazelcast](#1--instalacion-de-hazelcast)
    + [2.- Implementacion de Hazelcast](#2--implementacion-de-hazelcast)
  * [Fichero Batch de Arranque](#fichero-batch-de-arranque)
  * [Diagrama de la Infraestructura desplegada](#diagrama-de-la-infraestructura-desplegada)
- [Fase 5](#fase-5)
  * [1.- Creacion de una Maquina Virtual Vagrant](#1--creacion-de-una-maquina-virtual-vagrant)
  * [2.- Configuracion de Ansible](#2--configuracion-de-ansible)
  * [3.- Creacion de la clave privada](#3--creacion-de-la-clave-privada)
  * [4.- Comprobacion de conexion](#4--comprobacion-de-conexion)
  * [5.- Demostracion del Correcto Funcionamiento](#5--demostracion-del-correcto-funcionamiento)
  * [6.- Creacion de Playbooks](#6--creacion-de-playbooks)
    + [6.1 Java](#61-java)
    + [6.2 MySQL](#62-mysql)
    + [6.3 HaProxy](#63-haproxy)
    + [6.4 Playbook](#64-playbook)
- [Integrantes](#integrantes)


# Fase 1 #
## Descripcion de la web ##
Este proyecto est� dirigido a usuarios aficionados a los videojuegos. Se trata de una web donde encontrar�s informaci�n relativa a cualquier juegos como puede ser su trama, la compa��a o la puntuaci�n que les ha otorgado los usuarios. Adem�s podr�s ojear los eventos de videojuegos que se celebrar�n pr�ximamente y hacerte tus propias listas en tu perfil con los juegos que te interesen.
- **Parte p�blica**: El usuario podr� navegar por las entidades de Juego, Compa��a, Evento o Art�culo.

- **Parte privada**: Para acceder a esta parte, primero se crear� una cuenta del que se recibir� una notificaci�n por el servicio de correo electr�nico para confirmar el registro. Una vez iniciada la sesi�n, el usuario tendr� dispopnible la parte privada para poder puntuar o comentar los juegos/compa��as/eventos/art�culo, as� como ojear o modificar sus listas de juegos. Tambi�n tendr� el usuario su perfil en el que podr� cambiar de correo electr�nico o contrase�a.
En cuanto al administrador, podr� crear fichas de juegos, compa��as, eventos o art�culos.

## Entidades principales ##
-   **Usuario**: Se distinguir� entre usuario registrado, no registrado y administrador. �ste portar� un Id, un Correo, un Nombre de usuario, una Contrase�a, una Fecha de Nacimiento, una Foto de perfil y su Rol. Cada usuario registrado tendr� sus propias listas de juegos.
-   **Juego**: Portar� un Id, Nombre, G�nero, Fecha de Salida, Descripci�n, Compa��a, Puntuaci�n, Imagen y Url de la web oficial. Tambi�n contendr� su correspondiente lista de comentarios.
-   **Compa��a**: Informaci�n de la compa��a encargada de desarrollar juegos, ya sea indie o empresa grande. Contiene Id, Pa�s, Fecha de Fundaci�n y Descripci�n. Tiene su propia lista de juegos y comentarios.
-   **Evento**: Contendr� un Id, Fecha, Lugar, Precio, Descripci�n y una Imagen. Puede contener comentarios realizados por los usuarios.
-   **Comentario**: Cada usuario podr� aportar su opini�n sobre cualquier juego, compa��a, evento o art�culo. �ste portar� un Id, Usuario y el propio Texto.
-   **Art�culo**: �ste portar� un Id, Usuario, T�tulo, Copete, Cuerpo e Imagen. Todos los usuarios registrados podr�n comentar en ellas, y los administradores podr�n crear art�culos.
-   **Lista**: Contiene una serie de juegos al gusto del usuario. �ste portar� un Id, Nombre y Lista de juegos.

## Servicio Interno ##
El servicio interno implementado consiste en que nuestra aplicaci�n web se comunique con nuestro servicio de correos interno mediante API REST. Su funci�n es simplemente enviar un correo de bienvenida y confirmaci�n a los nuevos usuarios registrados.

# Fase 2 #
## Diagrama de Navegacion ##
En el siguiente diagrama se puede visualizar la accesibilidad entre las distintas p�ginas:

![Diagrama de Navegacion](https://github.com/lalinlulelo/GamesInfo/blob/master/images/diagrama%20de%20flujos.png)

En esta fase no se ha diferenciado las partes privada y p�blica. Sin embargo, el funcionamiento de la parte privada, ser� la posibilidad de visualizar las listas propias, creadas por el usuario, as� como el acceso a su propio perfil para configurarlo o visualizar ciertos detalles de �l.

A continuaci�n se dispone de la captura de las distintas pantallas citadas en el diagrama:
#### Pantalla de inicio sin usuario ####
Pantalla principal donde se muestra por medio de un carousel imag�nes de los juegos m�s destacados de la actualidad. Debajo del carousel podremos visualizar los �ltimos art�culos escritos y los juegos m�s populares de la web. Y en el Navbar est�n las distintas p�ginas donde podemos navegar as� como los placeholders para hacer login y b�squeda.

![Inicio sin Usuario](https://github.com/lalinlulelo/GamesInfo/blob/master/images/home.jpg?raw=true)
![Inicio sin Usuario2](https://github.com/lalinlulelo/GamesInfo/blob/master/images/home2.jpg?raw=true)

#### Pantalla de inicio con usuario ####
En caso de que hayamos introducido correctamente los datos de un usuario existente entonces saldr� el nombre del usuario en el Navbar y podremos desplegarlo para acceder a mi perfil para modificar mis datos personales. Tambi�n podremos acceder a mi lista de juegos o hacer logout para cerrar sesi�n.

![Inicio con Usuario](https://github.com/lalinlulelo/GamesInfo/blob/master/images/home_loged.jpg?raw=true)

#### Pantalla de Registro de Nuevo Usuario ####
Si quisieramos crear un nuevo usuario simplemente tendr�amos que rellenar el formulario para registrar un nuevo usuario dentro de la base de datos.

![Nuevo Usuario](https://github.com/lalinlulelo/GamesInfo/blob/master/images/register.jpg?raw=true)

#### Calendario de Eventos ####
Para los eventos de videojuegos hemos implementado un calendario del que nos marcar� todos los eventos disponibles en la base de datos.

![Calendario Eventos](https://github.com/lalinlulelo/GamesInfo/blob/master/images/event_calendar.jpg?raw=true)

#### Evento ####
La ficha de evento donde contiene la informaci�n esencial de cada evento. En caso de que hayamos iniciado sesi�n tambi�n podremos comentar nuestra opini�n sobre dicho evento.

![Evento](https://github.com/lalinlulelo/GamesInfo/blob/master/images/event.jpg?raw=true)

#### Lista de Juegos ####
La lista de juegos muestra todos los juegos registrados y gracias al uso de las consultas en repositorio podremos ordenarlos de distintas maneras.

![Lista Juegos](https://github.com/lalinlulelo/GamesInfo/blob/master/images/games.jpg?raw=true)

#### Juego ####
La ficha de juego contiene la informaci�n esencial de cada juego. En caso de que hayamos iniciado sesi�n tambi�n podremos comentar nuestra opini�n sobre dicho juego o agregarlo a nuestra propia lista.

![Juego](https://github.com/lalinlulelo/GamesInfo/blob/master/images/game.jpg?raw=true)

#### Lista de Compa�ias ####
La lista de compa��as muestra todas las compa�ias que han desarollado los juegos expuestos en la p�gina, y gracias al uso de las consultas en repositorio podremos ordenarlos de distintas maneras.

![Lista Compa�ias](https://github.com/lalinlulelo/GamesInfo/blob/master/images/companies.jpg?raw=true)

#### Compa�ia ####
La ficha de compa��a contiene la informaci�n esencial de cada compa�ia. En caso de que hayamos iniciado sesi�n tambi�n podremos comentar nuestra opini�n sobre dicha compa��a.

![Compa�ia](https://github.com/lalinlulelo/GamesInfo/blob/master/images/company.jpg?raw=true)

#### Perfil ####
Aporta la informaci�n correspodiente al usuario, siendo su nickname, su contrase�a, su cumplea�os y su email. 

![Perfil](https://github.com/lalinlulelo/GamesInfo/blob/master/images/profile.jpg?raw=true)

#### Perfil modificado #####
La informaci�n del usuario puede ser modificada, pulsando el boton "change" correspondiente al atributo deseado, e insertando la nueva informaci�n.

![Perfil modificado](https://github.com/lalinlulelo/GamesInfo/blob/master/images/profile_modified.jpg?raw=true)

#### Listas de Juegos ####
Esta secci�n del usuario muestra las distintas listas de juegos que ha creado personalmente a su inter�s.

![Listas de Juegos](https://github.com/lalinlulelo/GamesInfo/blob/master/images/my_list.jpg?raw=true)

#### Nueva Lista de Juegos ####
Para poder crear una nueva colecci�n de juegos, ser� necesario crear una nueva lista, insert�ndole un nombre para identificarla.

![Nueva Lista de Juegos](https://github.com/lalinlulelo/GamesInfo/blob/master/images/my_list_modified.jpg?raw=true)

#### A�adir Juego a una Lista ####
Para a�adir un juego a una lista, el usuario registrado, deber� dirigirse al juego en s�, seleccionar la opci�n de a�adir a lista, y especificar en que lista guardar el juego.

![Juego en Lista](https://github.com/lalinlulelo/GamesInfo/blob/master/images/game_to_list.jpg?raw=true)

#### Articulo ####
Desde la p�gina principal se puede acceder a uno de los art�culos expuestos, ampliando la informaci�n de la noticia. Podr� comentar en caso de haber iniciado sesi�n.

![Articulo](https://github.com/lalinlulelo/GamesInfo/blob/master/images/article.jpg?raw=true)

### Pantalla de administrador ###
Si el administrador inicia sesi�n en su cuenta, en la secci�n desplegable de su usuario tiene la opci�n **Admin Features** donde se le dirige a la pantalla expuesta en la imagen. En esta p�gina mediante un formulario puede a�adir un juego, compa��a, evento, art�culo o eliminar un elemento del tipo de entidad expuesto ya existente.

![admin](https://github.com/lalinlulelo/GamesInfo/blob/master/images/admin.jpg?raw=true)

## Diagrama de Entidad-Relacion ##
En el siguiente diagrama se puede visualizar un modelo de datos donde se representan las entidades de un sistema de informaci�n as� como sus interrelaciones y propiedades.

![Diagrama de Entidad-Relacion](https://github.com/lalinlulelo/GamesInfo/blob/master/images/DiagramaER.png)

## Diagrama UML de Entidades ##
En el siguiente diagrama UML se puede visualizar los distintos atributos de las entidades y c�mo est�n relacionados entre s�.

![Diagrama UML de Entidades](https://github.com/lalinlulelo/GamesInfo/blob/master/images/DiagramaUML.png?raw=true)

## Diagrama de clases ##
Mediante ObjectAid UML Diagram,se ha adquirido un esquema inicial, que posteriormente ha sido simplificado y complementado con los templates. Su leyenda ser�a la siguiente:

![#8faadc](https://github.com/lalinlulelo/GamesInfo/blob/master/images/claseJava.png?raw=true) Clases Java:
* ____Controller: clase de tipo **@Controller**
* ____Configuration: clase de tipo **@Configuration**
* ____Repository: clase de tipo **@Repository**
* UserRepositoryAuthenticationProvider: clase de tipo **@Component**
* Event, Company, Article, Comment, User, MyList & Comment: clase de tipo **@Entity**

![#f4b183](https://github.com/lalinlulelo/GamesInfo/blob/master/images/claseHTML.png?raw=true) Clases HTML
![Diagrama de Clases](https://github.com/lalinlulelo/GamesInfo/blob/master/images/Diagrama%20de%20clases.png?raw=true)

# Fase 3 #

## Instrucciones para desplegar la aplicacion ##
Para poder desplegar la aplicaci�n, es necesaria la instalaci�n previa de una m�quina virtual VMWare con el Sistema Operativo **Ubuntu 14.04**
<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/ubuntu.jpg?raw=true">
</p>

### 1.- Inicializacion de Ubuntu ###
Tras su instalaci�n, se le ha de a�adir mediante consola
* Java 

  * `sudo apt-get update`
  * `sudo apt-get install default-jre`
  * `sudo apt-get install default-jdk`
  
* mySQL

  * `sudo apt-get update`
  * `sudo apt-get install mysql-server mysql-client`
  * como contrase�a se le colocar�: `gugus`
  * `sudo mysql_secure_installation`
  * Tras su correcta instalaci�n, se instalar� mySQL Workbench
  * `sudo apt-get install mysql-workbench`
  
* Base de Datos

  * se inicia mySQLWorkbench y se crea una nueva conexi�n con nombre 'gamesinfo_db'
  
  ![mySQLWorkbench_new_conection](https://snag.gy/P7FuKm.jpg)
  
   <p align="center">
    <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/bd.jpg?raw=true">
  </p>
  
  * se crea un nuevo schema con nombre 'gamesinfo_db' aplicando los cambios
  
  ![mySQLWorkbench_new_schema](https://github.com/lalinlulelo/GamesInfo/blob/master/images/new_schema.jpg?raw=true)
  
  ![mySQLWorkbench_schema name](https://github.com/lalinlulelo/GamesInfo/blob/master/images/schema_name.jpg?raw=true)
  
### 2.- Elaboracion del jar ###

Para crear los ficheros jar, se ha de iniciar Spring Tool Suite abriendo los proyectos determinados. En �l, nos dirigimos en cada proyecto a `Run As > Maven built...` apareciendo la siguiente ventana:

 <p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/maven_built.jpg?raw=true">
</p>

En dicha ventana, en la seccion **Goals** se ha escribir: `clear package` y acto seguido, pulsar en run. Tras la notificaci�n por consola, de la correcta compilaci�n y construcci�n del 'jar', se puede recoger dentro de la carpeta **target** (situada en la propia carpeta del proyecto):

 <p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/target.jpg?raw=true">
</p>

### 3.- Arranque de los jar ###

Los ficheros jar se pasan a la m�quina virtual, mediante un dispositivo de almacenamiento USB, especificando a la m�quina virtual (tras introducir los ficheros en el dispositivo) la detecci�n del dispositivo en el entorno: `VM > Removable Devices > USB > Connect (Disconnect from Host)`.

Acto seguido, v�a terminales, se arrancan el servicio de mensajer�a y la propia aplicaci�n mediante el comando `java -jar fichero.jar`:

 ![Arranque de Jars](https://github.com/lalinlulelo/GamesInfo/blob/master/images/arrancar_jar.jpg?raw=true)
 
Tras comprobar el correcto inicio de ambas aplicaciones, nos dirigimos al icono de internet de la barra de tareas, y mediante click derecho a �l, seleccionamos `Connection Information`, apareciendo la siguiente ventana:

 <p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/connection%20info.jpg?raw=true">
</p>

### 4.- Inicio de pagina web ###

Finalmente nos dirigimos a un navegador web (fuera de la m�quina virtual) e insertamos la **direcci�n IPv4** de la m�quina virtual seguido del puerto de conexi�n. En nuestro caso: `https://192.168.42.131:8443/`

![Pagina Final](https://github.com/lalinlulelo/GamesInfo/blob/master/images/https%20page.jpg?raw=true)

## Servicio interno de correos ##
En esta secci�n inicializamos tanto el MailService como la propia aplicaci�n web siguiendo los pasos indicados en el apartado anterior. Tras arrancar la p�gina web en el navegador, si uno se dirige a Register nos llevar� al html new_user y rellenamos los datos.

#### Pantalla de relleno de datos ####
Se rellenan los datos del usuario que se desea registrar, empleando en este caso un correo electr�nico generado por Fake Mail Generator para realizar la demostraci�n.

![Rellenar datos](https://github.com/lalinlulelo/GamesInfo/blob/master/images/register_fill.JPG?raw=true)

#### Pantalla de recibo de correo ####
Tras el correcto registro, se puede observar, que efectivamente se ha creado el usuario y adem�s se ha recibido un correo.

![Recibo correos](https://github.com/lalinlulelo/GamesInfo/blob/master/images/mail_confirm.JPG?raw=true)

#### Pantalla de usuario previamente registrado ####
En caso de que el nombre de usuario o el correo ya existan previamente, te redirigir� de nuevo a la p�gina de nuevo usuario sin completar el registro previo.

![registro previo](https://github.com/lalinlulelo/GamesInfo/blob/master/images/already_exist.JPG?raw=true)

# Fase 4 #

## Instalacion de Vagrant ##
Para poder duplicar y separar los distintos servicios de la aplicaci�n web (servicio web, servicio interno y bases de datos), fue necesaria la instalaci�n de Vagrant. Para ello fue necesaria la descarga de [Vagrant](https://www.vagrantup.com/downloads.html), as� como la descarga e instalaci�n de [Virtual Box](https://www.virtualbox.org/wiki/Downloads), todo ello en el Sistema Operativo Host. Tras la ejecuci�n del ejecutable .msi de la propia p�gina de vagrant, se han de realizar los siguientes pasos:

### 1.- Instalacion de Ubuntu ###
Lo primero a realizar ser� crear una carpeta con nombre `vagrant` en un directorio escogido (en nuestro caso Documents), donde m�s adelante se crear� el vagrant file. A continuaci�n, nos ponemos a instalar Ubuntu 14.04, para ello ejecutamos el siguiente comando desde una ventana de comandos (`Ejecutar > cmd`):

* `vagrant box add ubuntu/trusty64`

Tras la correcta instalaci�n se ejecuta el siguiente comando:

* `vagrant init ubuntu/trusty64`

Y finalmente, tras completar la iniciaci�n, se realiza:

* `vagrant up`

Creando el vagrantfile, siendo notificado por consola.

### 2.- Configuracion del vagrantfile ###
Para declarar una IP privada, es necesario descomentar la l�nea del fichero vagrantfile, para ello nos dirigimos a la carpeta `vagrant` anteriormente creada y abrimos el fichero con un editor de texto como `notepad++`:

* `# config.vm.network "private_network", ip: "192.168.33.10�`

Tras guardar el fichero, se puede comprobar su correcto funcionamiento mediante el comando:

* `ping 192.168.33.10`

### 3.- Inicializacion ###
A continuaci�n, nos dispondremos a configurar el Sistema Operativo creado para tener los programas necesarios para la correcta ejecuci�n de los servicios:
* Arrancamos el sistema operativo mediante el siguiente comando

 * `vagrant ssh`

* Java 

  * `sudo apt-get update`
  * `sudo apt-get install default-jre`  
  * `sudo apt-get install default-jdk`
  
* mySQL

  * `sudo apt-get update`
  * `sudo apt-get install mysql-server mysql-client`
  * como contrase�a se le colocar�: `gugus`
  * `sudo mysql_secure_installation`
  * Tras su correcta instalaci�n, se instalar� mySQL Workbench
  * `sudo apt-get install mysql-workbench`
  
### 4.- Division de Servicios ###
Para poder realizar la divisi�n de servicios en distintas m�quinas virtuales, es necesario repetir el anterior proceso **ocho** veces, teniendo una m�quina para cada servicio, y en el fichero `vagrantfile` declarando distintas direcciones IP, en nuestro caso se han declarado las siguientes direcciones:

* Servicio Web 1: `192.168.33.10`

* Servicio Interno 1: `192.168.33.11`

* Base de Datos 1: `192.168.33.12`

* Servicio Web 2: `192.168.33.13`

* Servicio Interno 2: `192.168.33.14`

* Base de Datos 2: `192.168.33.15`

* Balanceador Servidor Web: `192.168.33.16`

* Balanceador Servicio Interno: `192.168.33.17`

* Balanceador Servicio Base de Datos: `192.168.33.18`

Una vez creadas las nueve m�quinas virtuales, es necesario configurar ciertas funcionalidades en las distintas m�quinas virtuales.

#### 4.1.- Maquina Virtual de Base de Datos ####
Debido a que se ha separado la base de datos de la aplicaci�n web, se ha de configurarla para que sea accesible mediante su direcci�n IP privada, y permitiendo al servicio web acceder a ella. Para ello accedemos inicialmente al archivo `my.cnf` localizado en `/vagrant/etc/mysql/`permitiendo cualquier tipo de modificaci�n en el fichero:

* `sudo chmod +rwx my.cnf`

Y accediendo mediante el editor:

* `sudo nano my.cnf`

Cambiamos la l�nea `bind address` por la IP privada de la propia m�quina virtual, en nuestro caso `192.168.33.12`, quedando como en la siguiente imagen:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/vagrant%20my_cnf.jpg?raw=true">
</p>

Tras su correcto guardado mediante `Ctrl + X` y asegurando el guardado y sobreescribiedolo, reiniciamos el servicio mediante:

* `sudo service mysql service`

Una vez el servicio se ha reiniciado, accedemos a la consola de **mysql** mediante el siguiente comando:

* mysql -u root -p

Y una vez tenemos como path `mysql>` se dispone a crear el usuario, recomendamos que sea el mismo que se tiene declarado en el fichero properties del proyecto del servicio web, en nuestro caso `root`con contrase�a `gugus`:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/vagrant%20mysql%20properties.jpg?raw=true">
</p>

Para ello colocamos en la consola el siguiente comando:

* `create user usuario@direccion_ip_privada_maquina_servicio_web identified by 'contrase�a'`

En nuestro caso el comando ser�a el siguiente:

* `create user root@192.168.33.10 identified by 'gugus';`

Tras ello, se crea la base de datos (con el mismo nombre que la primera vez que se hizo) con el comando:

* `create database gamesinfo_db;`

Se le aporta todos los permisos posibles al servicio web, sobre dicha base de datos con los comandos:

* `grant all privileges on gamesinfo_db.* to root@192.168.33.10;`
* `flush privileges;`

Y por si se desea comprobar la correcta creaci�n del usuario, se puede ejecutar el siguiente comando:

* `select user, host, password from mysql.user;`

Saliendo la siguiente informaci�n por consola:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/vagrant%20mysql%20create%20user.jpg?raw=true">
</p>

Finalmente salimos de la consola de mysql con el siguiente comando:

* `exit`

#### 4.2.- Maquina Virtual de Servicio Interno ####
A diferencia de la m�quina de bases de datos, aqu� simplemente se tiene que realizar el archivo jar para ello se pueden seguir los pasos indicados en el punto 2 de la Fase 3: [Elaboracion del jar](#2--elaboracion-del-jar).

Una vez creado el fichero `.jar` se copia y se pega en el mismo directorio en el que se encuentra el archivo 'vagrantfile' de esta m�quina virtual, y se procede a su ejecuci�n. Para ello nos dirigimos al directorio principal mediante el comando:

* `cd /vagrant`

Y en el ejecutamos el .jar con el comando:

* `java -jar mailService-0.0.1-SNAPSHOT.jar`

#### 4.3.- Maquina Virtual de Servicio Web ####
Lo primero que debemos realizar puesto que la base de datos se encuentra en una m�quina virtual distinta a la del servicio web, es cambiar en el fichero properties del proyecto, la l�nea:

* `spring.jpa.hibernate.ddl-auto=update`

A `none`:

* `spring.jpa.hibernate.ddl-auto=none`

Y construir como en el anterior apartado el debido fichero .jar. Tras su construcci�n se copia y pega en el mismo directorio que el archvo `vagrantfile` de esta m�quina virtual y se procede a su ejecuci�n con el siguiente comando donde se detallan ciertas propiedades de la aplicaci�n (recordemos que el usuario declarado en la base de datos fue `root` y su contrase�a `gugus`, que la direcci�n IP de la m�quina virtual de la base de datos fue `192.168.33.12`y que la base de datos creada se llama `gamesinfo_db`):

* `java -jar prueba_servidor-0.0.1-SNAPSHOT.jar --spring.datasource.url="jdbc:mysql://192.168.33.12:3306/gamesinfo_db?verifyServerCertificate=false&useSSL=true" --spring.datasource.username="root" --spring.datasource.password="gugus" --spring.jpa.hibernate.ddl-auto="update"`

## Instrucciones para la instalacion de HAProxy para Servicio Web ##

### 1.- Instalacion PPA ###
Debido a que Ubuntu 14.04 no soporta la versi�n estable de HAProxy (v 1.5), se emplea una PPA (Personal Package Archives) para poder realizar la instalaci�n con `apt-get`:

* `add-apt-repository ppa:vbernat/haproxy-1.5`

### 2.- Actualizacion del sistema ###
El siguiente paso es actualizar el sistema:

* `apt-get update`
* `apt-get dist-upgrade`

### 3.- Instalacion de HAProxy ###
Tras la correcta actualizaci�n, se instala HAProxy:

* `apt-get install haproxy`

### 4.- Generacion de Certificado SSL ###
Debido a que nuestros servidores web emplean certificado y por tanto protocolo https, es necesario generar un certificado para que haproxy permita la redirecci�n a dichos servidores. Para ello lo primero que se har� es crear un directorio donde guardar las claves y certificados:

* `sudo mkdir /etc/ssl/xip.io`

A continuaci�n nos dirigimos a dicho directorio creado para ello realizamos esta serie de comandos:

* `cd`
* `cd /vagrant`
* `cd /etc`
* `cd ssl`
* `cd xip.io`

Y creamos el fichero que contiene la clave privada:

* `sudo openssl genrsa -out xip.io.key 1024`

Tras su creaci�n, se crea el primer certificado con el siguiente comando:

* `sudo openssl req -new -key xip.io.key \-out xip.io.csr`

El cual nos mostrar� un formulario que se completar� como se ve a continuaci�n:
<br>
`> Country Name (2 letter code) [AU]:US`<br>
`> State or Province Name (full name) [Some-State]:Connecticut`<br>
`> Locality Name (eg, city) []:New Haven`<br>
`> Organization Name (eg, company) [Internet Widgits Pty Ltd]:SFH`<br>
`> Organizational Unit Name (eg, section) []:`<br>
`> Common Name (e.g. server FQDN or YOUR name) []:*.xip.io`<br>
`> Email Address []:gamesinfourjc@gmail-com`<br>
`> Please enter the following 'extra' attributes to be sent with your certificate request`<br>
`> A challenge password []:gugus`<br>
`> An optional company name []:URJC`<br>

Tras ello, creamos el segundo certificado:

* `sudo openssl x509 -req -days 365 -in xip.io.csr \-signkey xip.io.key \-out xip.io.crt`

Tras su finalizaci�n se podr� comprobar mediante el comando 'dir' que se tienen los siguientes ficheros en el directorio:
  * `xip.io.key`
  * `xip.io.csr`
  * `xip.io.crt`

Finalmente se crea el certificado necesario para haproxy, creado a partir de `xip.io.key`y `xip.io.crt`, mediante el comando:

* `sudo -s cat xip.io.crt xip.io.key \ | sudo tee xip.io.pem`

Completando este �ltimo comando, se puede comprobar que adem�s de contener los tres ficheros anteriores, ahora tambi�n se contiene a `xip.io.pem`.

En el caso de que se haya perdido un paso, tiene m�s informaci�n en este [enlace](https://serversforhackers.com/c/using-ssl-certificates-with-haproxy) y en este [enlace](https://www.youtube.com/watch?v=PsZ6MOQXRGM).

### 5.- Configuracion de HAProxy ###
Una vez se ha notificado la correcta instalaci�n, nos disponemos a configurar HAProxy. Para ello nos dirigimos a `/etc/haproxy` y all�, se aprueban los permisos del archivo `haproxy.cfg`:

* `chmod +rwx haproxy.cfg`

Y se procede a editarlo:

* `sudo nano haproxy.cfg`

En �l se a�aden las siguientes l�neas:

* Debajo de daemon:
  * `maxconn 3072`
  
* En la secci�n defaults:
  * `option forwardfor`
  * `option http-server-close`
  
* Y se crea una nueva secci�n a�adiendo:
  * `listen haproxy`<br>
       `bind 0.0.0.0:443 ssl crt /etc/ssl/xip.io/xip.io.pem`<br>
       `mode http`<br>
       `stats enable`<br>
       `stats uri /haproxy?stats`<br>
       `balance roundrobin`<br>
       `option http-server-close`<br>
       `option forwardfor`<br>
       `reqadd X-Forwarded-Proto:\ https`<br>
       `reqadd X-Forwarded-Port:\ 443`<br>
       `option forwardfor if-none`<br>
       `option abortclose`<br>
       `server nombre1 direccionIP:Puerto`<br>
       `server nombre2 direccionIP:Puerto`<br>
       `...`
       
HAProxy ofrece principalmente tres algoritmos de balanceo:
  
  * **Basado en Round Robin**: el balanceador selecciona a los distintos servidores por turnos
    * `balance roundrobin`
  * **Basado en el numero de conexiones**: el balanceador selecciona el servidor con menor n�mero de conexiones, empleando Round Robin en aquellos empatados
    * `balance leastconn`
  * **Basado en la IP origen y/o destino**: el balanceador selecciona el servidor en funci�n del seleccionado inicialmente a un usuario.
    * `balance source`
    
Puesto que en esta aplicaci�n web se realiza el uso de **tokens**, para eviar la p�rdida de ellos, se emplear� el algoritmo basado en la IP origen y/o destino, sustituyendo por tanto el `roundrobin` por `source`. 

El archivo deber�a quedar como se observa en la imagen de a continuaci�n:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/terminal_haproxy.jpg?raw=true">
</p>

Finalmente se guarda el archivo mediante `Ctrl + X`, afirmando que se est� seguro de guardar, y sobreescribiendo el archivo. Y se reinicia el servicio:

* `sudo service haproxy restart`

### 6.- Inicio de HAProxy ###
Tras la notificaci�n del correcto reinicio, se procede a arrancar HAProxy:

* `sudo service haproxy start`

### 7.- Inicio de HAProxy en Navegador Web ###
Una vez el terminal notifica su inicio, ya se puede uno dirigir a un navegador y colocar la direcci�n local seguida de `/haproxy?stats`  en nuestro caso ser�a `https://192.168.33.16:443/haproxy?stats` para poder observar los datos del balanceador:

 ![Arranque de HAProxy Web](https://github.com/lalinlulelo/GamesInfo/blob/master/images/haproxy_web.png?raw=true)

## Instrucciones para la instalacion de HAProxy para Servicio Interno ##

### 1.- Instalacion PPA ###
Debido a que Ubuntu 14.04 no soporta la versi�n estable de HAProxy (v 1.5), se emplea una PPA (Personal Package Archives) para poder realizar la instalaci�n con `apt-get`:

* `add-apt-repository ppa:vbernat/haproxy-1.5`

### 2.- Actualizacion del sistema ###
El siguiente paso es actualizar el sistema:

* `apt-get update`
* `apt-get dist-upgrade`

### 3.- Instalacion de HAProxy ###
Tras la correcta actualizaci�n, se instala HAProxy:

* `apt-get install haproxy`

### 4.- Configuracion de HAProxy ###
Una vez se ha notificado la correcta instalaci�n, nos disponemos a configurar HAProxy. Para ello nos dirigimos a `/etc/haproxy` y all�, se aprueban los permisos del archivo `haproxy.cfg`:

* `chmod +rwx haproxy.cfg`

Y se procede a editarlo:

* `sudo nano haproxy.cfg`

En �l se a�aden las siguientes l�neas:

* Debajo de daemon:
  * `maxconn 3072`
  
* En la secci�n defaults:
  * `option forwardfor`
  * `option http-server-close`
  
* Y se crea una nueva secci�n a�adiendo:
  * `listen haproxy`<br>
       `bind 0.0.0.0:80`<br>
       `mode http`<br>
       `stats enable`<br>
       `stats uri /haproxy?stats`<br>
       `balance source`<br>
       `option httpclose`<br>
       `option forwardfor`<br>
       `server nombre1 direccionIP:Puerto`<br>
       `server nombre2 direccionIP:Puerto`<br>
       `...`<br>

El archivo deber�a quedar como se observa en la imagen de a continuaci�n:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/terminal_haproxy_2.jpg?raw=true">
</p>

Finalmente se guarda el archivo mediante `Ctrl + X`, afirmando que se est� seguro de guardar, y sobreescribiendo el archivo. Y se reinicia el servicio:

* `sudo service haproxy restart`

### 5.- Inicio de HAProxy ###
Tras la notificaci�n del correcto reinicio, se procede a arrancar HAProxy:

* `sudo service haproxy start`

### 6.- Inicio de HAProxy en Navegador Web ###
Una vez el terminal notifica su inicio, ya se puede uno dirigir a un navegador y colocar la direcci�n local seguida de `/haproxy?stats`  en nuestro caso ser�a `http://192.168.33.17/haproxy?stats` para poder observar los datos del balanceador:

 ![Arranque de HAProxy Web](https://github.com/lalinlulelo/GamesInfo/blob/master/images/haproxy_web.png?raw=true)

## Instrucciones para la instalacion de HAProxy para Bases de datos ##

### 1.- Instalacion PPA ###
Debido a que Ubuntu 14.04 no soporta la versi�n estable de HAProxy (v 1.5), se emplea una PPA (Personal Package Archives) para poder realizar la instalaci�n con `apt-get`:

* `add-apt-repository ppa:vbernat/haproxy-1.5`

### 2.- Actualizacion del sistema ###
El siguiente paso es actualizar el sistema:

* `apt-get update`
* `apt-get dist-upgrade`

### 3.- Instalacion de HAProxy ###
Tras la correcta actualizaci�n, se instala HAProxy:

* `apt-get install haproxy`

### 4.- Configuracion de HAProxy ###
Una vez se ha notificado la correcta instalaci�n, nos disponemos a configurar HAProxy. Para ello nos dirigimos a `/etc/haproxy` y all�, se aprueban los permisos del archivo `haproxy.cfg`:

* `chmod +rwx haproxy.cfg`

Y se procede a editarlo:

* `sudo nano haproxy.cfg`

En �l se debe borrar/comentar todo lo presente e insertar las siguiente l�neas:
<br>
* `global`<br>
  `log 127.0.0.1 local0 notice`<br>
  `user haproxy`<br>
  `group haproxy`<br>
<br>
  `defaults`<br>
  `log global`<br>
  `retries 2`<br>
  `timeout connect 3000`<br>
  `timeout server 5000`<br>
  `timeout client 5000`<br>
<br>
  `listen mysql-cluster`<br>
  `bind 192.168.33.18:3306`<br>
  `mode tcp`<br>
  `option mysql-check user haproxy_check`<br>
  `balance roundrobin`<br>
  `server host_name_1 192.168.33.12:3306 check`<br>
  `server host_name_2 192.168.33.15:3306 check`<br>
<br>
  `listen stats`<br>
  `bind 0.0.0.0:80`<br>
  `mode http`<br>
  `stats enable`<br>
  `stats uri /haproxy?stats`<br>

El archivo deber�a quedar como se observa en la imagen de a continuaci�n:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/terminal_haproxy_3.jpg?raw=true">
</p>

Finalmente se guarda el archivo mediante `Ctrl + X`, afirmando que se est� seguro de guardar, y sobreescribiendo el archivo. Y se reinicia el servicio:

* `sudo service haproxy restart`

### 5.- Configuracion de mysql ###
Una vez reiniciado el servicio de haproxy, nos dirigimos a la terminal de las dos m�quinas virtuales de las bases de datos y realizamos simult�neamente en las dos los siguientes comandos:

  * `mysql -u root -p -e "INSERT INTO mysql.user (Host, User) values ('192.168.33.18','haproxy_test'); FLUSH PRIVILEGES;"`
  * `mysql -u root -p -e "GRANT ALL PRIVILEGES ON *.* TO 'haproxy_root'@'192.168.0.50' IDENTIFIED BY 'haproxy' WITH GRANT OPTION; FLUSH PRIVILEGES;"`
 
Con ello creamos un usuario con el que haproxy comprobar� si las BBDD est�n operables y otro usuario con el que acceder� a los datos.

### 6.- Estructuracion de Servidores de Bases de Datos en Maestro-Esclavo ###
Para poder tener consistencia en ambas bases de datos, necesitamos que una de las bases escuche a la otra, teniendo la jerarqu�a de Maestro-Servidor. En nuestro caso el Maestro ser� la m�quina virtual con direcci�n IP `192.168.33.12`, y el Esclavo ser� la m�quina virtual con direcci�n IP `192.168.33.15`.

  #### 6.1.- Servidor Maestro #####
  Nos dirigimos al fichero `my.cfg` situado en `/vagrant/etc/mysql/` mediante el editor (`sudo nano my.cfg`) habiendo habilitado los   
  permisos previamente (`chmod +rwx my.cfg`). En �l descomentamos, modificamos o a�adimos las siguientes instrucciones:
  
  * `server-id=1`<br>
  * `log-bin=mysql-bin`<br>
  * `sync_binlog=1`<br>
  * `max-binlog-size=500M`<br>
  * `expire_logs_days=4`<br>
  * `innodb_flush_log_at_trx_commit=1`<br>
  
  Y una vez guardado el fichero (`Ctrl + X`), reiniciamos el servicio de mysql con:
  
  * `sudo service mysql restart`
  
  Tras ello, nos dirigimos inicialmente al directorio principal (`cd /vagrant`) y all� nos dirigimos a mysql (`mysql -u root -p`) y 
  realizamos los siguiente comandos:
  
  * `CREATE USER root IDENTIFIED BY 'gugus';`
  * `GRANT REPLICATION SLAVE ON *.* TO 'root'@'192.168.33.15' IDENTIFIED BY 'gugus';`
  * `flush privileges;`
  
  Con ello creamos el usuario esclavo que pertenecer� al segundo servidor. Ahora toca realizar una copia de la base de datos, primero en 
  mysql con:
  
  * `use gamesinfo_db;`
  * `FLUSH TABLES;`
  * `FLUSH TABLES WITH READ LOCK;`
  * `SHOW MASTER STATUS;`
  
  Con esta �ltima instrucci�n deber�a de salir algo simmilar a la siguiente imagen, por consola:
  
  <p align="center">
    <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/mysql_master.jpg?raw=true">
  </p>
  
  Nos debemos quedar con los dos valores impresos, para emplearlos m�s adelante. A continuaci�n salimos de mysql, retornando al 
  directorio vagrant (`/vagrant`). All� realizamos el siguiente comando, mediante el cual nos aparecer� en la carpeta de la m�quina 
  virtual (en nuestro caso `C:/Users/guille-hp/Documents/vagrant/base_de_datos_1`) el fichero '.sql':
  
  * `mysqldump -u root -p gamesinfo_db >gamesinfo_db.sql`
  
  Dicho fichero '.sql' lo copiamos y pegamos en la carpeta de la segunda m�quina con Base de Datos (en nuestro caso `C:/Users/guille-
  hp/Documents/vagrant/base_de_datos_2`). Y nos trasladamos a la segunda m�quina.
  
  #### 6.2.- Servidor Esclavo #####
  Nos dirigimos al fichero `my.cfg` situado en `/vagrant/etc/mysql/` mediante el editor (`sudo nano my.cfg`) habiendo habilitado los   
  permisos previamente (`chmod +rwx my.cfg`). En �l descomentamos, modificamos o a�adimos las siguientes instrucciones:
  
  * `server-id=2`<br>
  * `relay-log=mysqld-relay-bin`<br>
  * `max-relay-log-size=500M`<br>
  * `relay_log_purge=1`<br>
  
   Y una vez guardado el fichero (`Ctrl + X`), reiniciamos el servicio de mysql con:
  
  * `sudo service mysql restart`
  
  Tras ello, nos dirigimos inicialmente al directorio principal (`cd /vagrant`) y all� nos dirigimos a mysql (`mysql -u root -p`) y 
  realizamos los siguiente comandos:
  
  * `CHANGE MASTER TO MASTER_HOST='192.168.33.12',`<br>
    `-> MASTER_USER='root',`<br>
    `-> MASTER_PASSWORD='gugus',`<br>
    `-> MASTER_LOG_FILE='mysql-bin.000001',`<br>
    `-> MASTER_LOG_POS=727,`<br>
    `-> MASTER_PORT=3306;`<br>
    
  En el comando anterior, debemos remarcar que en los campos **MASTER_LOG_FILE** y **MASTER_LOG_POS** se coloquen los dos datos 
  observados en el apartado anterior, al realizar el comando `SHOW MASTER STATUS` sobre el terminal mysql de la primera m�quina 
  virtual. El comando quedar�a semejante al de la siguiente imagen:

  <p align="center">
    <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/mysql%20slave.jpg?raw=true">
  </p>

  Y tras dicho comando ejecutamos:

  * `START SLAVE;`
  * `UNLOCK TABLES;`

  Si se desea comprobar el correcto funcionamiento del esclavo, se emplea el siguiente comando en mysql (`mysql>`):

  * `SHOW SLAVE STATUS\G`

  El cual mostrar� un listado de datos. Se puede mirar el valor �Seconds_Behind_Master� que indica qu� �retraso� tiene el servidor 
  esclavo respecto al maestro (si es NULL se trata de mal funcionamiento. Revisando el �Slave_IO_State� y �Last_Error�).    
  
### 7.- Inicio de HAProxy ###
Tras la notificaci�n del correcto reinicio, se procede a arrancar HAProxy:

* `sudo service haproxy start`

### 8.- Inicio de HAProxy en Navegador Web ###
Una vez el terminal notifica su inicio, ya se puede uno dirigir a un navegador y colocar la direcci�n local seguida de `/haproxy?stats`  en nuestro caso ser�a `http://192.168.33.17/haproxy?stats` para poder observar los datos del balanceador:

 ![Arranque de HAProxy Web](https://github.com/lalinlulelo/GamesInfo/blob/master/images/haproxy_web.png?raw=true)

## Instalacion e Implementacion de Hazelcast ##
Para evitar perder la sesi�n durante la ca�da de un servidor se emplea la replicaci�n de sesi�n mediante Hazelcast, empleando una cach� distribuida entre los servidores presentes en un balanceador:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/Hazelcast%20Explanation.png?raw=true">
</p>

### 1.- Instalacion de Hazelcast ###
Para poder emplear Hazelcast en nuestro proyecto de la aplicaci�n web, es necesario insertar las siguientes dependencias en el fichero `pom.xml`:

  * Jackson Core:<br>
    `<dependency>`<br>
    `    <groupId>com.fasterxml.jackson.core</groupId>`<br>
    `    <artifactId>jackson-databind</artifactId>`<br>
    `    <version>2.5.3</version>`<br>
    `</dependency>`<br>
  * Jackson Datatype:<br>
    `<dependency>`<br>
    `    <groupId>com.fasterxml.jackson.datatype</groupId>`<br>
    `    <artifactId>jackson-datatype-jsr310</artifactId>`<br>
    `    <version>2.5.3</version>`<br>
    `</dependency>`<br>
  * Springframework Session:<br>
    `<dependency>`<br>
    `    <groupId>org.springframework.session</groupId>`<br>
    `    <artifactId>spring-session</artifactId>`<br> 
    `</dependency>`<br>
  * Hazelcast:<br>
    `<dependency>`<br>
    `    <groupId>com.hazelcast</groupId>`<br>
    `    <artifactId>hazelcast</artifactId>`<br>
    `    <version>3.9.3</version>`<br>
    `</dependency>`<br>
  * Hazelcast Spring:<br>
    `<dependency>`<br>
    `    <groupId>com.hazelcast</groupId>`<br>
    `    <artifactId>hazelcast-spring</artifactId>`<br>
    `    <version>${hazelcast.version}</version>`<br>
    `</dependency>`<br>
  * Hazelcast WM<br>
    `<dependency>`<br>
    `    <groupId>com.hazelcast</groupId>`<br>
    `    <artifactId>hazelcast-wm</artifactId>`<br>
    `    <version>${hazelcast.version}</version>`<br>
    `</dependency>`<br>

### 2.- Implementacion de Hazelcast ###
Para hacer funcional Hazelcast en nuestro proyecto, despues de haberlo actualizado mediante `Maven > Maven Update`, nos dirigimos a la clase principal del proyecto e insertamos el siguiente `@Bean`, donde las dos direcciones IP presentes son las de los dos servidores que portar�n esta aplicaci�n:
<br>
`@Bean`<br>
`public Config config() {`<br>
`   Config config = new Config();`<br>
`   JoinConfig joinConfig = config.getNetworkConfig().getJoin();`  
`   joinConfig.getMulticastConfig().setEnabled(false);`<br>
`   joinConfig.getTcpIpConfig().addMember( "192.168.33.13" ).addMember( "168.192.33.10" ).setEnabled( true );`<br>
`   return config;`<br>
`}`<br>

## Fichero Batch de Arranque ##
Para facilitar la creaci�n de las 9 ventanas de comando, y su debido arranque se ha elaborado un script `.bat` automatizando brevemente el arranque de las m�quinas. Para ello, se crea un fichero .txt, al cual se le cambia la terminaci�n a .bat en el Sistema Operativo Host, y se abre con un editor de texto (en nuestro caso `notepad++`). Y en �l se escribe la siguiente secuencia de comandos:
  <br>
  <br>
  `@echo off`<br>
  `title Initialization of GamesInfo Program`<br>
  `echo Welcome to GamesInfo! Don't be scared, we're gonna open some vm`<br>
  <br>
  `rem ----- haproxy`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\haproxy_1 & mode 56, 10 & vagrant up & vagrant ssh"`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\haproxy_2 & mode 56, 10 & vagrant up & vagrant ssh"`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\haproxy_3 & mode 56, 10 & vagrant up & vagrant ssh"`<br>
  <br>
  `rem ----- server`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\server_1 & mode 85, 10 & vagrant up & vagrant ssh"`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\server_2 & mode 85, 10 & vagrant up & vagrant ssh"`<br>
  <br>
  `rem ----- mail service`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\servicio_interno_1 & mode 85, 10 & vagrant up & vagrant ssh"`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\servicio_interno_2 & mode 85, 10 & vagrant up & vagrant ssh"`<br>
  <br>
  `rem ----- database`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\base_de_datos_1 & mode 85, 10 & vagrant up & vagrant ssh"`<br>
  `start cmd /k "cd C:\Users\guille-hp\Documents\vagrant\base_de_datos_2 & mode 85, 10 & vagrant up & vagrant ssh"`<br>
  <br>
  `cls`<br>
  `echo Now we're gonna open some information's windows.`<br>
  `pause`<br>
  `start "" https://192.168.33.16/haproxy?stats`<br>
  `start "" http://192.168.33.17/haproxy?stats`<br>
  `start "" http://192.168.33.18/haproxy?stats`<br>
  `start "" https://192.168.33.16/`<br>
  <br>
  `cls`<br>
  `echo Now wait until all the programs are ready, and put them 'vagrant ssh'`<br>
  `pause`<br>
  `exit `<br>

## Diagrama de la Infraestructura desplegada ##
En el siguiente diagrama se puede visualizar la infraestructura desplegada de la Aplicaci�n Web:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/Diagrama%20de%20Infraestructura.png?raw=true" style="width: 50%; height: 50%">
</p>

# Fase 5 #
En esta fase se solicita automatizar el despliegue de la aplicaci�n mediante el sistema de gesti�n de configuraci�n Ansible. Para ello seguimos los siguientes pasos

## 1.- Creacion de una Maquina Virtual Vagrant ##
Para evitar provocar fallos en el resto de m�quinas virtuales, las cuales se encuentran en correcto funcionamiento, se crea una nueva m�quina virtual a la que se ha apodado su directorio `ansible`, y su direcci�n Ip ha sido ajustada a `192.168.33.19` (mediante la modificaci�n del fichero `Vagrantfile`). En caso de no acordarse de los pasos para crear una m�quina virtual e iniciarla con Java y MySQL dirigete a esta [seccion](#instalacion-de-vagrant).

Una vez teniendo la m�quina virtual instalada e inicializada (mediante `vagrant up`y `vagrant ssh`), procedemos a instalar Ansible. Para ello realizamos el siguiente comando:

* `sudo apt-add-repository -y ppa:ansible/ansible`
* `sudo apt-get update`
* `sudo apt-get install -y ansible`

## 2.- Configuracion de Ansible ##
Finalizada su instalaci�n, nos dirigimos al directorio `/etc/ansible` y accedemos al fichero `hosts` (`sudo nano hosts`), habiendo habilitado previamente los permisos (`chmod +rwx hosts`). En �l a�adimos los distintos servidores con las siguiente serie de  instrucciones:

   `[webservers]`<br>
   `192.168.33.10`<br>
   `192.168.33.13`<br>
   <br>
   `[internalservers]`<br>
   `192.168.33.11`<br>
   `192.168.33.14`<br>
   <br>
   `[dbservers]`<br>
   `192.168.33.12`<br>
   `192.168.33.15`<br>
   <br>
   `[haproxyservers]`<br>
   `192.168.33.16`<br>
   `192.168.33.17`<br>
   `192.168.33.18`<br>
   <br>
   `[global]`<br>
   `192.168.33.19`<br>

Tras ello guardamos el fichero (`Ctrl + X`). Y nos dirigimos al fichero `ansible.cfg` del mismo directorio (`sudo nano ansible.cfg`), habiendo habilitado previamente los permisos (`chmod +rwx hosts`). En �l descomentamos la l�nea:

  * `host_key_checking = False`
  
Y guardamos el fichero (`Ctrl + X`).

## 3.- Creacion de la clave privada ##
Para poder operar con ansible, es necesario generar una clave privada, para ello nos dirigimos al directorio principal (`cd /vagrant`) y comprobamos si tenemos el directorio `.ssh` en �l (`ls -a`). En caso de no tenerlo, lo creamos con el comando:

  * `sudo mkdir .ssh`
  
Y accedemos a �l (`cd .ssh`). En �l ejecutamos el siguiente comando:
  
  * `ssh-keygen`
 
En �l se nos solicitar� un nombre para la clave el cual se pondr� **id_rsa**. Y posteriormente una contrase�a con la encriptarlo, en nuestro caso se ha puesto 'gugus' en ambas solicitudes de contrase�a. Una vez generadas las claves podemos comprobar su existencia mediante el comando `dir`.

A continuaci�n, nos dirigimos al Sistema Operativo Host (en nuestro caso `Windows`), y en �l al directorio de la m�quina (en nuestro caso `/Documents/vagrant/ansible` y en �l, a la carpeta `.ssh` podiendo observar la presencia de las dos claves creadas (`id_rsa`y `id_rsa.pub`). 

Copiamos la clave p�blica (`id_rsa.pub`) y la pegamos en los directorios del resto de m�quinas virtuales (los 2 servidores web, los 2 servicios internos, las 2 bases de datos y los 3 balanceadores), sin necesidad de crear carpetas adicionales (junto al `VagrantFile` de la m�quina determinada).

## 4.- Comprobacion de conexion ##
Para poder comprobar que las conexiones a los distintos servidores se encuentran operables, incialmente arrancamos los 9 servidores, **no** arrancando sus respectivos ficheros `-jar`. Y una vez inicializados, nos dirigimos a la m�quina virtual de **ansible**, en ella al directorio `/vagrant/.ssh/` y ejecutamos el siguiente comando por cada servidor que tenemos:

*  `ssh -i id_rsa direccionIPservidor_x `

Por ejemplo en el caso de el servidor web 1:

* `ssh -i id_rsa 192.168.33.10`

Tras ello nos solicitar� la contrase�a de dicha m�quina virtual, en el caso de que no se haya modificado la contrase�a, se deber�a insertar la contrase�a por defecto de dicha m�quina virtual: `vagrant` (en nuestro caso se cambiaron todas las contrase�as de las m�quinas virtuales mediante el comando `passwd`a la contrase�a `password`). Obteniendo una imagen semejante a la siguiente como resultado:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/ansible_terminal.jpg?raw=true">
</p>
 
## 5.- Demostracion del Correcto Funcionamiento ##
Finalmente se pueden realizar comandos simples mediante el siguiente comando:

* `ansible _conjunto -m shell -a "comando_a_ejecutar_las_mv" --private-key id_rsa --ask-pas --ask-sudo-pass`

Por ejemplo, si deseamos que todas las m�quinas virtuales impriman el mensaje 'hi', realizamos el siguiente comando:

* `ansible all -m shell -a "/bin/echo hi" --private-key id_rsa --ask-pass --ask-sudo-pass`

Mostrando el siguiente resultando:

<p align="center">
  <img src="https://github.com/lalinlulelo/GamesInfo/blob/master/images/ansible_hi.jpg?raw=true">
</p>

En el caso de que se qusiese realizar un comando a solo un grupo de m�quinas (por ejemplo `webservers`) emplear�amos el siguiente comando: 

* `ansible webservers -m shell -a "comando_a_ejecutar_las_mv" --private-key id_rsa --ask-pas --ask-sudo-pass`

Y en el caso de que se quisiera realizar m�s de un comando se emplear�a `"comando_1 & comando_2 & etc."`.

## 6.- Creacion de Playbooks ##
Una vez comprobado mediante varias pruebas, su correcto funcionamiento, toca crear una seria de documentos llamados **playbooks** los cuales contienen una serie de instrucciones que inicializan una m�quina virtual en caso de posible p�rdida. Para ello inicialmente hemos de descargar una serie de paquetes provenientes de la p�gina [Ansible Galaxy](https://galaxy.ansible.com/list#/roles?page=1&page_size=10) siendo una biblioteca con playbooks configurados para instalar programas. Los paquetes a descargar e instalar en la m�quina virtual de ansible son los siguientes:

 ### 6.1 Java ###
 Para poder instalar Java 7 y 8 en una m�quina, tendremos que dirigirnos a la p�gina de java con m�s relevancia de Ansible Galaxy 
 mediante este [enlace](https://galaxy.ansible.com/kbrebanov/java/). Ah� el creador nos indica entre otras cosas, que lo hemos de 
 instalar en la m�quina virtual de ansible con el siguiente comando:
 
 * `ansible-galaxy install kbrebanov.java`
 
 Tras terminar la instalaci�n, nos indicar� que ha creado un fichero en el directorio `./ansible/roles` nombrado `kbrebanov.java` 
 siendo un directorio. Debido a que en la aplicaci�n web se tiene una base de datos maestra y una base de datos esclava, vamos a tener 
 que modificar dos veces ese directorio, para ello creamos dos copias del directorio en el mismo lugar (`.ansible/roles`) mediante los 
 siguientes comandos.
 
  * `cp -a kbrebanov.java/ ./java_8.java`
  * `cp -a kbrebanov.java/ ./java_7.java`

 Tras comprobar mediante el comando `dir` que se han creado correctamente las dos copias del directorio, nos adentramos en 
 **java_7.java** (mediante el comando `cd`), podiendo observar mediante el comando `dir` la presencia de las siguientes carpetas en su
 interior:
   
  * `defaults`
  * `meta`
  * `README.md`
  * `tests`
  * `tasks`
  * `vars`
  * `LICENSE`

Nos dirigimos a la carpeta `defaults` y en ella, aportando los derechos de modificacion (`sudo chmod +rwx main.yml`) procedemos a 
la modificaci�n del �nico fichero en su interior `main.yml` (`sudo nano main.yml`). En �l se nos muestra una configuraci�n de 
ejemplo que se tendr� que modificar a nuestro gusto, apoy�ndonos de la informaci�n descrita en la [p�gina de su descarga](https://galaxy.ansible.com/kbrebanov/java/). En dicho fichero introducimos y modificamos, obteniendo la siguiente configuraci�n:
  <br>
  `---                                          `<br>
  `# defaults file for java                     `<br>
  `                                             `<br>
  `java_implementation: openjdk                 `<br>
  `                                             `<br>
  `java_openjdk_version: 7                      `<br>
  `java_openjdk_jre_only: false                 `<br>
  `java_openjdk_headless: false                 `<br>
  `java_openjdk_use_ppa: true                   `<br>
  `                                             `<br>
  `java_oracle_version: 7                       `<br>
  `java_oracle_install_jce_policy: false        `<br>
  
 Tras ello guardamos el fichero mediante `Ctrl + X`.
  
 ### 6.2 MySQL ###
 Para poder instalar mysql en una m�quina, tendremos que dirigirnos a la p�gina de mysql con m�s relevancia de Ansible Galaxy mediante 
 este [enlace](https://galaxy.ansible.com/geerlingguy/mysql/). Ah� el creador nos indica entre otras cosas, que lo hemos de instalar en 
 la m�quina virtual de ansible mediante el comando:
 
  * `ansible-galaxy install geerlingguy.mysql`
      
 Tras terminar la instalaci�n, nos indicar� que ha creado un fichero en el directorio `./ansible/roles` nombrado `geerlingguy.mysql` 
 siendo un directorio. Debido a que en la aplicaci�n web se tiene una base de datos maestra y una base de datos esclava, vamos a tener 
 que modificar dos veces ese directorio, para ello creamos dos copias del directorio en el mismo lugar (`.ansible/roles`) mediante los 
 siguientes comandos.
   
   * `cp -a geerlingguy.mysql/ ./master.sql`
   * `cp -a geerlingguy.mysql/ ./slave.sql`
      
  Tras comprobar mediante el comando `dir` que se han creado correctamente las dos copias del directorio, nos adentramos en 
  **master.sql** (mediante el comando `cd`), podiendo observar mediante el comando `dir` la presencia de las siguientes carpetas en su
  interior:
   
   * `defaults`
   * `handlers`
   * `meta`
   * `README.yml`
   * `tasks`
   * `templates`
   * `vars`
    
   Nos dirigimos a la carpeta `defaults` y en ella, aportando los derechos de modificacion (`sudo chmod +rwx main.yml`) procedemos a 
   la modificaci�n del �nico fichero en su interior `main.yml` (`sudo nano main.yml`). En �l se nos muestra una configuraci�n de 
   ejemplo que se tendr� que modificar a nuestro gusto, apoy�ndonos de la informaci�n descrita en la [p�gina de su descarga](https://galaxy.ansible.com/geerlingguy/mysql/). En dicho fichero introducimos y modificamos, obteniendo la siguiente configuraci�n:
   
   
   Se refresca el fichero de hosts de ansible:
   
   * `ssh-keygen -R ip_maquina_virtual`
   
   ### 6.3 HaProxy ###
   
   ### 6.4 Playbook ###
   Regresamos al directorio `/vagrant/.ssh`(mediante el comando `cd`) y all� creamos el fichero nombre_playbook.yml (mediante el 
   comando `touch nombre_playbook.yml`). Y lo abrimos para editar (`sudo nano nombre_playbook`). Este ser� nuestro fichero de ejecuci�n 
   de los programas a instalar. Para ello seguiremos la siguiente estructura:
   <br>
   `---                                          `<br>
   `- hosts: grupo 1                              `<br>
   `  sudo: yes                                   `<br>
   `  roles:                                      `<br>
   `  - programa_1                                `<br>
   `  - programa_2                                `<br>
   `  - programa_3                                `<br>
   `                                              `<br>
   `- hosts: grupo 2                              `<br>
   `  sudo: yes                                   `<br>
   `  roles:                                      `<br>
   `  - programa_1                                `<br>
   `  - programa_2                                `<br>
   `  - programa_3                                `<br>
   `                                              `<br>
   `etc                                           `<br>
    
# Integrantes
Doble Grado Dise�o y Desarrollo de Videojuegos e Ingenier�a de Computadores.
-  **Agust�n L�pez Arribas**: 
    -   E-mail: a.lopezarri@alumnos.urjc.es
    -   Github: [Agustwin](https://github.com/Agustwin)
        
-  **Zhong Hao Lin Chen**:
    -   E-mail: z.linc@alumnos.urjc.es
    -   Github: [lalinlulelo](https://github.com/lalinlulelo)
        
-  **Guillermo Mel�ndez Morales**:
    -   E-mail: g.melendezm@alumnos.urjc.es
    -   Github: [guillemelmor](https://github.com/guillemelmor)