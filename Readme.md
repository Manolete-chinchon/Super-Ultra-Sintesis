![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/TruePlayer-3-2-2025.png)
<details>
  <summary><h2>📖 Briefing</h2></summary>


<details>
  <summary><b>Idea del Proyecto</b></summary>
  <br>
La idea principal es hacer una pagina web de ventas de zapatos al estilo Nike y Adidas, con un sistema de backups que genere copias de seguridad conectado a un servidor DNS y  además un DHCP que se encargará de asignar direcciones ip a los servidores, las copias seran distribuidas por un servidor Truenas donde será almacenado por los servidores Maestro-esclavo conectados por LDAP todo protegido por un firewall.
</details>

<details>
  <summary><b>Objetivos</b></summary>
  <br>
Queremos que la web tenga la estructura similar a Nike o Adidas, con carrrito, lista de deseos y opciones de crear cuenta e inicio y cerrar sesión. Otra cosas que queremos es que con Mysql guardamos la base de datos y estas se envien al servidor Truenas en forma de backups para que las distribuya a los servidores linux Maestro-Esclavo que lo almacenará. Las Ip seran distribuidas por el DHCP que se situará junto el firewall.
  <br>
  <br>
Nuestro objetivo es aprender las funciones y a manejar el protocolo LDAP y a explorar y poder manejar con fluidez un servidor Truenas. Por parte del protocolo LDAP no conocemos nada y por parte del servidor Truenas sabemos poco y tiene opciones muy interesantes por explorar.
</details>

<details>
  <summary><b>Módulos del ciclo que tengan que ver con el proyecto</b></summary>
<br>
   Los módulos del ciclo que estarán presente en nuestro proyecto serán principalmente:
  <br>
  <br>
  
   Aplicaciones web: Este modulo se implementará para la creación y posterior edición de la web, html y css por parte del contenido y diseño, y php y mysql para la creación y la conexión con una base de datos.
   Seguridad informática: Este modulo se implementará para el uso del servidor Truenas, se encargará de la creación y distribución de los backups a los servidores linux master-slave, además de la implementación de un sistema de seguridad mediante firewall por sophos que tambien hará la función de DHCP.
  Sistemas operativos en red: Este modulo se implementará para la creación y posterior implementación de un servidor apache para el alojamiento de la web y para la comunicación LDAP para los servidores maestro esclavo que conectarán con el TrueNas
   Servicios en red: Este modulo se implementará para la creación del servidor DNS.
</details>

<details>
  <summary><b>Materiales necesarios</b></summary>
   <br>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;Oracle virtualbox para los servidores (DNS + DHCP, Truenas).</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;Sophos firewall.</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;Cisco Packet Tracer (Para mapa lógico).</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;HTML + CSS.</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;APACHE O NGINX (PARA WEB).</p>
</details>
     
<details>
  <summary><b>Recursos</b></summary>
   <br>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;https://www.w3schools.com/html/html_intro.asp</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;https://openwebinars.net/academia/portada/html5-css3/</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;https://askubuntu.com/questions/360190/how-to-configure-master-slave-ldap-replication</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;https://www.youtube.com/watch?v=LzRK_8zwqxY</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;https://somebooks.es/?s=LDAP+</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;https://pandao.github.io/editor.md/en.html</p>
  </details>  
</details>     
     
<details>
  <summary><h2>📋 Planificación  y Arquitectura</h2></summary>

<details>
  <summary><b>Objetivos y Funcionalidades</b></summary>
  <br>
  Replicación de servidor OpenLDAP maestro-esclavo que copia la base de datos de una aplicación web 
  que mejora la seguridad para proteger las copias  
 </details> 
 
