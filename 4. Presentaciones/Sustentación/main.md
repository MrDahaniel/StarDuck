---
marp: true
theme: rose-pine-moon
paginate: true
footer: <div class="foot"> Escuela de Ingeniería de Sistemas e Informática <br> Universidad Industrial de Santander, Bucaramanga, Colombia </div>
---

<style>
    div.names {
        display: grid;
        grid-template-columns: repeat(3, 1fr); 
        justify-items: center;
    }
    div.names .col { text-align: center; }    

    footer  { width: 95%  } 
    div.foot { 
        display: flex;
        align-items: center
    }
    div.foot .shart     { margin-right: auto; }
    div.foot .hugo      { text-align: right; }

    div.twocols {
        display: grid;
        grid-template-columns: repeat(2, 1fr); 
        align-items: center
    }

    div.center-grid     { justify-items: center; }

    div.twocols .col    {  }

    div.center { text-align: center; }

	table.tableizer-table {
		border: 1px solid #D58D8D; 
        color: #FFF;
	} 
	.tableizer-table td {
		padding: 4px;
		margin: 3px;
		border: 1px solid #D58D8D;
		background-color: #242434; 
	}
	.tableizer-table th {
		background-color: #D58D8D; 
		color: #FFF;
		font-weight: bold;
	}
</style>

<h1><center>  Mecanismos de adaptación autonómica de arquitectura software para la plataforma <br> Smart Campus UIS </center></h1>
<hr style="transform: translateY(-30px);margin-top:-5px;margin-bottom:-40px;">
<h6 style="text-align: center;">Trabajo de grado para optar al título de Ingeniero de Sistemas</h6>

<div class="names">
    <div class="col">
        <h3 style="transform: translateY(15px)"> Autor </h3>
        <p> Daniel David <br> Delgado Cervantes </p>
    </div>
    <div class="col">
        <h3 style="transform: translateY(15px)"> Director </h3>
        <p> Gabriel Rodrigo <br> Pedraza Ferreira </p>
    </div>
    <div class="col">
        <h3 style="transform: translateY(15px)"> Codirector </h3>
        <p> Henry Andres <br> Jimenez Herrera </p>
    </div>
</div>

<!-- _footer: '
    <div class="foot">
        <div class="shart">
            <img src="assets/UISLogo Alt.png" width="30%" />
        </div>
        <div class="hugo">
            Escuela de Ingeniería de Sistemas e Informática <br>
            Universidad Industrial de Santander, Bucaramanga, Colombia
        </div>
    </div>
' -->
<!-- _paginate: skip -->

---

<div class="twocols center-grid">

# Agenda

