---
layout: post
title:  "[ES] Ray Tracing - Distribuido"
date:   2017-09-19 21:07:00
categories: jekyll
---

## [ES] Ray Tracing - Distribuido

Hoy se analizará un algoritmo de renderización llamado Ray Tracing, que consiste en obtener una imagen de un escenario desde un punto de vista, como si el ojo fuera un foco, un foco de de rayos que chocaran con cualquier objeto del escenario hasta una fuente de luz, o tambien cualquier otro lugar que no tenga ningun objeto. Y de ahí

![Ray Tracing](/assets/800px-Ray_trace_diagram.svg.png)

Como se puede ver, se logra captar un instante del escenario. Entonces si queremos captar una representación de un escenario con objetos en movimiento no puede ser posible con lo que ya sabemos.

![Distributed Ray Tracing](/assets/blurr.jpg)

Para lograr esto, se necesita de emplear la técnica de Ray Tracing Distribuido. Esto no tiene que ver con sistemas distribuidos o algo relacionado a mejorar el rendimiento de esta técnica, ya que sabemos que es una de las técnicas más costosas en terminos de rendimiento.

El ray tracing, como se ve en la primera figura, consiste en lanzar un rayo para representar un punto del escenario, es un rayo sin área, generando una imagen perfecta del escenario para muchos generando una imagen irreal. Para poder quitar este grado de perfección no consideraremos un rayo generado para un punto, si no un promedio de la información que se tiene de diferentes rayos en un área, para un punto determinado.

![Distributed Tecnique](/assets/img272.gif)

Logrando así una imagen en movimiento, si el área de los rayos es muy grande, o una imagen más "real" si se emplea con un área muy pequeño, por ejemplo en vez de una sombra con bordes bien definidos, podemos ver una figura con una sombra penumbra, algo que ocurre en la vida real.

![Penumbra Example](/assets/penumbra.png)

Estos son solo unos de los posibles efectos que se pueden lograr con el método del Ray Tracing Distribuido.
