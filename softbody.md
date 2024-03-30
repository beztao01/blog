---
layout: default
---

## Soft Body

### Introducción 

La simulación de cuerpo blando se utiliza para simular objetos deformables suaves. Fue diseñado principalmente para agregar movimiento secundario a la animación, como movimientos de partes del cuerpo de un personaje en movimiento.

También funciona para simular objetos blandos más generales que se doblan, deforman y reaccionan a fuerzas como la gravedad y el viento, o chocan con otros objetos.

Si bien puede simular telas y otros tipos rígidos de objetos deformables hasta cierto punto, la simulación de telas puede hacerlo mejor con un solucionador diseñado específicamente para este propósito.

La simulación funciona combinando la animación existente en el objeto con las fuerzas que actúan sobre él. Hay fuerzas exteriores como la gravedad o campos de fuerza y ​​fuerzas interiores que mantienen unidos los vértices. De esta manera puedes simular las formas que adoptaría un objeto en la realidad si tuviera volumen, estuviera lleno de algo y sobre él actuaran fuerzas reales.

Los cuerpos blandos pueden interactuar con otros objetos mediante colisión. Pueden interactuar consigo mismos a través de la autocolisión.

El resultado de la simulación de un cuerpo blando se puede convertir en un objeto estático. También puede editar la simulación, es decir, editar resultados intermedios y ejecutar la simulación desde allí.

Escenarios típicos para el uso de cuerpos blandos.

(imagen de banderola)

Los cuerpos blandos son muy adecuados para:

    • Mueve los personajes en movimiento.
    • Objetos elásticos y deformables fabricados con materiales como caucho o gelatina.
    • Ramas de árboles moviéndose con el viento, cuerdas balanceándose y cosas por el estilo.
    • Banderas, mangas anchas, cojines u otros tejidos sencillos que reaccionen a las fuerzas.

Los siguientes vídeos pueden darte más ideas:
(dos videos sugeridos por Blender foundation)


### Creando un Soft Body

La simulación de cuerpo blando funciona para todos los objetos que tienen vértices o puntos de control (mallas, curvas, superficies y celosías lattices texto original).

Para agregar una simulación de cuerpo blando a un objeto, vaya a la pestaña Física en Propiedades y active el botón Cuerpo blando. Para obtener una referencia de todas las configuraciones, consulte esta página. ANCLA

Una simulación de cuerpo blando se inicia reproduciendo la animación con alt A y se detiene la simulación con Alt-A  o Esc


### Interacción en tiempo real 

Para trabajar con una simulación de cuerpo blando, le resultará útil utilizar el editor de línea de tiempo. Puede cambiar entre fotogramas y la simulación siempre se mostrará en el estado real. Puede interactuar en tiempo real con la simulación, por ejemplo, moviendo objetos en colisión o sacudiendo un objeto de cuerpo blando.

Luego puede seleccionar el objeto de cuerpo blando mientras ejecuta la simulación y aplicar el modificador en la pestaña Modificadores de Propiedades. Esto hace que la deformación sea permanente.

### Consejos 

Los cuerpos blandos funcionan especialmente bien si los objetos tienen una distribución de vértices uniforme. Necesitas suficientes vértices para buenas colisiones. Cambias la deformación (la rigidez) si agregas más vértices en una región determinada.

El cálculo de las colisiones puede llevar mucho tiempo. Si algo no es visible, ¿para qué calcularlo?

Para acelerar el cálculo de la colisión, suele ser útil colisionar con un objeto adicional, más simple, invisible y algo más grande.

Utilice cuerpos blandos sólo donde tenga sentido. Si intentas cubrir una malla corporal con un trozo de tela ajustado y animas únicamente con un cuerpo suave, no tendrás éxito. Es posible que se active la autocolisión del vello corporal suave, pero ese es un camino que debes recorrer solo. Nos ocuparemos de las colisiones en detalle más adelante.

Intente utilizar un cuerpo suave Lattice o Curve Guide en lugar del objeto en sí. Esto puede ser magnitudes más rápidas.

Ajustes 
Referencia

Grupo :
Física ‣ Cuerpo Blando

