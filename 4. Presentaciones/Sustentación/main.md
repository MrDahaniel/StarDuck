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
            <img src="assets/UISLogo.png" width="30%" />
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
-   [Visión General](#visión-general)
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
-   [Crecimiento](#crecimiento)
-   [Costo](#costo)
-   [Computación Autonómica](#computación-autonómica)
<!-- -   [Smart Campus UIS](#smart-campus-uis) -->

</div>

---

# Computación a Gran Escala

<div class="twocols center-grid">

<div class="col">

</div>

<div class="col">

</div>

<div>

---

# Crecimiento

<div class="twocols center-grid">

<div class="col">

</div>

<div class="col">

</div>

<div>

---

# Costo

<div class="twocols center-grid">

<div>

---

# Computación Autonómica

<div class="twocols center-grid">

<div class="col">

</div>

</div>

---

# Sistemas IoT

<div class="twocols center-grid">

<div class="col">

</div>

</div>

---

# Smart Campus UIS

<div class="twocols center-grid">

<div class="col">

</div>

</div>

---

<div class="twocols center-grid">

<div class="col center">

# Visión General

</div>

<div class="col">

</div>

<div>

---

<div class="twocols center-grid">

# Objetivos

-   [Objetivo General](#objetivo-general)
-   [Objetivos Específicos](#objetivos-específicos)

---

<divdiv>

# Objetivo General

-   Diseñar un conjunto de mecanismos autonómicos para permitir la adaptación de la Arquitectura Software IoT respecto a un modelo objetivo en la plataforma Smart Campus UIS

---

# Objetivos Específicos

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

# Prototipado Iterativo

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

<div class="col center">

# Ambientación conceptual y tecnológica

</div>

<div class="col">

-   [Criterios de selección](#criterios-de-selección)
-   [Búsqueda de alternativas](#búsqueda-de-alternativas)

</div>

</div>

---

# Criterios de selección

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Búsqueda de alternativas

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

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

# Un nuevo modelo

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Sintaxis de la notación

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Validando aplicaciones

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

# Resultados

-   [Resultados Escenario A](#resultados-escenario-a)
-   [Resultados Escenario B](#resultados-escenario-b)

---

# Resultados Escenario A

<div class="twocols center-grid">
<div class="col center">

</div>

<div class="col">

</div>
</div>

---

# Resultados Escenario B

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

# Fin
