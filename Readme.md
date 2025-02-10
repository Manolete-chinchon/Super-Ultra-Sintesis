![](https://github.com/Manolete-chinchon/Super-Ultra-Sintesis/blob/main/images/TruePlayer-3-2-2025.png)
<details>
  <summary><h2>📖 Briefing</h2></summary>


<details>
  <summary><b>Idea del Proyecto</b></summary>
  <br>
La idea principal es hacer una pagina web de ventas de zapatos al estilo nike y adidas, con un sistema de backups que genere copias de seguridad conectado a un servidor DNS y  además un DHCP que se encargará de asignar direcciones ip a los servidores, las copias seran distribuidas por un servidor Truenas donde será almacenado por los servidores Maestro-esclavo conectados por LDAP todo protegido por un firewall.
</details>

<details>
  <summary><b>Objetivos</b></summary>
  <br>
Queremos que la web tenga la estructura similar a nike o adidas, con carrrito, lista de deseos y opciones de crear cuenta e inicio y cerrar sesión. Otra cosas que queremos es que con Mysql guardamos la base de datos y estas se envien al servidor Truenas en forma de backups para que las distribuya a los servidores linux Maestro-Esclavo que lo almacenará. Las Ip seran distribuidas por el DHCP que se situará junto el firewall.
  <br>
  <br>
Nuestro objetivo es aprender las funciones y a manejar el protocolo LDAP y a explorar y poder manejar con fluidez un servidor Truenas. Por parte del protocolo LDAP no conocemos nada y por parte del servidor Truenas sabemos poco y tiene opciones muy interesantes por explorar.
</details>

<details>
  <summary><b>Módulos del ciclo que tengan que ver con el proyecto</b></summary>
<br>
   Los módulos del ciclo que estarán presente en nuestro proyecto serán principalmente:
   <p>&nbsp;&nbsp;&nbsp;&nbsp;Aplicaciones web.</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;Seguridad informática.</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;Sistemas operativos en red.</p>
   <p>&nbsp;&nbsp;&nbsp;&nbsp;Servicios en red.</p>
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
  <br>
  Ubuntu server versión 22.04.2
  
  TrueNAS CORE 13.0-U6.4
</details>

<details>
  <summary><b>Asignación de Roles y Responsabilidades</b></summary>
 <br>
  Àlex: Parte principal de la web, LDAP, apoyo al Truenas
  
  Roberto: LDAP, parte principal del Truenas, apoyo a la web, DNS
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