#### Colección de colisiones
Si se establece, el cuerpo blando colisiona con objetos de la colección, en lugar de utilizar objetos que están en la misma capa.

Objeto
Fricción
La fricción del medio circundante. Generalmente la fricción amortigua un movimiento. Cuanto mayor es la fricción, más viscoso es el medio. La fricción siempre aparece cuando un vértice se mueve en relación con el medio que lo rodea.

Masa
Valor de masa para los vértices. Una masa más grande ralentiza la aceleración, excepto en el caso de la gravedad, donde el movimiento es constante independientemente de la masa. Una masa mayor significa una mayor inercia, por lo que frenar con una carrocería blanda también es más difícil.

Punto de control
Puede pintar pesos y utilizar un grupo de vértices específico para valores de masa.

Simulación
Velocidad
Puede controlar la sincronización interna del sistema de cuerpo blando con este valor. Establece la correlación entre la velocidad de cuadros y el tempo de la simulación. Un cuerpo en caída libre debe recorrer una distancia de unos cinco metros en un segundo y viajar a una velocidad de diez metros por segundo.

Puede ajustar la escala de su escena y simulación con esta correlación. Si renderiza con 25 fotogramas por segundo, deberá configurar la Velocidad en 1,3.

Cache

Referencia
Grupo :
Física ‣ Cuerpo blando ‣ Caché
Las simulaciones de física de Soft Body utilizan un sistema unificado para el almacenamiento en caché y el horneado. Consulte la documentación de Particle Cache y General Baking como referencia.

Meta
Meta 
Referencia

Grupo :
Física ‣ Cuerpo Blando ‣ Meta

Habilitar esto le dice a Blender que use el movimiento de las animaciones (curvas F, armaduras, padres, celosías, etc.) en la simulación. El "objetivo" es la posición final deseada para los vértices según esta animación.

Ver fuerzas exteriores para más detalles.

Grupo de vértices
Utilice un grupo de vértices para permitir ponderaciones de objetivos por vértice (multiplicadas por el objetivo predeterminado ).

Ajustes 
Rigidez
La rigidez del resorte para Goal . Un valor bajo crea resortes muy débiles (una “unión” más flexible a la portería), un valor alto crea un resorte fuerte (una “unión” más rígida a la portería).

Mojadura
El coeficiente de fricción para Goal . Los valores más altos amortiguan el efecto del resorte (pequeña sacudida) y el movimiento pronto finalizará.

Fortalezas 
Por defecto
Peso/fuerza objetivo para todos los vértices cuando no se asigna ningún grupo de vértices . Si utiliza un grupo de vértices, el peso de un vértice define su objetivo.

Mínimo máximo
Cuando usa un grupo de vértices, puede usar Mínimo y Máximo para ajustar (fijar) los valores de peso. El peso de vértice más bajo se convertirá en Mínimo , el valor más alto se convertirá en Máximo .

Ajustes
Fortalezas
Bordes
Bordes 
Referencia

Grupo :
Física ‣ Cuerpo Blando ‣ Bordes

Permita que los bordes de un objeto de malla actúen como resortes. Ver fuerzas interiores .

muelles
Utilice un grupo de vértices específico para los valores de resistencia del resorte.

Jalar
La rigidez del resorte para los bordes (cuánto se permite que los bordes se estiren). Un valor bajo significa resortes muy débiles (un material muy elástico), un valor alto es un resorte fuerte (un material más rígido) que resiste ser arrancado.

Un valor de 0,5 es látex, 0,9 es como un suéter, 0,999 es una servilleta o cuero muy almidonado. La simulación de cuerpo blando tiende a volverse inestable si usa un valor de 0,999, por lo que debería reducir este valor un poco si eso sucede.

Empujar
Cuánto resiste el cuerpo blando a ser aplastado, como un resorte de compresión. Valores bajos para tela, valores altos para objetos inflados y material rígido.

Húmedo
La fricción para los resortes de borde. Los valores altos (máximo de 50) amortiguan el efecto Push / Pull y calman la tela.

Plasticidad
Deformación permanente del objeto después de una colisión. Los vértices toman una nueva posición sin aplicar el modificador.