<details>
  <summary><b>Tecnologías a Implementar</b></summary>
  <br>
  Las tecnologias que se implementarán en el proyecto 
  <br>
  <br>
    
  **HTML**: HTML (Lenguaje de Marcas de Hipertexto) es el componente más básico de la Web. Define el significado y la estructura del contenido web. 
      
  **CSS** : El CSS podría definirse como un tipo de lenguaje que permite definir y crear la presentación visual de un documento ya estructurado y escrito en un lenguaje de marcado como puede ser HTML. Es decir, permite generar el diseño visual de páginas web e interfaces de usuario.
      
  **PHP** : Ofrece varias posibilidades para contenidos web dinámicos en su sitio web. PHP puede manejar fácilmente.
      una variedad de bases de datos, sistemas de archivos y directorios y también es adecuado para aplicaciones web complejas.
      
  **MySQL** : Es un sistema de gestión de bases de datos relacionales de código abierto. Al igual que con otras bases de datos relacionales, MySQL almacena los datos en tablas formadas
      por filas y columnas. Los usuarios   pueden definir, manipular, controlar y consultar datos con el lenguaje de consulta estructurada, también conocido como SQL.
      
  **JavaScript**: JavaScript es un lenguaje de programación que los desarrolladores utilizan para hacer páginas web interactivas. 
  Desde actualizar fuentes de redes sociales a mostrar animaciones y mapas interactivos, las funciones de JavaScript pueden mejorar la experiencia del usuario de
  un sitio web.
</details>

<details>
  <summary><b>Hardware virtualizado</b></summary>
  <br>
  
  **Firewall**: Un firewall es un sistema de seguridad de red de las computadoras que restringe el tráfico de Internet entrante, saliente o dentro de una red privada. Un firewall decide qué tráfico de red se admite y qué tráfico se considera peligroso. Básicamente, separa el tráfico bueno del malo, o el seguro del no fiable.
 
  **Máquina virtual**: Una máquina virtual (VM) es una representación virtual o emulación de un equipo físico que utiliza software en lugar de hardware para ejecutar programas e implementar aplicaciones. Al utilizar los recursos de una única máquina física, como memoria, CPU, interfaz de red y almacenamiento, las máquinas virtuales permiten a las empresas ejecutar virtualmente varias máquinas con distintos sistemas operativos en un único dispositivo.
</details>

<details>
  <summary><b>Servicios a Implementar</b></summary>
  <br>
  
  **DNS**: El sistema de nombres de dominio (DNS) es el componente del protocolo estándar de Internet responsable de convertir los nombres de dominio de uso humano en las direcciones del protocolo de Internet (IP) que los ordenadores utilizan para identificarse entre sí en la red.
  
  **DHCP**: Este protocolo se encarga de asignar de manera dinámica y automática una dirección IP, ya sea una dirección IP privada desde el router hacia los equipos de la red local, o también una IP pública por parte de un operador que utilice este tipo de protocolo para el establecimiento de la conexión.
  
  **LDAP**: Se trata de un conjunto de protocolos de licencia abierta que son utilizados para acceder a la información que está almacenada de forma centralizada en una red. Este protocolo se utiliza a nivel de aplicación para acceder a los servicios de directorio remoto
  
  **APACHE**: La funcionalidad principal de este servicio web es servir a los usuarios todos los ficheros necesarios para visualizar la web. Las solicitudes de los usuarios se hacen normalmente mediante un navegador (Chrome, Firefox... etc.). Por ejemplo, cuando un usuario escribe en su navegador página.com, esa petición llegará a nuestro servidor Apache que mediante el protocolo HTTP este se encargará de facilitarle los textos, imágenes, estilos, etc. que conforman la portada de nuestra web de forma segura.
</details>

<details>
  <summary><b>Sistemas Operativos a Utilizar</b></summary>
  
| Servicio | Sistema Operativo                             | RAM  | Almacenamiento | Procesadores | Ip           |
| -------- | --------------------------------------------- | ---- | -------------- | ------------ | ------------ |
| Host     | Win11_22H2_Spanish_x64v2                      | 16 GB| 722 GB         | 8            | ?            |
| DNS      | ubuntu-22.04.2-live-server-amd64              | 2 GB | 20 GB          | 2            | ?            |
| DHCP     | ubuntu-22.04.2-live-server-amd64              | 2 GB | 20 GB          | 2            | ?            |
| Apache   | ubuntu-22.04.2-live-server-amd64              | 2 GB | 16 GB          | 2            | ?            |
| Firewall | netgate-installer-v1.0-RC-amd64-20240919-1435 | 3 GB | 20 GB          | 2            | ?            |
| Truenas  | TrueNAS-13.0-U6.3                             | 8 GB | 20 GB x2       | 2            | ?            |

</details>

<details>
  <summary><b>Asignación de Roles y Responsabilidades</b></summary>
 <br>
  Àlex: Parte principal de la web, LDAP, apoyo al Truenas, firewall
  
  Roberto: LDAP, parte principal del Truenas, apoyo a la web, DNS, firewall
