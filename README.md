# Diseño de Red

<p align="justify">La empresa cuenta con tres departamentos y una red aislada para clientes. Cada departamento tiene su propia subred con una máscara de red adecuada y se emplean direcciones IPv4 en una estructura jerárquica. A continuación, se detalla el diseño de cada segmento de red:</p>

### Departamento 1: 10 empleados
<ul align="justify">
   <li>Direcciones de Red: 192.168.1.0/28</li>
   <li>Puerta de Enlace: 192.168.1.0</li>
   <li>Dirección de Broadcast: 192.168.1.15</li>
   <li>Rango de Hosts Válidos: Entre 192.168.1.1 y 192.168.1.14</li>
</ul>

### Departamento 2: 10 empleados
<ul align="justify">
   <li>Direcciones de Red: 192.168.2.0/28</li>
   <li>Puerta de Enlace: 192.168.2.0</li>
   <li>Dirección de Broadcast: 192.168.2.15</li>
   <li>Rango de Hosts Válidos: Entre 192.168.2.1 y 192.168.2.14</li>
</ul>

### Departamento 3: 15 empleados
<ul align="justify">
   <li>Direcciones de Red: 192.168.3.0/27</li>
   <li>Puerta de Enlace: 192.168.3.0</li>
   <li>Dirección de Broadcast: 192.168.3.31</li>
   <li>Rango de Hosts Válidos: Entre 192.168.3.1 y 192.168.3.30</li>
</ul>

### Red Aislada para Clientes: 5 puestos
<ul align="justify">
   <li>Direcciones de Red: 192.168.4.0/29</li>
   <li>Puerta de Enlace: 192.168.4.0</li>
   <li>Dirección de Broadcast: 192.168.4.7</li>
   <li>Rango de Hosts Válidos: Entre 192.168.4.1 y 192.168.4.6</li>
</ul>

<p align="justify">&nbsp;</p>

<img src="https://github.com/valen28030/Packet_Tracer/assets/167770750/2d301f75-1627-42e7-9e84-d8a86b1a6cd8" alt="1" width="500">

## Incorporar un servidor web a la red para alojar la página web de la empresa

<p align="justify">Para lanzar y mantener la presencia en línea de la empresa, se propone la integración de un servidor web dedicado en la red. A continuación, se detallan los pasos necesarios para implementar esta solución:</p>


<p align="justify"><strong>● Servidor Web</strong></p>
<p align="justify">Se recomienda instalar un servidor web, como Apache, Nginx o Microsoft IIS, en un servidor dedicado. Este servidor será responsable de gestionar las solicitudes de páginas web y mostrarlas a los usuarios.</p>
&nbsp;

<p align="justify"><strong>● Desarrollo de la Página Web</strong></p>
<p align="justify">La creación de la página web se llevará a cabo utilizando tecnologías comunes como HTML, CSS y JavaScript. Esto garantizará una experiencia de usuario intuitiva y atractiva.</p>
&nbsp;

<p align="justify"><strong>● Base de Datos</strong></p>
<p align="justify">Para almacenar y gestionar datos relacionados con la página web, se sugiere conectar una base de datos, como MySQL, PostgreSQL o MongoDB, al servidor web.</p>
&nbsp;

<p align="justify"><strong>● Servidor DNS</strong></p>
<p align="justify">Se ajustarán las configuraciones de DNS para que el dominio de la empresa dirija al servidor web con su dirección IP pública. Además, se aprovecharán servicios de registro de dominios para garantizar una resolución de nombres eficiente.</p>
&nbsp;

<p align="justify"><strong>● Firewall y Seguridad</strong></p>
<p align="justify">Se establecerán reglas en el firewall para permitir el tráfico de páginas web de manera segura. Asimismo, se implementarán certificados SSL/TLS para proteger las comunicaciones entre el servidor web y los usuarios, garantizando la privacidad y la integridad de los datos.</p>
&nbsp;

