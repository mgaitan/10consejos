:title: 10 consejos para un mejor software (de) científico(s)
:data-transition-duration: 500
:css: slides.css

-----

:id: portada

*****************************************************************
      10 consejos para un mejor software (de) científico(s)
*****************************************************************


.. image:: img/scipycon.png


.. raw:: html

    <center>por Martín Gaitán</center>

.. image:: img/twitter.png
   :align: center

--------

Quién soy
---------

- Compañero de Nati, Zamba y Minou
- Hincha de Boca y del dulce de leche
- Ingeniero en Computación (UNC)
- Pythonista desde 2007
- Emprendedor en @Phasety
- Trabajo con químicos que programan

.. image:: img/But-why-meme.png
   :align: center

---------

Sobre esta charla
-----------------

.. epigraph::

    De un hombre de software, a los hombres y mujeres
    de la academia, con respeto y cariño.

    -- yo

.. tip:: Also Known As:

    catarsis | solidaridad | pedido de auxilio

----------


En general ¿qué hace el software (de) científico(s)?
----------------------------------------------------

- Herramienta de **exploración** de problemas
- Nicho **muy** específico
- Modelado numérico / simulación
- Manipulación de datos
- Gráficos

------

Problemas comunes
-----------------

- Ciclo prueba-error-corrección lento
- Documentación escasa
- Múltiples herramientas para lograr un resultado
- Limitaciones de scope del lenguaje ("no escala")
- ¿Pirata yo?

----

Y sobre todo...
---------------

**Inercia académica**

.. epigraph::

    No sigas las huellas de tus maestros.
    Busca lo que ellos buscaron.

    -- Matsuo Bashō

------

Consejo 1:
----------

Pare de sufrir
---------------

| Use **Python** (y su *stack* científico)

.. image:: img/sufrir.jpg

.. note:: Python es una lenguaje versátil,
          interactivo, simple y documentado

-----

.. image:: img/python-powered.png
   :width: 15%


| (muy) Fácil de aprender
| con sintáxis legible y expresiva
| Dinámico, multiparadigma, tipado fuerte
| Interpretado, **Interactivo**, Extensible
| Multiplataforma, Libre y Gratis
| Gran documentación y bibliotecas
| y una maravillosa **comunidad de usuarios**

| **Ideal para ciencias e ingenierías**


------

#EsPregunta
-----------

¿Les cobran por vocal?
----------------------

.. code-block:: fortran

   DIMENSION FGx(2),FGy(2),FGTx(2),FGTy(2),FGVx(2),FGVy(2)
   DIMENSION DFGNx(2,2),DFGNy(2,2)
   DIMENSION DPDNx(2),DPDNy(2),XOLD(5),OLD(5)

.. image:: img/sms.jpg
   :align: center

------

Consejo 2:
----------

Programe para humanos
---------------------

| Especialmente para Ud mismo, luego del fin de semana largo.

.. epigraph::

    Programs must be written for people to read, and only incidentally for machines to execute.

    -- Abelson & Sussman, Structure and Interpretation of Computer Programs

-----

Ésta la conozco
---------------

.. code:: html

    From: Juan <subdito@todavianosegit.edu>
    To: Dr. God <sersuperior@todavianosegit.edu>
    Subject: Trabajo

    Doctor, acá le mando el zip con la última versión
    que incluye mi parte del paper

    ----

.. code:: html

    From: Dr. God <sersuperior@todavianosegit.edu>
    To: Juan <subdito@todavianosegit.edu>
    Subject: Re: Trabajo

    Estimado Juan me olvidé de avisarle que María modificó esa parte
    y cambiaron los parámetros de la función.
    Por favor, revise el último código que le adjunto.

------

Ésta también
------------

.. image:: img/copies.png
   :align: center


-------

Consejo 3:
-----------

Usá control de versiones
------------------------

| Aprendé `GIT <http://nyuccl.org/pages/GitTutorial/>`_

- Cambios incrementales
- Trabajo **colaborativo**: qué, quién, cuándo (para qué)
- Branchs: libertad para experimentar
- Backups
- Dropbox **no es una solución**

-----

Ay, ¡los inputs!
-----------------

.. code-block::

    1
    0 0
    CARBON DIOXIDE
    304.21  73.83  0.22362  0.114197
    3.7042  0.029682  0.823228
    ETHANE
    305.32  48.72  0.09949  0.173685
    5.6544  0.045144  0.634870
    0.0
    0.0
    200.0

--------

Consejo 4:
-----------

La interactividad es poder!
---------------------------

| "API programable FTW!"


Si **no queda otra** (configuración):

- Usá estándares: por ejemplo **json** o YAML.
- Dale semántica a los datos

.. epigraph::

    "Simple is better than complex.
     Explicit is better than implicit"

    -- The Zen of Python


--------

Efecto ``model2param.for``
---------------------------

| El código se copia fácil. Los bugs también.

.. image:: img/copy_paste.jpg
   :align: center

-----

Consejo 5:
----------

Don't Repeat Yourself
---------------------

.. image:: img/dry.jpg
   :align:  center


-------

Bienvenidos al código (de un) científico
----------------------------------------

.. image:: img/tank.jpg
   :align: center
   :width: 80%


------

Consejo 6:
-----------

¡Modularizá!
------------

.. image:: img/legos.jpg
   :align: center

------

La mochila de los parámetros
----------------------------

.. code-block:: fortran

        CALL SUP(x1,y1,x2,y2, sup_out)
        CALL PER(x1,y1,x2,y2, per_out)

----

Consejo 7:
----------

Programá tan alto como puedas
------------------------------

| buscá efectividad

.. code-block:: python

    class Rectangulo(object):

        def __init__(self, punto1, prunto2):
            self.punto1 = punto1
            self.punto2 = punto2

        def superficie(self):
            return abs((self.punto1.x - self.punto2.x) *
                       (self.punto1.y - self.punto2.y))

        def perimetro(self):
            ...

----------

¡A tu grandeza, Newton!
-----------------------

.. code-block::

    subroutine mi_newton(f, fp, x0, x, iters, debug)

        !esta funcion implementa el metodo de Newton para
        !encontrar el 0 de una función f

Really?

------------

Consejo 8:
----------

No reinventes la rueda
-----------------------

.. epigraph::

    If I have seen further it is by standing
    on the shoulders of giants.

    -- Sir Isaac Newton


.. tip:: Tip: ``scipy.optimize.newton``

----

Hacer software no es sólo escribir código
-----------------------------------------

| Comentarios, documentos, diagramas.
| son bienvenidos

**Atenti:**

| no se trata de describir el código que podemos leer.

------

Consejo 9:
----------

documentar!
------------

.. image:: img/document.jpg
   :align: center

.. note:: ipython notebook es genial.

----

Probar programas es agotador
-----------------------------

.. image:: img/trabajo.jpg
   :align: center

----

Consejo 10:
-----------

que la computadora trabaje por vos
-----------------------------------

| **¡Unittests!**

| (programitas que prueban (partes) de programas)

.. code-block::

    def test_suma():
        assert suma(2, 2) == 4

-----

Los tests te dan seguridad
--------------------------

| Mejorar sabiendo que funciona


.. image:: img/escalada.gif
   :align: center


-----

Una más ?
-------------

------

Intentá siempre,
------------------

siempre,
--------

aprender más
------------

| Por lo tanto

------

Consejo de yapa:
----------------

vení mañana
------------


| Jueves y viernes 10hs

| **Tutorial de introducción a Python Científico**


.. image:: img/scipycon.png


-----


Muchas gracias
--------------


.. image:: img/twitter.png
   :align: center