Doblar
Esta opción crea conexiones virtuales entre un vértice y los vértices conectados a sus vecinos. Esto incluye bordes diagonales. La amortiguación también se aplica a estas conexiones.

Longitud
Los bordes pueden encogerse o hincharse. Este valor se da en porcentaje, 0 desactiva esta función. 100% significa que no hay cambios, el cuerpo mantiene el 100% de su tamaño.

Colisión
Borde
Comprueba si hay bordes de la malla del cuerpo blando que colisionan.

Rostro
Comprueba si alguna parte de la cara de la malla del cuerpo blando colisiona (lo cual requiere un uso computacional intensivo). Si bien Face habilitado puede resolver errores de colisión, no parece haber ninguna configuración de amortiguación para ello. Por lo tanto, las partes del objeto de cuerpo blando cerca de una malla de colisión tienden a "temblar" a medida que rebotan y caen hacia atrás, incluso cuando no hay movimiento de ninguna malla. La colisión de borde tiene amortiguación, por lo que se puede controlar, pero el valor de amortiguación de deflexión en un objeto de colisión no parece afectar la colisión de cara.


Aerodinámica
erodinámica 
Fuerza de los medios circundantes. Ver fuerzas exteriores para más detalles.

Tipo
Simple :
Los bordes reciben una fuerza de arrastre de los medios circundantes.

Fuerza de elevación :
Los bordes reciben una fuerza de elevación cuando pasan a través del medio circundante.

Factor
Cuánta fuerza aerodinámica usar. Pruebe con un valor de 30 al principio.

Rigidez 
Para caras cuádruples, los bordes diagonales se utilizan como resortes. Esto evita que las caras cuádruples colapsen por completo en caso de colisión (lo que harían de otra manera).

Cortar
Rigidez de los resortes virtuales creados para caras cuádruples.

Rigidez
Auto colisión

Autocolisión 
Referencia

Grupo :
Física ‣ Cuerpo blando ‣ Autocolisión

Nota

La autocolisión solo funciona si ha activado Usar bordes .

Cuando está habilitado, le permite controlar cómo Blender evitará que el cuerpo blando se cruce consigo mismo. Cada vértice está rodeado por una bola virtual elástica. Los vértices no podrán penetrar las bolas de otros vértices. Si quieres un buen resultado es posible que tengas que ajustar el tamaño de estas bolas. Normalmente funciona bastante bien con las opciones predeterminadas.

Tipo de cálculo
Manual :
El tamaño de la bola establece directamente el tamaño de la bola.

Promedio :
La longitud promedio de todos los bordes unidos al vértice se calcula y luego se multiplica con la configuración Tamaño de bola . Funciona bien con vértices distribuidos uniformemente.

Mínimo/Máximo :
El tamaño de la bola es tan grande como la longitud del resorte más pequeña/más grande del vértice multiplicada por el tamaño de la bola .

Promedio mínimo máximo :
Tamaño = ((Min + Max)/2) × Tamaño de la bola .

Tamaño de la bola
Fracción de la longitud de los bordes adjuntos. La longitud del borde se calcula en función del algoritmo elegido. Este ajuste es el factor que se multiplica por la longitud del resorte. Es una distancia esférica (radio) dentro de la cual, si entra otro vértice de la misma malla, el vértice comienza a desviarse para evitar una autocolisión.

Establezca este valor en la distancia fraccionaria entre los vértices que desea que tengan su propio "espacio". Un valor demasiado alto incluirá demasiados vértices en todo momento y ralentizará el cálculo. Un nivel demasiado bajo permitirá que otros vértices se acerquen demasiado y, por lo tanto, posiblemente se crucen porque no habrá tiempo suficiente para frenarlos.

Rigidez
Qué elástica es esa bola de espacio personal. Una rigidez alta significa que el vértice reacciona inmediatamente cuando otro vértice entra en su espacio.

humedecimiento
Cómo reacciona el vértice. Un valor bajo simplemente ralentiza el vértice cuando se acerca demasiado. Un valor alto lo rechaza.

Nota

Las colisiones con otros objetos se configuran en el panel (otra) Colisión . Para colisionar con otro objeto, deben compartir al menos una capa común.


