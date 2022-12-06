---
title: "Framework para la determinación del nivel de autonomía de un sistema software"
output: pdf_document
bibliography: bibliography.bib
csl: apa.csl
---

# Mecanismos De Adaptación De Arquitectura Software Para Smart Campus UIS

## Objetivo General

-   Implementar mecanismos que permitan la adaptación de una arquitectura Software IoT respecto a un modelo objetivo.

Palabras Clave
: Computación Autonómica, Arquitectura de Software, Self-Configuration, IoT, Open Source

## Justificación

La complejidad de los sistemas software ha ido en aumento. A medida que se hace la transición a arquitecturas orientadas a microservicios [@forrester_research_2019]; la computación distribuida es más común gracias a las soluciones _cloud_ [@the_cloud_in_2021] y la computación embebida se hace más presente [@deichmann_doll_klein_mühlreiter_stein_2022, p. 3]; la administración y gestión de estos requiere de una mayor cantidad de recursos en términos técnicos y humanos con el fin de mantenerlos en los estados más óptimos respecto a los requerimientos del negocio. La búsqueda de reducir o abstraer la complejidad de la gerencia de estos sistemas se ha convertido en una necesidad [@lalanda_diaconescu_mccann_2014, pp. 23-24].

Esta necesidad, así mismo, se presenta en los campos del Internet de las Cosas (IoT). Es en esta área de la computación embebida donde, debido a las cambiantes condiciones del mundo real, cambian de manera constante la arquitectura de estos sistemas de software. Partiendo de esto, una de las posibles soluciones se encuentra en la computación autonómica. Desde este enfoque, los sistemas software presentan auto-configuración, auto-optimización, auto-sanación y auto-protección, características que permiten la auto-gestión del sistema [@evaluation_2004]. De esta manera el trabajo de administrar los componentes, con el fin mantener la arquitectura, es responsabilidad del mismo.

Siendo así, tenemos el caso de Smart Campus UIS, una plataforma de IoT de la Universidad Industrial de Santander. Esta ha realizado implementaciones parciales de una arquitectura autonómica con capacidad de auto-describirse [@henry_2020], sin embargo no presenta mecanismos de auto-configuración, o adaptación, con los cuales realizar cambios dentro de la arquitectura.

Partiendo de esto, se propone trabajar en el desarrollo de mecanismos de adaptación de arquitectura para Smart Campus UIS. De esta manera, tomando en cuenta una arquitectura objetivo, o de referencia, la plataforma tendrá la posibilidad de realizar los cambios correspondientes a si misma con el fin de acercase lo más posible a esta.

<div style="page-break-after: always;"></div>

## References
