# [Diseño y visualización de información](https://github.com/profesorfaco/troncal/) → Clase 09 → 14 de octubre

### RawGraph *et al*

RAWGraphs, como proyecto, nació en el [DensityDesign Lab](https://densitydesign.org/) del Politécnico de Milán, y hoy por hoy es mantenido por el mismo Lab y [Calibro](https://calib.ro/).

Para saber más sobre el proyecto, se le pide leer: Mauri, M., Elli, T., Caviglia, G., Uboldi, G., & Azzi, M. (2017). *RAWGraphs: A Visualisation Platform to Create Open Outputs*. Proceedings of the 12th Biannual Conference on Italian SIGCHI Chapter, 28:1--28:5. https://doi.org/10.1145/3125571.3125585

En el *abstract* del artículo que se le pide leer, traducido con la versión gratuita del traductor DeepL.com, dice:

> RAWGraphs es una aplicación web de código abierto para la creación de visualizaciones estáticas de datos diseñadas para ser modificadas posteriormente. Concebida originalmente para diseñadores gráficos con el fin de proporcionar una serie de tareas no disponibles con otras herramientas, evolucionó hasta convertirse en una plataforma que ofrece formas sencillas de mapear las dimensiones de los datos en variables visuales. Presenta un enfoque de la visualización de datos basado en gráficos: cada modelo visual es un módulo independiente que expone distintas variables visuales que pueden utilizarse para mapear dimensiones de datos. De este modo, los usuarios pueden crear visualizaciones de datos complejas. Por último, la herramienta está pensada para producir resultados abiertos, es decir, no sujetos a soluciones propietarias, que puedan editarse posteriormente.

En el abstract pudo leer una idea repetida:

- *visualizaciones estáticas de datos diseñadas **para ser modificadas posteriormente*** 

- *la herramienta está pensada para producir resultados abiertos, es decir, no sujetos a soluciones propietarias, que puedan **editarse posteriormente***

Otras aplicaciones que permiten la creación de visualizaciones son:  

- https://flourish.studio/

- https://www.tableau.com/

- https://www.datawrapper.de/

Pero ellas no comparten la idea de la *modificación posterior* ni el *resultado abierto*. 

Si lo que importa es la modificación y el resultado abierto, corresponde pensar en alternativas más complejas; entre ellas podrían considerarse las bibliotecas de JavaScript especializadas en la creación de visualizaciones, entre las que se cuentan: 

- https://d3js.org/

- https://www.chartjs.org/

- https://echarts.apache.org/


Cualquiera se la anternativa que se use, corresponde considerar desde el diseño que, **los gráficos (*chart* en inglés; *diagramm* en alemán) se ven y leen. Capturan la mirada y en ellos se nos da algo a comprender según cierta convención; y es por lo convenido que distintos gráficos tienen distintas funciones y estructuras**.

Para no fallar en la elección de un gráfico, la primera pregunta que le corresponde hacerse es *¿Qué desea mostrar?*. 

Por favor revise la pregunta y alternativas de respuesta en: https://datavizcatalogue.com/ES/buscar.html

Luego, si usted tiene 2 columnas de datos: cada columna puede pasar al eje *x* o *y*, a la *abscisa* o la *ordenada*, y con eso ya estaría traslando lo abstracto de 2 variables a una configuración visual en un plano cartesiano.

Pero si usted tiene sólo 2 columnas de datos, no tendría sentido, por ejemplo, proponer un [gráfico de burbujas](https://datavizcatalogue.com/ES/metodos/grafico_de_burbujas.html), porque tal gráfico se estructura con 4 variables (o 4 columnas de datos):

- coordenadas x
- coordenadas y
- radio de la burbuja
- color de la burbuja

Tales variables se aprovechan de las variables posición, tamaño, textura, orientación, forma y/o color (matiz, saturación y luminosidad)

En [*Semiology of Graphics*](https://www.esri.com/en-us/esri-press/browse/semiology-of-graphics-diagrams-networks-maps) de Jacques Bertin, se lee:

> Fixed at a given point on the plane, the mark, provided it has a certain dimension, can be drawn in different modes. It can vary in\
SIZE\
VALUE\
TEXTURE\
COLOR\
ORIENTATION\
SHAPE\
and can also express correspondence between its planar position and its position in the series constituting each variable.

Corresponde hacer un paréntesis en lo de VALUE y COLOR, que refieren a dos de tres propiedades del color. 

Hay una cuestión práctica, relacionada con la impresión a color en la década de 1960 en París, que podría justificar a un Jacques Bertin que omite una de las tres propiedades del color: *The saturated tone is not of constante value but varies in value according to the color* […] *fact that leads to many of the main problems raised by the use of color* (2008, p.85). 

Para la época en que Jacques Bertin teorizaba convenía omitir, por problemas de reproducción impresa, la S en HSB, HSV, HSL o HSI:

- **H**ue

- **S**aturation

- **B**rightness, **V**alue, **L**ightness o **I**ntensity

La H de *Hue* refiere al color-color, el matiz o, según algunas traducciones, el tono. Ejemplo: El rojo es un *hue* distinto del verde. El *Hue* se define por grados (0° a 359°) en un círculo que une al extremo violeta con el extremo rojo a través del magenta no espectral. 

La S de *Saturation* refiere a la fuerza o pureza del color. Ejemplo: un rojo-rojo es un rojo muy saturado, y un verde-verde también lo es. La *Saturation* se define con porcentajes (0% a 100%).

El asunto se complica en las múltiples opciones para la tercera sigla, cuando B, V, L e I refieren a cuán iluminada esté la marca coloreada en el plano, acercándose a la luz (blanco) u oscuridad (negro), y lo hace con un porcentaje, de 0% a 100%. Pero el 100% implica distintas iluminaciones según sea B, V, L o I. A usted le corresponde averiguar y recordar cuándo la mejor iluminación es 50% o 100%.

Puesto de otro modo, a usted le queda averiguar, con la ayuda de un modelo tridimensional, cuando el rojo-rojo con la mejor iluminación es 0° 100% 100% y cuándo es 0° 100% 50% entre HSB, HSV, HSL o HSI.

Aún en el paréntesis, queda agregar que la omisión de una de las propiedades del color puede ser útil después de un giro importante de la Organización Mundial de la Salud, la que pensaba a la discapacidad como atributo personal en la década de 1980 y comenzó a pensar en el año 2001 que la discapacidad depende del contexto: «La discapacidad no es sólo un problema de salud. Es un fenómeno complejo que refleja la interacción entre las características del cuerpo de una persona y las características de la sociedad en la que vive» ([Microsoft, 2016](https://inclusive.microsoft.design/tools-and-activities/Inclusive101Guidebook.pdf)).

Aunque el 99% de la población [no sería ciega en Chile](https://fundacionluz.cl/noticias/2023/04/comunicado-los-bajos-porcentajes-educacionales-de-las-personas-con-discapacidad-visual-redundan-en-una-alta-cesantia-71-2-con-ceguera-total-no-tiene-trabajo/), nos queda que entre videntes el daltonismo puede afectar al 0,5% de las mujeres y 8% de los hombres. Lo que corresponde es mantener la confianza en el *VALUE*, pero revisar bien *HUE* y *SATURATION* con herramientas tales como [COLOR BREWER 2.0](https://colorbrewer2.org/), activando la opción de *colorblind safe*, o revisar nuestros trabajos en un navegador web después de activa alguna extensión como [Daltonize](https://chromewebstore.google.com/detail/daltonize/obcnmdgpjakcffkcjnonpdlainhphpgh?pli=1).


#### Referencias:

Bertin, J. (2008). Semiology of Graphics: diagrams, networks, maps. Esry Press. 

Koponen, J. & Hildén, J. (2019). Data Visualization Handbook. Aalto korkeakoulusäätiö.


_ _ _ _ 

[clase-08](https://github.com/profesorfaco/troncal/blob/main/clase-08/README.md) ⇆ [clase-10](https://github.com/profesorfaco/troncal/blob/main/clase-10/README.md)