Solucionador

solucionador 
Referencia

Grupo :
Física ‣ Cuerpo blando ‣ Solver

La configuración en el panel Soft Body Solver determina la precisión de la simulación.

Tamaño de paso mínimo
Pasos mínimos de simulación por cuadro. Aumente este valor si el cuerpo blando no alcanza objetos de colisión que se mueven rápidamente.

máx.
Pasos máximos de simulación por cuadro. Normalmente, el número de pasos de simulación se establece dinámicamente (con el Límite de error ), pero probablemente tenga una buena razón para cambiarlo.

Paso automático
Utilice velocidades para tamaños de paso automáticos. Ayuda al Solver a determinar cuánto trabajo necesita hacer en función de la velocidad a la que se mueven las cosas.

Límite de errores
Norma la calidad general de la solución entregada. La configuración más crítica que define la precisión con la que el solucionador debe comprobar las colisiones. Comience con un valor que sea la mitad de la longitud promedio del borde. Si hay errores visibles, inquietudes o respuestas demasiado exageradas, reduzca el valor. El solucionador realiza un seguimiento de qué tan "mal" lo está haciendo y el límite de error hace que el solucionador realice un "tamaño de paso adaptativo".

Diagnóstico 
Rendimiento de impresión en la consola
Imprime en la consola cómo está funcionando el solucionador.

Estimar transformaciones
Matriz de estimación, dividida en COM, ROT, SCALE.

Ayudantes 
Estas configuraciones controlan cómo reaccionará (deformará) el cuerpo blando una vez que se acerque o realmente cruce (corte) otro objeto de colisión en la misma capa.

Ahogo
Calma (reduce la velocidad de salida de) un vértice o borde una vez que penetra una malla de colisión.

Difuso
Borrosidad durante una colisión, los valores altos hacen que el manejo de la colisión sea más rápido pero menos estable. La simulación es más rápida, pero menos precisa.
Las colisiones con otros objetos se configuran en el panel (otra) Colisión . Para colisionar con otro objeto, deben compartir al menos una capa común.
Diagnóstico
Ayudantes



 exterior FORCES
Se aplican fuerzas exteriores a los vértices (y casi exclusivamente a los vértices) de los objetos de cuerpo blando. Esto se hace usando las Leyes de la Física de Newton:

Si no hay fuerza sobre un vértice, éste permanece inmóvil o se mueve con rapidez constante en línea recta.

La aceleración de un vértice depende de su masa y de la fuerza. Cuanto más pesada es la masa de un vértice, más lenta es la aceleración. Cuanto mayor es la fuerza mayor es la aceleración.

Por cada acción hay una reacción igual y opuesta.

Bueno, esto se hace sólo en el rango de precisión de cálculo, siempre hay un poco de amortiguación para evitar sobrepasar el cálculo.

Ejemplo 
Comenzaremos con un ejemplo muy sencillo: el cubo predeterminado.

Para juzgar el efecto de las fuerzas externas, primero debes apagar el Objetivo , para que los vértices no se retraigan a su posición original.

Inicie la reproducción para ejecutar la simulación.


¿Lo que sucede? El cubo se mueve en dirección Z negativa. Cada uno de sus ocho vértices está afectado por una fuerza global constante: la gravitación. La gravitación sin fricción es independiente del peso de un objeto, por lo que cada objeto que usarías aquí como cuerpo blando caería con la misma aceleración. El objeto no se deforma, porque todos los vértices se mueven con la misma velocidad en la misma dirección.

Campos de fuerza 
Los vértices del cuerpo blando interactúan con todos los campos de fuerza aplicados (generalmente a partículas) en la capa, como el viento, los campos de fuerza y ​​cualquier efecto de campo físico en una capa común.

Pesos de campo de cuerpo blando 
Referencia

Grupo :
Física ‣ Cuerpo blando ‣ Pesos de campo

El panel Pesos del campo del cuerpo blando le permite controlar cuánta influencia tiene cada tipo de campo de fuerza externo en el sistema del cuerpo blando.

Colección efector
Limite los efectores a un grupo específico. Sólo los efectores de este grupo tendrán efecto en el sistema actual.