</details>

<details>
  <summary><b>Diagrama de Gantt</b></summary>
  
  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/Gr%C3%A1fico%20Diagrama%20de%20Gantt%20Profesional%20Multicolor.png)
</details>

<details>
  <summary><b>Diagrama de red</b></summary>

  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/Captura%20de%20pantalla%202025-02-10%20081700.png)
</details>

</details>

<details>
  <summary><h2>💻 DNS y DHCP</h2></summary>

<details>
  <summary><b>DNS</b></summary>
 <br>
  
Cuando administramos una infraestructura de servidores, es útil poder buscar las direcciones de red o IPs usando un nombre en lugar de tener que recordar números. Para lograr esto, podemos usar el servicio DNS, que convierte los nombres en direcciones IP.
  
En este caso, configuraremos un servidor DNS en Ubuntu 22.04 usando BIND9. Este servidor tendrá dos tipos de zonas:

**Zona directa:** que permite resolver nombres a direcciones IP.

**Zona inversa:** que convierte direcciones IP en nombres.

Requisitos previos:
 - Una MV con Ubuntu Server 22.04 
 - Un  adaptador de red: 
    - Red NAT: 192.168.1.0/24

## Actualización del sistema

Antes de empezar actualizamos el sistema operativo para garantizar que todas las aplicaciones y paquetes estén en su versión más reciente.
Para ello utilizamos los comandos  

**sudo apt update** para listar los paquetes que necesitan actualizaciones.
<br>
**sudo apt upgrade** para realizar las actualizaciones de los paquetes.

También instalamos el servicio Bind9 con el comando:
**sudo apt install bind9**

## Configuración

Para el servidor necesitamos que la IP se mantenga fija para ello modificamos el archivo netplan ubicado en /etc/netplan/00-installer-config.yaml
el resultado deberia tener la siguiente estructura:

   ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/DNS/netplan.JPG)

Para realizar los cambios del netplan aplicamos 
  
    sudo netplan try - Indica si hay algun error en la configuación 
  
    sudo netplan apply - Aplicar los cambios 

## **Zonas**
<br>

**Zona Directa**

El primer archivo que editaremos será el que nos servirá para la zona directa. Para ello en la ubicación /etc/bind/ crearemos un directorio zones, 
copiamos el archivo db.local cambiandole el nombre con el comando
<br>

        sudo cp db.local /etc/bind/zones/db.proyectodns.com

Ahora podemos editar el archivo, debería quedar algo parecido a lo siguiente:

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/DNS/Zona%20directa%20dns.JPG)
<br>

comprobamos que el archivo esta correctamente editado usamos el comando:
<br>

      sudo named-checkzone db.proyectodns.com /etc/bind/zones/db.proyectodns.com
<br>

**Zona Inversa**

Para la zona inversa copiamos el archivo db.127 y lo guardamos en el directorio zones en mi caso lo he llamado db.1.168.192 
<br>

      sudo cp db.127 /etc/bind/zones/db.1.168.192
      
Ahora editamos el contenido del archivo y el resultado debería verse así:

  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/DNS/Zona%20inversa%20DNS.JPG)

Comprobamos que el archivo ha sido correctamente editado con:
<br>

      sudo named-checkzone 6.168.192.in-addr-arpa /etc/bind/zones/db.6.168.192
        
<br>

**Configuración Local**

<br>

Para configurar las zonas de DNS locales para que el servidor resuelva nombres de dominio específicos dentro de la red editaremos el fichero **named.conf.local** antes de editar es recomendable hacer una copia del fichero
con el comando 

<br>

          sudo cp named.conf.local /etc/bind/named.conf.local.BKP

Ahora podemos editar el fichero named.conf.local y el resultado debería ser el siguiente:

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/DNS/named_conf_local.JPG)

<br>
Comprobamos que la configuración es la correcta y no hayamos cometido errores con el comando:

<br>

        named-checkconf

si despues de lanzar el comando no devuelve nada significa que está bien configurado 

<br>

## **Lista de acceso y servidores forwarders**

<br>

Ahora editaremos el fichero **/etc/bind/named.conf.options** para crear una lista de acceso para restringir el acceso a quienes pueden realizar las consultas a nuestro servidor DNS. También pondremos un par de servidores forwarders donde pueda delegar nuestro servidor DNS local cuando no pueda resolver alguna consulta.

