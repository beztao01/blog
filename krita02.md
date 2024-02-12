---
layout: default

---

## Krita unos primeros pasos

Algunos datos para la interfaz usando vectores.

![vectores02](https://i.imgur.com/C11VUHA.jpg)

1. Espacio de trabajo vectorial.
2. Opciones de la herramienta.
3. Capa vectorial, no se debe usar capa de pintura.
4. Herramienta Curva de Bezier para trazo vectorial.
5. Rotación del canvas.

Krita se caracteriza por ser un lienzo digital, eso no evita que puedas usar las herramientas vectoriales que tiene.

Puedes cambiar el espacio de trabajo para usarlo hay uno específico para tal proposito, llamda big vector, con las clásicas herramientas para contorno y relleno que puedes cambiar en cualquier momento.

Tienes que usar forzosamente la capa vectorial.

Para hacer trazos libres tienes la herramienta curva de Bezier.


##Gráficos vectoriales

Krita 4.0 ha tenido una reescritura masiva de las herramientas vectoriales. Aquí hay una página que explica las herramientas vectoriales:

### ¿Qué son los gráficos vectoriales?

Krita es principalmente una herramienta de edición de gráficos rasterizados, lo que significa que la mayor parte de la edición cambia los valores de los píxeles en la trama que compone la imagen.

![MarineGEO circle logo](/assets/img/MarineGEO_logo.png "MarineGEO logo")

![Pincel](https://docs.krita.org/fr/_images/Pixels-brushstroke.png)


Por otro lado, los gráficos vectoriales utilizan las matemáticas para describir una forma. Debido a que utiliza una fórmula, los gráficos vectoriales se pueden cambiar de tamaño a cualquier tamaño.

Por un lado, esto hace que los gráficos vectoriales sean ideales para logotipos y pancartas. Por otro lado, los gráficos rasterizados son mucho más fáciles de editar, por lo que los vectores tienden a ser el dominio del diseño deliberado, que utiliza mucha precisión.

### Herramientas para hacer formas.
Puede comenzar a crear gráficos vectoriales creando primero una capa vectorial (presione el botón de flecha al lado de + en la ventana acoplable de capas para obtener tipos de capas adicionales). Luego, se pueden utilizar todas las herramientas de dibujo habituales fuera de Mano alzada, Dinámica y Multipincel para dibujar formas.

Las herramientas Trazado y Polilínea son las herramientas que utiliza con más frecuencia en una capa vectorial, ya que le permiten crear las formas más dinámicas.

Por otro lado, las herramientas Elipse y Rectángulo le permiten dibujar formas especiales, que luego pueden editarse para crear formas circulares especiales o rectángulos redondeados fáciles.

La herramienta de caligrafía y texto también crea vectores especiales. La herramienta de caligrafía sirve para producir trazos similares a los de un pincel, mientras que la herramienta de texto crea un objeto de texto que se puede editar posteriormente.

Todos estos utilizarán el tamaño actual del pincel para determinar el grosor del trazo, así como el color actual de primer plano y de fondo.

Hay una última forma de crear vectores: la herramienta Imagen vectorial . Le permite agregar formas que se han definido en un archivo SVG como símbolos. A diferencia de las otras herramientas, estas tienen su propio relleno y trazo.

### Organizar formas
Una capa vectorial tiene su propia jerarquía de formas, muy parecida a como toda la imagen tiene una jerarquía de capas. Entonces las formas pueden estar una frente a la otra. Esto se puede modificar con la ventana acoplable Organizar o con la herramienta Seleccionar formas .

La ventana acoplable Organizar también le permite agrupar y desagrupar formas. También le permite alinear formas con precisión, por ejemplo, alinearlas hacia el centro o tener un espacio uniforme entre todas las formas.

### Editar formas
La edición de formas vectoriales se realiza con la herramienta Seleccionar formas y la herramienta Editar formas .

La herramienta Seleccionar formas se puede utilizar para seleccionar formas vectoriales, agruparlas (mediante ratón derecho), desagruparlas, usar valores booleanos para combinar o restar formas entre sí (mediante ratón derecho), moverlas hacia arriba y hacia abajo o realizar transformaciones rápidas.

### Llenar
Puedes cambiar el relleno de una forma seleccionándola y cambiando el color de primer plano activo.

También puedes cambiarlo accediendo a las opciones de la herramienta Seleccionar formas y yendo a la pestaña Relleno .

Las formas vectoriales se pueden rellenar con un color sólido, un degradado o un patrón.

### Ataque
Los trazos se pueden rellenar con los mismos elementos que los rellenos.

Sin embargo, también se pueden modificar más. Por ejemplo, puedes agregar guiones y marcadores a la línea.

### Coordenadas
Las formas se pueden mover con la herramienta Seleccionar formas y en las opciones de la herramienta puede especificar las coordenadas exactas.

### Edición de nodos y parámetros especiales.
Si tiene una forma seleccionada, puede hacer doble clic en ella para acceder a la herramienta adecuada para editarla. Normalmente esta es la herramienta Editar forma , pero para texto esta es la herramienta Texto .

En la herramienta Editar forma , puede moverse por los nodos en el lienzo para obtener rutas regulares. Para trazados especiales, como la elipse y el rectángulo, puede mover nodos y editar los parámetros específicos en la ventana acoplable Opciones de herramienta .

### Trabajando junto con otros programas.
Una de las grandes cosas que trajo Krita 4.0 fue el paso ODGde SVG. Lo que esto significa es que Krita guarda como archivos SVGinternos KRA, y eso significa que Krita puede abrirse SVGsin problemas. Esto es importante ya que SVGes el formato vectorial más popular.

### paisaje de tinta.
Puede copiar y pegar vectores de Krita a Inkscape, o de Inkscape a Krita. Solo se admiten las funciones, con excepción de funciones más pequeñas como los degradados de malla.SVG 1.1



_fsl_

[Regresar](./)