Gravedad
Controle cuánto efecto tiene la Gravedad Global en el sistema.

Todo
Escale todos los pesos efectores.

Aerodinámica 
Los bordes pueden verse afectados por el viento a medida que se mueven y navegar o aletear con la brisa. Un modelo aerodinámico sencillo de una bandera ondeando al viento.

Esta fuerza exterior especial no se aplica a los vértices sino a los bordes de conexión. Técnicamente, se aplica una fuerza perpendicular al borde. La fuerza aumenta con la proyección de la velocidad relativa en el borde (producto escalar). Tenga en cuenta que la fuerza es la misma si sopla viento o si arrastra el borde por el aire con la misma velocidad. Eso significa que un borde que se mueve en su propia dirección no está sujeto a ninguna fuerza, y un borde que se mueve perpendicular a su propia dirección está sujeto a una fuerza máxima.

El ángulo y la velocidad relativa entre el medio y el borde se utilizan para calcular la fuerza sobre el borde. Esta fuerza hace que los vértices con pocas aristas de conexión (frente de un plano) caigan más rápido que los vértices con más aristas de conexión (en el centro de un plano). Si todos los vértices tienen la misma cantidad de aristas en una dirección, caen con la misma velocidad.

La configuración de Aerodinámica se establece en el panel Bordes suaves del cuerpo .

Meta 
Una “meta” es una forma a la que un objeto de cuerpo blando intenta adaptarse. Actúa como un alfiler en un conjunto elegido de vértices, controlando el efecto que el cuerpo blando tiene sobre ellos.

Habilitar Soft Body Goal le dice a Blender que use la posición (o posición animada) de un vértice en la simulación. La animación de los vértices se puede realizar de todas las formas habituales (curvas F, armaduras, padres, celosías, etc.) antes de aplicar la simulación del cuerpo blando. El "objetivo" es la posición final deseada para los vértices. La forma en que un cuerpo blando intenta lograr este objetivo se puede definir mediante fuerzas de rigidez y amortiguación.

Consulte la Configuración de objetivos para obtener más detalles.

Fuerza del objetivo 
La fuerza del objetivo define cuánto movimiento se aplica de un sistema de animación.

Un valor de Objetivo de 1,0 significa que no hay simulación de cuerpo blando, el objeto actúa como cualquier objeto animado normal (es decir, el vértice se mantiene en su posición original). Cuando se establece el Objetivo en 0.0 (o ningún objetivo), el vértice solo se ve influenciado por las leyes físicas de acuerdo con la simulación del cuerpo blando.

Al establecer valores objetivo entre 0,0 y 1,0, puede combinar entre que el objeto se vea afectado solo por el sistema de animación y que el objeto se vea afectado solo por el efecto de cuerpo blando.

Goal también sirve como memoria, para asegurarse de que los objetos blandos no se deformen demasiado y terminen en la forma animada no suave. Usando el sistema de ponderación del grupo de vértices , puede definir un peso de objetivo por vértice. Para que esto parezca más natural, se pueden definir fuerzas de resorte para controlar qué tan lejos pueden moverse los vértices desde su posición original.

A menudo, Weight Paint se utiliza para ajustar el peso cómodamente. Para objetos que no son de malla, se utiliza en su lugar el parámetro Peso de sus vértices/puntos de control; Utilice el menú contextual en el modo de edición o el panel Transformar en la región de la barra lateral. El peso de las partículas de cabello también se puede pintar en el modo de edición de partículas .

Detalles técnicos 
En el mundo de Soft Body, los vértices de las mallas se tratan como partículas que tienen masa. Su movimiento está determinado por las fuerzas que los afectan. Además de otras fuerzas, las partículas individuales pueden interactuar entre sí a lo largo de los bordes utilizando un modelo físico muy parecido a los amortiguadores utilizados en los automóviles. Las partes de trabajo son:

Un resorte que intenta mantener las partículas a cierta distancia. La fuerza con la que el resorte intenta hacerlo está controlada por el parámetro de cuerpo blando Rigidez .

Un elemento amortiguador para calmar el movimiento. La resistencia que el elemento genera contra el movimiento está controlada por el parámetro de cuerpo blando Amortiguación .




 interior