El resultado del fichero deberia ser algo parecido al siguiente:

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/DNS/Lista%20de%20acceso%20y%20forwaders.JPG)

<br>

Ya casi finalizamos, pero antes de poner en marcha el servicio modificamos el fichero **/etc/default/named** donde especificaremos la opción-4 como argumento para el usuario bind, que  se crea automáticamente durante la instalación del servicio bind9. 

La opción -4  nos sirve para forzar el uso de IPv4 siempre y evitar  mensajes de error de red inalcanzable por direccionamiento IPv6.

Resultado:

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/DNS/default%20named%20IPV4.JPG)

<br>
Con esto ya tenemos finalizada la configuración de nuestro servicio DNS, para comprobar que todo esta funcionando correctamente.
con:
para iniciar el servicio dns:

        sudo systemctl start bind9
<br>
para visualizar errores y el estado del servicio

        sudo systemctl status bind9

<br>

resultado:
<br>

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/DNS/Status%20Bind9.JPG)
        
</details>

<details>
  <summary><b>DHCP</b></summary>
 <br>
  
</details>

</details>

<details>
  <summary><h2>👩🏿‍💻 Apache</h2></summary>
  <br>

Apache es un servidor web de código abierto y gratuito que ha sido uno de los más populares en el mundo desde su lanzamiento en 1995. Apache es desarrollado y mantenido por la Apache Software Foundation. Es altamente configurable y compatible con una amplia variedad de sistemas operativos, incluyendo Linux, Windows, y macOS.

Apache es utilizado para servir páginas web estáticas y dinámicas a los usuarios a través de internet o una intranet y además apache es compatible con una variedad de lenguajes de programación y tecnologías como PHP, Python, Perl, y más.

Para obtener información de fuentes oficiales entre en este enlace: https://httpd.apache.org/

## Actualización del sistema

Antes de empezar actualizamos el sistema operativo para garantizar que todas las aplicaciones y paquetes estén en su versión más reciente.
Para ello utilizamos los comandos  

**sudo apt update** para listar los paquetes que necesitan actualizaciones.
<br>
**sudo apt upgrade** para realizar las actualizaciones de los paquetes.

## Configuración netplan

Para el servidor necesitamos que la IP se mantenga fija para ello modificamos el archivo netplan ubicado en /etc/netplan/00-installer-config.yaml
el resultado deberia tener la siguiente estructura:

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/netplan%20apache.png)

Para realizar los cambios del netplan aplicamos 
  
    sudo netplan try 
<br>

    sudo netplan apply

## Instalar apache

Ahora que esta todo actualizado y configurado ya podemos instalar el apache, para ello ponemos el sguiente comando:

    sudo apt install apache2

Una vez instalado podemos iniciar el servidor

    systemctl start apache2

Ahora que ya hemos iniciado comprobamos que funcione correctamente

    systemctl status apache2

Todo deberia verse así

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/image.png)

## Configuración de la web

Para empezar entramo en el archivo index.html que se encuaentra en el directorio donde se almacenan las webs

    sudo nano /var/www/html/index.html

Dentro del archivo editamos el codigo para que la web se vea como queramos

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/Html%20juan.png)

A continuacion entramos en los archivos de connfiguracion de la web

    sudo nano /etc/apache2/sites-availible/000-default.conf

Allí configuramos el nombre de dominio, un alias (opcional) para el dominio, la pagina que se mostrará por defecto y la carpeta raíz del sitio web

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/Configuraci%C3%B3n%20web.png)

Luego miraremos los sitios que estan disponibles y luego los que estan activados, comprobamos si nuestra web está activada con los comandos

    sudo ls /etc/apache2/sites-enabled
<br>

    sudo ls /etc/apache2/sites-available

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/Sitios%20activados.png)

Si nuestra web no esta activada aplicamos el siguiente comando para activarla

    sudo a2ensite sitio-web.conf

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/Activar%20sitio.png)
<details>
  <summary><h3>PHP</h3></summary>
  <br>
PHP es un lenguaje de programación que se usa principalmente para crear páginas web dinámicas. Es decir, te permite generar contenido de manera interactiva, por ejemplo, mostrando datos que provienen de una base de datos o personalizando la página según el usuario.

Cuando usas Apache junto con PHP en tu servidor, Apache se encarga de gestionar las solicitudes web, mientras que PHP se encarga de procesar la lógica del lado del servidor y generar el contenido dinámico.