<p align="justify"><strong>● Gestión de Tráfico</strong></p>
<p align="justify">Se utilizarán herramientas como balanceadores de carga para distribuir la carga entre distintos servidores, lo que mejorará la disponibilidad y el rendimiento del sitio web.</p>
&nbsp;

<p align="justify"><strong>● Backup y Recuperación</strong></p>
<p align="justify">Se creará un plan de respaldo habitual para guardar la configuración del servidor web y la información del sitio. Este plan será crucial para recuperarse en caso de pérdida de datos o interrupciones del servicio.</p>
&nbsp;

<p align="justify"><strong>● Redes Sociales y SEO</strong></p>
<p align="justify">Se agregarán enlaces a redes sociales y se aplicarán estrategias de optimización para motores de búsqueda (SEO) para mejorar la visibilidad del sitio web en línea y aumentar su alcance.</p>
&nbsp;

<p align="justify"><strong>● Actualizaciones y Mantenimiento</strong></p>
<p align="justify">Se realizarán actualizaciones periódicas del software del servidor web y de los elementos del sistema operativo para garantizar la seguridad y el rendimiento óptimo del sitio web.</p>

<p align="justify">Este enfoque integral garantizará una presencia en línea robusta y segura para la empresa, brindando una experiencia positiva a los usuarios y clientes potenciales.</p>

<p align="justify">&nbsp;</p>

## Propuestas de Mejora

<ul align="justify">
   <li>Incorporar un router por cada departamento entre el switch central y los switches departamentales.</li>
&nbsp;
   <li>Añadir nuevos servidores dedicados a Base de Datos, archivos u otras funciones internas.</li>
&nbsp;   
  <li>Instalar puntos de acceso Wi-Fi para mejorar la conectividad a internet.</li>
 &nbsp; 
  <li>Implementar un firewall para proporcionar seguridad en la red.</li>
 &nbsp;
  <li>Considerar la adición de elementos como hubs, repetidores, etc.</li>
</ul>

<p align="justify">&nbsp;</p>

## Pruebas de Conectividad
<p align="justify">Se realizaron pruebas de conectividad para verificar el funcionamiento de la red:</p>

### Probar conexión en PC dentro de la misma red
<ul align="justify">
   <li>Se realizó un ping a la dirección IP de otra computadora dentro de la misma red para asegurar la conectividad interna. Se recibió una respuesta exitosa con un 0% de pérdida de paquetes.</li>
</ul>

![1](https://github.com/valen28030/Packet_Tracer/assets/167770750/7ee7b9c6-9ac3-4cb1-8d21-4baa56078f8f)

&nbsp;

### Probar conexión con el Router
<ul align="justify">
   <li>Se configuró y se probó la conexión con el router utilizando una PDU para enviar mensajes desde una computadora al router y viceversa. Además, se realizó un ping a la dirección IP del router, obteniendo una respuesta positiva en ambos casos.</li>
</ul>

![2](https://github.com/valen28030/Packet_Tracer/assets/167770750/173451d6-ce8f-4645-a291-741288821436)

&nbsp;

### Probar conexión con Internet
<ul align="justify">
   <li>Se creó una conexión a internet a través de una nube y se configuró mediante el router. Posteriormente, se probó la conexión y se obtuvo un resultado exitoso.</li>
</ul>

![3](https://github.com/valen28030/Packet_Tracer/assets/167770750/ab5f20eb-d46a-460e-a08e-91a5f5dc1c4d)

![3 1](https://github.com/valen28030/Packet_Tracer/assets/167770750/3489cabe-99b9-4032-a968-4ab61c0add0c)

&nbsp;

### Otras conexiones
<ul align="justify">
   <li>Se verificó la conexión del servidor a internet mediante un ping a su dirección IP.</li>
</ul>

![4](https://github.com/valen28030/Packet_Tracer/assets/167770750/339c183c-f613-4308-85df-ab26b995346a)

&nbsp;

## Packet Tracer

![gif](https://github.com/valen28030/Packet_Tracer/assets/167770750/2b07d603-a095-4428-883d-47dd2709e69e)