Entre cada vértice vecino de una malla, normalmente se crean bordes para conectarlos. Imagine cada borde como un resorte. Cualquier resorte mecánico puede estirarse bajo tensión y apretarse bajo presión. Todos los resortes tienen una longitud ideal y una rigidez que limita cuánto se puede estirar o apretar el resorte.

En el caso de Blender, la longitud ideal es la longitud del borde original que diseñaste como parte de tu malla, incluso antes de habilitar el sistema Soft Body. Hasta que agregue la física del cuerpo blando, se supone que todos los resortes son perfectamente rígidos: no se estiran ni se aprietan.

Puede ajustar la rigidez de todos esos resortes de borde, permitiendo que la malla se hunda, se doble, se agite con la brisa o se acumule en el suelo.

Para crear una conexión entre los vértices de un objeto de cuerpo blando, tiene que haber fuerzas que mantengan unidos los vértices. Estas fuerzas son efectivas a lo largo de los bordes de una malla, las conexiones entre los vértices. Las fuerzas actúan como un resorte. Fig. Vértices y fuerzas a lo largo de sus bordes de conexión. ilustra cómo se conecta una cuadrícula de vértices de 3×3 (un plano de malla en Blender) en una simulación de cuerpo blando.

../../../_images/physics_soft-body_forces_interior_theory-1.svg
Vértices y fuerzas a lo largo de sus aristas de conexión. 

../../../_images/physics_soft-body_forces_interior_theory-2.svg
Fuerzas adicionales con Stiff Quads habilitado. 

Pero dos vértices podrían girar libremente si no se crean aristas adicionales entre ellos. El método lógico para evitar que un cuerpo colapse sería crear aristas adicionales entre los vértices. Esto funciona bastante bien, pero cambiaría drásticamente la topología de su malla.

Por suerte, Blender permite definir conexiones virtuales adicionales . Por un lado, puede definir conexiones virtuales entre los bordes diagonales de una cara cuádruple ( Fig. Stiff Quads . Fuerzas adicionales con Stiff Quads habilitado ). Por otro lado, puede definir conexiones virtuales entre un vértice y cualquier vértice conectado a sus vecinos. Rigidez a la flexión . En otras palabras, la cantidad de curvatura permitida entre un vértice y cualquier otro vértice que esté separado por dos conexiones de borde.

Ajustes 
Las características de los bordes se establecen con las propiedades Resortes y Cuadrángulos rígidos en el panel Bordes suaves del cuerpo . Consulte la configuración de Bordes suaves del cuerpo para obtener más detalles.

Consejos: Prevenir el colapso 
Cuádriceps 
Para mostrar el efecto de las diferentes configuraciones de bordes usaremos dos cubos (azul: solo quads, rojo: solo tris) y los dejaremos caer sin ningún objetivo sobre un avión (cómo configurar la colisión se muestra en la página Colisiones ).

Sin cuádriceps rígidos. 
../../../_images/physics_soft-body_forces_interior_quadvstri-sb-001.png
Cuadro 1. 

../../../_images/physics_soft-body_forces_interior_quadvstri-sb-036.png
Cuadro 36. 

../../../_images/physics_soft-body_forces_interior_quadvstri-sb-401.png
Cuadro 401. 

En la figura. Sin cuádriceps rígidos. , se utilizan los ajustes predeterminados (sin Stiff Quads ). El cubo "quad only" colapsará por completo, el cubo compuesto de tris mantiene su forma, aunque se deformará temporalmente debido a las fuerzas creadas durante la colisión.

Con cuádriceps rígidos. 
../../../_images/physics_soft-body_forces_interior_quadvstri-sb-001.png
Cuadro 1. 

../../../_images/physics_soft-body_forces_interior_quadvstri-sb-sq-036.png
Cuadro 36. 

../../../_images/physics_soft-body_forces_interior_quadvstri-sb-sq-401.png
Cuadro 401. 

En la figura. Con cuádriceps rígidos. , Stiff Quads está activado (para ambos cubos). Ambos cubos mantienen su forma, no hay diferencia para el cubo rojo, porque de todos modos no tiene cuadritos.