## Instalación PHP
El primer paso es hacer la instalación del php con el siguiente comando:

    sudo apt install php libapache2-mod-php
![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/PHP/Php%20instalaci%C3%B3n.png)

En momentos posteriores la instalación creamos un archivo php, le ponemos un codigo que genera automáticamente. Para crear el archivo php usamos el siguiente comando.

    sudo nano /var/www/juan/info.php
![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/PHP/Archivo%20php.png)

Una vez creado el archivo vamos a un cliente a la web que esté conectado, ponemos la ip del servidor en el buscador y nos deberia llevar a la web apache generada anteriormente.
![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/apache/PHP/Comprobacion%20php.png)
</details>

</details>
<details>
  <summary><h2>🔥 Firewall</h2></summary>

  <details>
  <summary><b>PfSense</b></summary>
    <br>
PfSense es un sistema operativo basado en FreeBSD que funciona como firewall y router. Es muy utilizado para gestionar redes, filtrar tráfico, crear redes privadas virtuales (VPN), y mucho más. En este caso, lo instalaremos en una máquina virtual o física, configurando una red interna y un adaptador puente para permitir la comunicación entre dispositivos.

Imagen ISO de pfSense: https://www.pfsense.org/download/

## Preparación del entorno

Adaptador de red: Puente (Para la WAN)

Adaptador de red: Red interna (Para la LAN)

Para instalar pfSense en la MV voy a utilizar la siguiente configuración:

RAM: 3 GB

HDD:  20 GB

S.O.:  BSD

## Instalación de pfSense
Para la instalacion de Pfsense realizaremos la configuración predeterminada. Para ello seguiremos los pasos siguientes.

Une vez que iniciamos la máquina nos saltara un aviso de derechos de copyright de netgate, aceptamos para continuar la instalación.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/derechos%20Copyright%20pfsense.PNG)


Luego seleccionamos la opción de instalar Pfsense para continuar con la configuración.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Opci%C3%B3n%20de%20instalaci%C3%B3n%20pfsense.PNG)


Luego nos saltará un mensaje para que configuremos las opciones de red. En este caso nos pide que configuremos que interfaz de red será utilizada para la WAN, escogemos la em0.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/WAN%20em0.PNG)


Como la configuración de la WAN sera dada por DHCP dejamos todo por defecto y seguimos con la instalación.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/continuamos%20con%20la%20instalacion.PNG)


Una vez terminamos la configuración de la wan, nos saldrá el siguiente mensaje que no hemos asignado la interfaz de LAN. seleccionamos la segunda interfaz disponible em1 para asignarla como LAN.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/seleccionamos%20la%20lan.PNG)

Una vez seleccionada la interfaz que utilizaremos como LAN, dentro de la configuración podemos escoger la ip que queramos asignarle al firewall y  también los rangos de IP que queremos que sean asignados a los equipos. Una vez finalizada la configuración que queramos o necesitemos asignar continuamos con la instalación. 

la configuración que hemos hecho en este caso es la siguiente:

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Configuraci%C3%B3n%20IP%20LAN.PNG)


Confirmamos la configuración de interfaces que hemos realizado.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Confirmaci%C3%B3n%20de%20interfaces.PNG)


Despues de terminar con la configuración de interfaces y continuar nos saldrá un mensaje preguntando si queremos instalar la community edition de pfsense aceptamos y continuamos.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Intalaci%C3%B3n%20community%20edition%20pfsense.PNG)


Dejamos la configuración por defecto ya que son las recomendadas y continuamos. Para los siguientes mensajes los aceptamos todos para realizar el particionado por defecto.

![](hhttps://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Partici%C3%B3n%20y%20fichero%20por%20defecto.PNG)


Seleccionamos la instalación de la última version estable, con esto empezará el proceso de instalación.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/%C3%BAltima%20versi%C3%B3n.PNG)


Cuando finaliza el proceso de instalación deberemos reiniciar el sistema, despues apagamos la máquina, quitamos la ISO de Pfsense y volvemos a encender la máquina para poder iniciar correctamente. de lo contrario la máquina virtual nos volverá a lanzar al inicio del proceso de instalación.

resultado:

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/configuraci%C3%B3n%20adaptadores.png)


## Configuración de pfSense