-   [Contexto y problemática](#contexto-y-problemática)
-   [Objetivos](#objetivos)
-   [Metodología](#metodología)
-   [Desarrollo](#desarrollo)
-   [Resultados](#resultados)
-   [Conclusiones](#conclusiones)
-   [Trabajo Futuro](#trabajo-futuro)

</div>

---

<div class="twocols center-grid">

# Contexto y problemática

-   [Computación a gran escala](#computación-a-gran-escala)
-   [Crecimiento y costo](#crecimiento-y-costo)
-   [Computación Autonómica](#computación-autonómica)
-   [Sistemas IoT](#sistemas-iot)
-   [Smart Campus UIS](#smart-campus-uis)
-   [Visión General](#vision-general)

</div>

---

<!-- _header: <h1 id="computación-a-gran-escala"> Computación a Gran Escala </h1> -->

<div class="twocols center-grid">
<div class="col center">

Orientada al manejo de grandes cantidades de datos y problemas de alta complejidad.

</div>
<div class="col">

-   Surge por el interés en tomas de decisiones apoyadas por computadoras, machine-learning, simulaciones, etc.
-   Tiene un gran costo monetario debido al hardware e infraestructura requerida.
-   Incluye computación distribuida, cloud computing, etc.

</div>
<div>

<!--
La computación a gran escala es, en esencia, sistemas computacionales con el objetivo de procesar muchos datos y solucionar problemas complejos.

Estos, por su gran capacidad de recursos de cómputo, han sido llamados super-computadoras y tienen a tener un gran costo. Y dadas las limitaciones de algunas compañías en adquirir este tipo de soluciones, han surgido diferentes acercamientos a esta gran escala. Entre ellos, está la computación distribuida y cloud computing.

Esto sin embargo, presenta 2 problemas. El crecimiento y el costo.

-->

---

<!-- _header: <h1 id="crecimiento-y-costo"> Crecimiento y costo </h1> -->

<div class="col center">

Los sistemas de gran escala, crecen. Esto es costoso y complicado de manejar.

![width:800](assets/GoogleNetwork.png)

</div>

<!--
El mantener sistemas distribuidos por todo el mundo, no es algo particularmente barato. Ni en términos de dinero, ni en términos de personal.

Aquí tenemos como ejemplo la infraestructura de red de Google, esta está compuesta por casi 8000 nodos encargados del manejo de todo el tráfico de datos usados por los usuarios.

Manejar este tipo de infraestructuras, no es una tarea particularmente sencilla. Hay varias maneras de solucionar esto, y una de ellas es la computación autonómica.

-->

---

<!-- _header: <h1 id="computación-autonómica"> Computación Autonómica </h1> -->

<div class="twocols center-grid">
<div class="col">

-   Auto-conocimiento
-   Auto-configuración
-   Auto-optimización
-   Auto-sanación
-   Auto-protección
-   Auto-conciencia

</div>
<div class="col center">

![width:750](assets/Mape-k%20Alt.png)
Ciclo de control MAPE-K

</div>
</div>

<!--
Inicialmente planteada por IBM a inicios de los 2000, la computación autonómica busca el dotar a los sistemas de computación con propiedades de autogestión las cuales pueda modificar su estado en búsqueda de manejarse a sí mismo.

Las principales propiedades que un sistema autonómico debe tener son:

- Auto-conocimiento: habilidad de conocer su estado actual, las interacciones del sistema.
- Auto-configuración: capacidad de re-configurarse frente a los constantes cambios en el entorno.
- Auto-optimización: búsqueda constante de optimizar el funcionamiento de sí mismo.
- Auto-sanación: aptitud de restaurar el sistema en el caso de que se presenten fallas.
- Auto-protección: facultad de protegerse a sí mismo de ataques externos.
- Auto-conciencia: posibilidad de conocer el ambiente en el que el sistema se encuentra.

El objetivo de estas propiedades autonómicas es reducir la complejidad de manejar este tipo de sistemas, ayudando así a los administradores de sistemas.

Ahora, uno de los campos en donde se pueden aplicar estos conceptos, es en los sistemas IoT.

-->

---

<!-- _header: <h1 id="sistemas-iot"> Sistemas IoT </h1> -->

<div class="twocols center-grid">
<div class="col">

![width:450](assets/IoTLogo.png)

</div>
<div class="col center">

"La Internet de las cosas (IoT) describe la red de objetos físicos ("cosas") que llevan incorporados sensores, software y otras tecnologías con el fin de conectarse e intercambiar datos con otros dispositivos y sistemas a través de Internet"
(Oracle, s.f.)

</div>
</div>

<!--
Los sistemas IoT, son descritos por Oracle como redes de objetos físicos con sensores y actuadores. Estos son usados para diversas tareas las cuales van desde el control de dispositivos como luces hasta monitoreo ambiental.

Para efectos de esta presentación, nos interesa principalmente esto último. Dentro de las aplicaciones que se tienen dentro del monitoreo, es el desarrollo de los llamados Smart Campus.
-->

---

<!-- _header: <h1 id="smart-campus-uis"> Smart Campus UIS </h1> -->

<div class="twocols center-grid">

<div class="col center">

Los Smart Campus son versiones
en miniatura de las Smart Cities.

Smart Campus UIS es una implementación realizada aquí de este concepto.

</div>

<div class="col">

![](assets/SmartCampus.png)

</div>

</div>

<!--
Los smart-palabra, son sistemas IoT con el fin de realizar el control y monitoreo de un area geográfica dada. Estas son conocidas dependiendo del tamaño de área en las que estén presentes.

Aquí en la UIS, se está llevando acabo el desarrollo de una plataforma de este estilo la cual permita realizar despliegues de diferentes sistemas IoT con la realización de diferentes aplicaciones. Entre ellas, como se había nombrado antes, el monitoreo ambiental.

Esto implica el uso de una gran cantidad de dispositivos, distribuidos geográficamente, encargados de la recolección de los diferentes tipos de datos. Esto, a su vez, implica que, para que las aplicaciones registradas en la plataforma funcionen de manera adecuada, se requiere del manejo de todos los dispositivos, que a la larga, van a ser muchos.

Ahora, partiendo de esto, se planteó el dotar a Smart Campus UIS, con propiedades autonómicas. Veamos una visión general del proyecto.
-->

---

<!-- _header: <h1 id="vision-general"> Visión General </h1> -->

<div class="center">

![width:950](assets/VisionGeneral.png)

</div>

<!--

La visión general del proyecto es la siguiente:

Se quería que los usuarios/administradores del sistema, tuvieran la capacidad de definir un estado de referencia para una aplicación. Esta, así mismo, sería tomada como parte de la base de conocimiento, y usada para evaluar el estado de la aplicación observada.

A partir de esta evaluación, se tendrían que formular las acciones a tomar con el fin de acercar el estado observado hacia el estado objetivo. Estas acciones, finalmente, serían ejecutadas sobre Smart Campus UIS, dando como resultado cambios en el estado observado.

Como podemos ver, tenemos algo bastante similar al planteamiento realizado inicialmente por IBM. Para dotar a Smart Campus UIS de estas propiedades autonómicas, será necesario tener:

0. Una manera para que los usuarios puedan declarar los estados de referencia
1. Una manera de monitorear la actividad de los sensores que están recolectando información
2. Una manera de evaluar el estado de la aplicación respecto a su estado de referencia definido
3. Una manera de planear las acciones a realizar respecto a la evaluación realizada
4. Una manera de ejecutar las acciones planeadas sobre la plataforma

-->

---

<div class="twocols center-grid">

# Objetivos

-   [Objetivo General](#objetivo-general)
-   [Objetivos Específicos](#objetivos-específicos)

---

<!-- _header: <h1 id="objetivo-general"> Objetivo General </h1> -->

-   Diseñar un conjunto de mecanismos autonómicos para permitir la adaptación de la Arquitectura Software IoT respecto a un modelo objetivo en la plataforma Smart Campus UIS

---

<!-- _header: <h1 id="objetivos-específicos"> Objetivos Específicos </h1> -->

<div class="twocols">

<div class="col">

1.  Proponer una notación (lenguaje) para describir una arquitectura objetivo de un sistema software IoT.
2.  Diseñar un mecanismo para determinar las diferencias existentes entre una arquitectura actual en ejecución y una arquitectura objetivo especificada.

</div>

<div class="col">

3.  Diseñar un conjunto de mecanismos de adaptación que permitan disminuir las diferencias entre la arquitectura actual y la arquitectura objetivo.
4.  Evaluar la implementación realizada a partir de un conjunto de pruebas con el fin de establecer la efectividad de los mecanismos usados.

</div>

---

<div class="twocols center-grid">

# Metodología

-   [Prototipado Iterativo](#prototipado-iterativo)

---

<!-- _header: <h1 id="prototipado-iterativo"> Prototipado Iterativo </h1> -->

<div class="col center">

![width:1000](assets/Metodología.png)

</div>

---

<div class="twocols center-grid">

# Desarrollo

-   [Ambientación Conceptual Y tecnológica](#ambientación-conceptual-y-tecnológica)
-   [Definición de la notación de la arquitectura](#definición-de-la-notación-de-la-arquitectura)
-   [Mecanismos de descripción](#mecanismos-de-descripción)
-   [Mecanismos de adaptación](#mecanismos-de-adaptación)
-   [Validación de resultados](#validación-de-resultados)

---

<div class="twocols center-grid">
<div class="col">

# Ambientación Conceptual Y tecnológica

</div>
<div class="col">

-   [Criterios de selección](#criterios-de-selección)
-   [Búsqueda de alternativas](#búsqueda-de-alternativas)

</div>

</div>

<!--

Con esta ambientación conceptual, se buscaba el realizar identificar una notación que se pudiera usar para poder realizar el modelado de las aplicaciones que se estarían desarrollando sobre Smart Campus UIS.

A partir de esto, se definieron unos criterios por los cuales se evaluaran cada unas de las alternativas identificadas durante las consultas a literatura.

-->

---

<!-- _header: <h1 id="criterios-de-selección"> Criterios de selección </h1> -->

Requisitos

1. Describir la arquitectura de un sistema IoT
2. Permitir ubicar los componentes en una ubicación geográfica
3. Habilitar el modelado de los componentes a nivel de sus entradas
4. Poder el establecer el estado de los componentes

Nice to have

5. Modelar el comportamiento de sus componentes
6. Permitir el exportar el modelo de manera gráfica

<!--



-->

---

<!-- _header: <h1 id="búsqueda-de-alternativas"> Búsqueda de alternativas </h1> -->

<!-- <div class="twocols center-grid"> -->

<div class="col center">

Se buscaron diferentes LDAs diseñados para IoT, pero
no se adecuaban a las necesidades del proyecto.

</div>

<div class="col center">

<table style="margin: 0px auto;" class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th></th><th>MontiThings</th><th>Eclipse Mita</th><th>SysML4IoT</th><th>ThingML</th><th>IoT-DDL</th></tr></thead><tbody>
 <tr><td>C1</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td></tr>
 <tr><td>C2</td><td>✗</td><td>✗</td><td>✗</td><td>✗</td><td>✗</td></tr>
 <tr><td>C3</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td></tr>
 <tr><td>C4</td><td>✓</td><td>✓</td><td>✗</td><td>✓</td><td>✗</td></tr>
 <tr><td>C5</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td><td>✗</td></tr>
 <tr><td>C6</td><td>✗</td><td>✗</td><td>✗</td><td>✓</td><td>✗</td></tr>
</tbody></table>

</div>
</div>

---

<!-- <!-- _header: <h1 id="búsqueda-de-alternativas"> Búsqueda de alternativas </h1>

<div class="center">

<table style="margin: 0px auto; ;" class="tableizer-table">
<thead><tr class="tableizer-firstrow"><th></th><th>MontiThings</th><th>Eclipse Mita</th><th>SysML4IoT</th><th>ThingML</th><th>IoT-DDL</th></tr></thead><tbody>
 <tr><td>C1</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td></tr>
 <tr><td>C2</td><td>✗</td><td>✗</td><td>✗</td><td>✗</td><td>✗</td></tr>
 <tr><td>C3</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td></tr>
 <tr><td>C4</td><td>✓</td><td>✓</td><td>✓</td><td>✓</td><td>✗</td></tr>
 <tr><td>C5</td><td>✓</td><td>✓</td><td>✗</td><td>✓</td><td>✗</td></tr>
 <tr><td>C6</td><td>✗</td><td>✗</td><td>✗</td><td>✓</td><td>✗</td></tr>
</tbody></table>
</div>
</div>

--- -->

<div class="twocols center-grid">
<div class="col center">

# Definición de la notación de la arquitectura

</div>

<div class="col">

-   [Un nuevo modelo](#un-nuevo-modelo)
-   [Sintaxis de la notación](#sintaxis-de-la-notación)
-   [Validando aplicaciones](#validando-aplicaciones)

</div>
</div>

---

<!-- _header: <h1 id="un-nuevo-modelo"> Un nuevo modelo </h1> -->

<div class="col center">

![width:1200](assets/HenryModelo%20Alt.png)

</div>

---

<!-- _header: <h1> Un nuevo modelo </h1> -->

<div class="col center">

![width:800](assets/Metamodel%20B%20Alt.png)

</div>

---

<!-- _header: <h1 id="sintaxis-de-la-notación"> Sintaxis de la notación </h1> -->

<div class="twocols center-grid">
<div class="col center">

![](assets/Railroad%20Complete.png)

</div>

<div class="col">

![width:480](assets/ModelYaml.png)

</div>
</div>

---

<!-- _header: <h1 id="validando-aplicaciones"> Validando aplicaciones </h1> -->

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

<div class="twocols center-grid">

<div class="col center">

# Mecanismos de descripción

</div>
<div class="col">

-   [Monitorear](#monitorear)
-   [Centralizando datos](#centralizando-datos)
-   [Analizar](#analizar)
-   [Evaluando el estado](#evaluando-el-estado)

</div>

</div>

---

# Monitorear

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Centralizando datos

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Analizar

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Evaluando el estado

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

<div class="twocols center-grid">

<div class="col center">

# Mecanismos de adaptación

</div>

<div class="col">

-   [Identificando problemas](#identificando-problemas)
-   [Definiendo acciones](#definiendo-acciones)
-   [Planear](#planear)
-   [Actuar](#actuar)

</div>

</div>

---

# Identificando problemas

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Definiendo acciones

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Planear

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Actuar

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

<div class="twocols center-grid">

<div class="col center">

# Validación de resultados

</div>

<div class="col">

-   [Condiciones y banco de pruebas](#condiciones-y-banco-de-pruebas)
-   [Escenario A](#escenario-a)
-   [Escenario B](#escenario-b)

</div>
</div>

---

# Condiciones y banco de pruebas

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Escenario A

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Escenario B

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

<div class="twocols center-grid">

# Conclusiones

---

<div class="twocols center-grid">

# Trabajo Futuro

-   [Interfaces gráficas](#interfaces-gráficas)
-   [Estadísticas](#estadísticas)

---

# Interfaces gráficas

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Estadísticas

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Preguntas