Rigidez a la flexión 
El segundo método para evitar que un objeto colapse es cambiar su rigidez a la flexión . Esto incluye los bordes diagonales (la amortiguación también se aplica a estas uniones).

Rigidez a la flexión. 
../../../_images/physics_soft-body_forces_interior_quadvstri-sb-001.png
Cuadro 1. 

../../../_images/physics_soft-body_forces_interior_quadvstri-sb-bs-036.png
Cuadro 36. 

../../../_images/physics_soft-body_forces_interior_quadvstri-sb-bs-401.png
Cuadro 401. 

En la figura. Rigidez a la flexión. , La flexión se activa con una configuración de fuerza de 1. Ahora ambos cubos son más rígidos.

../../../_images/physics_soft-body_forces_interior_quadvstri-bending-001.png
Dos aviones van a chocar. 

../../../_images/physics_soft-body_forces_interior_quadvstri-bending-101.png
Sin rigidez a la flexión. 

../../../_images/physics_soft-body_forces_interior_quadvstri-bending-high-101.png
Alta rigidez a la flexión (10). 

La rigidez a la flexión también se puede utilizar si desea que un plano subdividido parezca más una tabla. Sin doblarse, las caras pueden girar libremente entre sí como bisagras. Fig. Sin rigidez a la flexión. . No habría ningún cambio en la simulación si activaras Stiff Quads , porque las caras no están deformadas en absoluto en este ejemplo.

La rigidez a la flexión es la fuerza necesaria para que el plano se deforme.



Colisión 
Hay dos tipos de colisiones diferentes que puede utilizar: colisión entre diferentes objetos y colisión interna. Deberíamos dejar una cosa clara desde el principio: los objetivos principales del cálculo de colisiones son los vértices de un cuerpo blando. Entonces, si tiene muy pocos vértices, se producirán muy pocas colisiones. En segundo lugar, puede utilizar aristas y caras para mejorar el cálculo de colisiones.

Colisiones con otros objetos 
Para que un cuerpo blando choque con otro objeto existen algunos requisitos previos:

Si se establece Collision Collection , el objeto debe pertenecer a la colección.

El objeto de la colisión tiene que ser un objeto de malla.

Tienes que activar la Colisión en la pestaña Física para el objeto de colisión. El objeto de la colisión también puede ser un cuerpo blando.

Ejemplos 
Un cubo de cuerpo blando que choca con un avión (Fig. Un cubo de cuerpo blando que choca con un avión. ) funciona bastante bien, pero un plano de cuerpo blando cae a través de un cubo con el que se supone que debe chocar (Fig. Un plano de cuerpo blando que choca con un cubo, por lo que no hay interacción alguna ).

../../_images/physics_soft-body_collision_cube-plane-1.png
Un cubo de cuerpo blando que choca con un avión. 

../../_images/physics_soft-body_collision_cube-plane-2.png
Un avión de cuerpo blando que choca con un cubo, por lo que no hay interacción alguna. 

¿Porqué es eso? Porque el método de cálculo predeterminado solo verifica si los cuatro vértices del plano del cuerpo blando chocan con el cubo cuando el avión es arrastrado hacia abajo por la gravedad. Puede activar Colisión: Cara (en el panel Bordes suaves del cuerpo ) para habilitar la colisión entre la cara del plano y el objeto, pero este tipo de cálculo lleva mucho más tiempo.

Echemos un vistazo más de cerca al cálculo de colisiones, para que pueda tener una idea de cómo podríamos optimizarlo.

Calculando colisiones 
Las simulaciones de cuerpos blandos se realizan de forma predeterminada por vértice. Si los vértices del cuerpo blando no chocan con el objeto de colisión, no habrá interacción entre los dos objetos.

En el vídeo a continuación, puedes ver los vértices chocando con un avión. Si un vértice penetra en la zona entre Exterior e Interior , es rechazado por una fuerza en la dirección de la cara normal. La posición en la que finalmente termina un vértice depende de las fuerzas que actúan sobre él. En el ejemplo (el primer vértice a la izquierda en el video a continuación), la gravedad y la fuerza de repulsión de la cara se equilibran. La velocidad a la que se saca el vértice de la zona de colisión está influenciada por el parámetro Choke en la configuración de Soft Body Solver .


