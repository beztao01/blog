---
layout: default

---

## Krita

Una alternativa libre a Photoshop.

Krita como su página lo indica, es un programa profesional de pintura digital, gratuito y hecho con código libre, ha sido creado por artistas mismos que desean hacer éstas herramientas accesibles para todos.

![Krita](https://upload.wikimedia.org/wikipedia/commons/1/15/Krita_5.0.0_screenshot.png)

Se usa para:

Arte conceptual

Pinturas de textura y mate

Ilustraciones e historietas

Enlace para descarga:
[Aqui](https://krita.org/es/)

### Tabletas de dibujo
Esta página trata sobre las tabletas de dibujo, qué son, cómo funcionan y dónde pueden salir mal las cosas.

#### ¿Qué son las tabletas?
Dibujar con un mouse puede resultar poco intuitivo y difícil en comparación con el lápiz y el papel. Peor aún, el uso prolongado del ratón puede provocar el síndrome del túnel carpiano. Es por eso que la mayoría de las personas que dibujan digitalmente utilizan una pieza de hardware especializada conocida como tableta de dibujo.

../_images/Krita_tablet_types.png
Una tableta gráfica es una pieza de hardware que puedes conectar a tu máquina, muy parecida a un teclado o un mouse. Por lo general, parece una almohadilla de plástico con un lápiz óptico. Otro formato popular es un monitor de computadora con un lápiz que se utiliza para dibujar directamente en la pantalla. Es mejor usarlos que un mouse porque es más natural dibujar con un lápiz y, en general, es mejor para las muñecas.

Con un lápiz óptico instalado correctamente, Krita puede usar información como la sensibilidad a la presión , lo que le permite realizar trazos que se hacen más grandes o más pequeños dependiendo de la presión que ejerza sobre ellos, para crear trazos más ricos e interesantes.

##### Nota

A veces, la gente confunde los lápices táctiles con una tableta adecuada. Puedes notar la diferencia porque el lápiz óptico de una tableta de dibujo generalmente tiene una punta puntiaguda, mientras que un lápiz hecho para tocar con los dedos tiene una punta grande y redonda de goma, como un dedo. Es posible que estas tabletas no den buenos resultados y se recomienda una tableta sensible a la presión .

../_images/Krita_tablet_stylus.png
Tabletas compatibles
Las tabletas compatibles son propiedad de los propios desarrolladores de Krita, por lo que pueden diagnosticar y corregir errores de forma fiable. Mantenemos una lista de ellos aquí .

Si buscas información sobre tablets iPad o Android, mira aquí .

Controladores y sensibilidad a la presión
Entonces has comprado una tableta, una tableta de dibujo real. ¡Y quieres que funcione con Krita! Entonces conectas el cable USB, inicias Krita y… ¡No funciona! O bueno, puedes hacer caricias, pero esa sensibilidad a la presión de la que tanto has oído hablar no parece funcionar.

Esto se debe a que necesita instalar un programa llamado "controlador". Por lo general, puede encontrar el controlador en un CD que se entregó junto con su tableta o en el sitio web del fabricante. Instálalo y, mientras esperas, entraremos en detalles de qué es.

Ejecutarlo en su computadora es un sistema básico que realiza todas las partes difíciles de ejecutar una computadora por usted. Este es el sistema operativo o SO. La mayoría de las personas usan un sistema operativo llamado Windows, pero las personas que usan un dispositivo Apple tienen un sistema operativo llamado macOS, y algunas personas, incluidos muchos de los desarrolladores, usan un sistema llamado Linux.

Sin embargo, el principio básico de todos estos sistemas es el mismo. Le gustaría ejecutar programas como Krita, llamado software, en su computadora, y desea que Krita pueda comunicarse con el hardware, como su tableta gráfica. Pero lograr que esos dos se comuniquen puede ser realmente difícil, por lo que el sistema operativo funciona como un pegamento entre los dos.

Cada vez que inicias Krita, Krita primero hará conexiones con el sistema operativo, por lo que puede pedirle muchas de estas cosas: le gustaría mostrar cosas, usar la memoria, etc. ¡Lo más importante es que le gustaría obtener información de la tableta!

../_images/Krita_tablet_drivermissing.png
¡Pero no puede! Resulta que tu sistema operativo no sabe mucho sobre tabletas. Para eso están los conductores. La instalación de un controlador le brinda al sistema operativo suficiente información, para que el sistema operativo pueda brindarle a Krita la información correcta sobre la tableta. El trabajo del fabricante de hardware es escribir un controlador adecuado para cada sistema operativo.

##### Advertencia

Debido a que los controladores modifican un poco el sistema operativo, siempre necesitarás reiniciar tu computadora al instalar o desinstalar un controlador, ¡así que no olvides hacerlo! Por el contrario, debido a que Krita no es un controlador, ni siquiera necesita desinstalarlo para restablecer la configuración, simplemente cambie el nombre o elimine el archivo de configuración.

#### Dónde puede salir mal: Windows
Krita se conecta automáticamente a su tableta si los controladores están instalados. Cuando las cosas van mal, normalmente el problema no está en Krita.

##### Las tabletas Surface Pro necesitan dos controladores
Ciertas tabletas que usan n-trig, como Surface Pro, tienen dos tipos de controladores. Uno es nativo, n-trig y el otro se llama WinTab. Desde 3.3, Krita puede usar controladores estilo Windows Ink, simplemente vaya a Configuración ‣ Configurar Krita… ‣ Configuración de la tableta y alterne la Entrada de puntero de Windows 8+ (Windows Ink) allí. Ya no es necesario instalar los controladores WinTab para bolígrafos basados ​​en n-trig.

##### Actualizaciones de Windows 10
A veces, una actualización de Windows 10 puede estropear los controladores de la tableta. En ese caso, reinstalar los controladores debería funcionar.

#### Tabletas Wacom
Hay tres problemas conocidos con las tabletas Wacom y Windows.

La primera es que si ha personalizado la configuración del controlador, a veces, a menudo después de una actualización del controlador, pero eso no es necesario, el controlador se estropea. Restablecer el controlador a la configuración predeterminada y luego cargar la configuración desde una copia de seguridad resolverá este problema.

La segunda es que por alguna razón podría ser necesario cambiar el orden de prioridad de visualización. Es posible que tengas que convertir la pantalla de tu Cintiq en tu pantalla principal o, por el contrario, convertirla en la pantalla secundaria. Verifique nuevamente en la utilidad de configuración de Wacom que la tableta en el Cintiq esté asociada con la pantalla del Cintiq.

La tercera es que si tiene una tableta con pantalla como Cintiq y un control remoto Wacom ExpressKeys, y ha desactivado Windows Ink en la página de calibración del cuadro de diálogo de configuración del lápiz, para tener el conjunto completo de funciones de WinTab, el Cintiq necesita ser el primer elemento en la lista de aplicaciones de escritorio de Wacom. De lo contrario, tendrá un desplazamiento entre el lápiz y el mouse que empeorará cuantas más pantallas haya a la izquierda de la pantalla del Cintiq.

##### Controladores rotos
Los controladores de la tableta deben ser fabricados por el fabricante. A veces, con tabletas realmente baratas, el hardware está bien, pero el controlador está mal escrito, lo que significa que simplemente no funciona bien. Lamentablemente, no podemos hacer nada al respecto. Tendrá que enviar una queja al fabricante por esto o comprar una tableta mejor con controladores de mejor calidad.

##### Conductores conflictivos
En Windows, sólo puede tener instalado un único controlador estilo WinTab a la vez. Así que asegúrese de desinstalar el controlador anterior antes de instalar el que viene con la tableta que desea utilizar. Otros sistemas operativos son un poco mejores en esto, pero incluso Linux, donde los controladores suelen estar preinstalados, no puede ejecutar dos tabletas con controladores diferentes a la vez.

##### Software que interfiere
A veces, hay software que intenta crear una capa de seguridad entre Krita y el sistema operativo. Sandboxie es un ejemplo de esto. Sin embargo, Krita no siempre puede conectarse a ciertas partes del sistema operativo mientras está en el espacio aislado, por lo que a menudo falla en programas como Sandboxie. De manera similar, ciertos programas de mouse, como las utilidades de Razer, también pueden afectar la capacidad de Krita para comunicarse con el sistema operativo, convirtiendo la información de la tableta en información del mouse. Este tipo de software debe configurarse para dejar a Krita en paz o desinstalarse.

Se ha informado que el siguiente software interfiere con los eventos de la tableta en Krita:

1.- caja de arena

2.- Utilidades del ratón Razer

2.- “Modo de juego” AMD Catalyst TM (esto le rompió el clic derecho a alguien)

##### Flicks (espera que aparezca el círculo y luego llama a la paleta emergente)
Si se encuentra en una situación en la que al intentar dibujar sigue apareciendo la paleta emergente en Windows, entonces el problema podría ser el movimiento. Se trata de un tipo de gesto, una pequeña funcionalidad de Windows que le permite realizar un movimiento que sirve como método abreviado de teclado. Windows los activa automáticamente cuando instala controladores de tableta, porque las personas que crearon esta parte de Windows olvidaron que la gente también dibuja con las computadoras. Por lo tanto, deberá desactivarlo en la configuración de películas de Windows.

##### Sensibilidad de doble clic de Wacom (inicios rectos de líneas)
Si experimenta un problema en el que el inicio del trazo es recto y tiene una tableta Wacom, podría deberse a la detección de doble clic del controlador Wacom.

Para solucionar este problema, vaya a la utilidad de configuración de Wacom y reduzca la sensibilidad del doble clic.

© Copyright con licencia de documentación libre GNU 1.3+ a menos que se indique lo contrario

_fsl_

[Regresar](./)