Una vez finalizada la instalación de Pfsense, abrimos una máquina cliente para comprobar que nos brinda la IP dentro del rango configurado y comprobamos que tenemos acceso a internet abriendo el navegado y entrando a una página cualquiera o haciendo un Ping.

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Ping%20y%20navegador.png)

Una vez confirmado que todo esta correctamente, abrimos el navegador y escribimos la IP de la LAN para abrir el administrador y poder configurar el firewall.

Inicia sesión con las credenciales predeterminadas (usuario: admin, contraseña: pfsense).
![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Intefaz%20Pfsense.png)


![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Interfaz%20Interior.png)

Una vez dentro nos desplazamos a la configuración general para definir el DNS y si quermos también el dominio

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Configuraciones_Generales.png)

En la configuración del DHCP asignamos el rango de IP que se repartiran

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Configuraci%C3%B3n%20DHCP.png)

Creamos una regla en el portforward para hacer un tunel de comunicación de internet hacia el servidor

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Port%20forward%20http.png)

## OpenVPN

Ahora instalamos las dependencias necesarias para crear nuestro VPN

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Dependencias%20OpenVPN.png)

Generamos las certificaciones para el buen uso

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/OpenVPN_CA.png)

Creamos un usuario especifico para usar en el OpenVPN, cuando ya este creado creamos unas certificaciones especificas para este usuario

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/CertificadosVPN_y_Usuarios.png)

Configuramos la regla para ya tenerlo listo y poder usar el VPN correctamente

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/OpenVPN%20REGLA.png)

En un dispositivo movil, por ejemplo, descargamos una aplicación cualquiera para el VPN, cargamos el archivo VPN y se nos guarada la configuración

<img src="https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/OpenVPN%20interfaz%20movil.jpg" width="500" height="800" />

Le damos a conectar y comenzara a salir un monton de texto hasta que nos diga succes

<img src="https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Conexi%C3%B3n%20VPN.jpg" width="500" height="800" />

Una vez conectados podemos comprobar que podemos entrar a la pagina de configuración de pfsense

<img src="https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Acceso%20pfsense%20movil.jpg" width="500" height="800" />

Tambien al dominio apache situado en la misma red interna

<img src="https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/VPN_WEB.jpg" width="500" height="800" />

## SSH

Creamos la regla para habilitar el ssh y permitir las conexiones hacia el servidor

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/Port%20forward%20SSH.png)

Una vez creado comprobamos las conexiones, si nos conectamos correctamente habremos realizado con éxito la configuración del ssh

![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/firewall/pfsense/comprobaci%C3%B3n%20ssh.png)

<h3>Pruebas y verificación</h3>

Verifica que los dispositivos en la LAN puedan conectarse a Internet.

Prueba la conectividad entre dispositivos en la red interna.

Asegúrate de que el firewall esté funcionando correctamente.

</details>
<details>
  <summary><b>Conexión OpenVPN (extra)</b></summary>
<br>
Este extra trata sobre una conexión de dos maquinas virtuales de dos dispositivos diferentes, para eso necesitamos un router, tres cables ethernet, un cable de corriente y dos PCs con las maquinas virtuales, el firewall pfsense y el cliente windows 10.
Lo primero que hay que hacer es conectar los dos PCs al mismo router para que este todo en la misma red, luego colocar el adaptador de red en red nat de las dos maquinas e iniciarlas. En el firewall pasamos el archivo de vpn de android al cliente ubuntu por los medios que guste, en el windows con cualquier aplicación cargamos el archivo y ya deberia estar en la misma red del firewall.
</details>
</details>

<details>
  <summary><h2>🔐 TrueNas</h2></summary>

</details>

<details>
  <summary><h2>🖥️ Web</h2></summary>
  <details>
<summary><b>Estructura de la web</b></summary>
<br>
    
## Mapa del sitio

  En este mapa se permiten ver las conexiones que hay entre paginas.
    <br>
    
  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/web/Mapa%20del%20sitio.png)

## Mockups

Este es el mockup de la pagina de inicio

  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/web/Mokap%20inicio.png)

Este es el mockup de la pagina de compra

  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/web/Mokup%20compra.png)

Este es el mockup de la pagina del carrito

  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/web/Mokap%20carrito.png)

Este es el mockup de la pagina del login

  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/web/Mokap%20login.png)

Este es el mockup de la pagina del registro

  ![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/web/Mokap%20register.png)
</details>

</details>