Ver también

Descargue el archivo blend .

Ahora veamos qué sucede si hacemos que los vértices sean más pesados ​​y los dejamos viajar a mayor velocidad. En el vídeo de arriba, puedes ver los vértices viajando a diferentes velocidades. Los dos del extremo derecho (quinto y sexto) viajan tan rápido que pasan justo por la zona de colisión (esto se debe a la precisión predeterminada del solucionador, que podremos corregir más adelante). Notarás que el cuarto vértice también viaja bastante rápido y al ser más pesado rompe la zona interior. Los primeros tres vértices chocan correctamente.

Puede configurar su colisión para que los bordes e incluso las caras se incluyan en el cálculo de la colisión en el panel Bordes suaves del cuerpo con las opciones Cara de colisión y Borde . Entonces la colisión se calcula de otra manera. Se comprueba si el borde o la cara se cruza con el objeto de colisión, no se utilizan las zonas de colisión.

Buenas colisiones 
Si la colisión que has configurado no se comporta correctamente, puedes intentar lo siguiente:

El objeto de cuerpo blando debe tener más subdivisiones que el objeto de colisión. Agregue cortes de bucle al objeto de cuerpo blando en áreas estratégicas que sabe que tienen más probabilidades de verse involucradas en una colisión.

Verifique la dirección de las normales de la cara.

Si el objeto de la colisión tiene púas afiladas, estas podrían penetrar el cuerpo blando.

La resolución del solucionador debe coincidir con la velocidad a la que viajan los vértices del cuerpo blando. Reduzca el parámetro Límite de error y aumente con cuidado el paso mínimo .

Exterior e Interior deben ser lo suficientemente grandes, pero las zonas de caras opuestas no deben superponerse, o habrá fuerzas en direcciones opuestas.

Si usas fuerzas fuertes debes usar zonas grandes.

Establezca Choke en un valor suficientemente alto (hasta arriba si es necesario) si tiene dificultades con los vértices repelidos.

Las caras en colisión son difíciles de controlar y requieren largos tiempos de cálculo. Intenta no usarlos.

A menudo es mejor crear una malla simplificada para usarla como objeto de colisión; sin embargo, esto puede resultar difícil si utiliza una malla animada.

Autocolisiones 
Para obtener información sobre la autocolisión, consulte la configuración de Autocolisión .



Ejemplos 
A continuación se muestran algunos ejemplos sencillos que muestran el poder de la física del cuerpo blando.

Un cubo que 
El proceso 
Primero, cambie los fotogramas inicial y final a 1 y 150.

Luego, agrega un avión y escale cinco veces. Luego, vaya a la pestaña de física y agregue una colisión. La configuración predeterminada está bien para este ejemplo.

Ahora agregue un cubo, o use el cubo predeterminado, luego ingrese al Modo de edición para subdividirlo tres veces. Agregue un modificador de bisel para suavizar los bordes y luego, para agregar un poco más, presione Rdos veces y mueva el cursor un poco.

Cuando termine, su escena debería verse así:

../../_images/physics_soft-body_examples_scene-ready.png
La escena, lista para la física del cuerpo blando. 

Todo está listo para agregar la física del cuerpo blando. Ir aPropiedades ‣ Físicay elige Cuerpo Blando . Desmarque el Objetivo de cuerpo blando y marque Autocolisión de cuerpo blando . Además, en Bordes suaves del cuerpo , aumente la curvatura a 10.

Al reproducir la animación ahora se mostrará una animación lenta de un cubo que rebota. Para acelerar las cosas, necesitamos perfeccionar la física del cuerpo blando.

En Soft Body Cache, cambie los valores de los fotogramas inicial y final. En este caso 1 y 150. Ahora, para probar si todo funciona, puedes dar un paso de caché de 5 o 10, pero para la animación final es mejor reducirlo a 1, para almacenar en caché todo.

Ahora puedes hornear la simulación, darle materiales y texturas al cubo y renderizar la animación.











_fsl_

[Regresar](./)
