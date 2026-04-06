# Unidad 2-Apuntes
------
Este repositorio contiene los apuntes de clase correspondientes a la Unidad II, elaborados a partir de una investigación documental y el análisis de diversas fuentes académicas. En él se desarrollan los temas teóricos más relevantes de la unidad, presentados de manera ordenada, clara y estructurada, con el propósito de facilitar su comprensión.

------
# 📑 Índice - Unidad II
- [2.1 Transformación bidimensional](#21-transformación-bidimensional)
  - [2.1.1 Traslación](#211-traslación)
  - [2.1.2 Escalamiento](#212-escalamiento)
  - [2.1.3 Rotación](#213-rotación)
  - [2.1.4 Sesgado](#214-sesgado)
- [2.2 Representación matricial de las transformaciones bidimensionales](#22-representación-matricial-de-las-transformaciones-bidimensionales)
- [2.3 Trazo de líneas curvas](#23-trazo-de-líneas-curvas)
  - [2.3.1 Bézier](#231-bézier)
  - [2.3.2 B-spline](#232-b-spline)

- [2.4 Fractales](#24-fractales)

- [2.5 Uso y creación de fuentes de texto](#25-uso-y-creación-de-fuentes-de-texto)
- [Bibliografía](#bibliografía)
---
2.1. Transformación bidimensional.
----
En adición a objetos geométricos, las transformaciones geométricas juegan un rol crucial en los gráficos por computadora. Las transformaciones geométricas pueden ser usadas para posicionar objetos, por ejemplo para cambiarlos a otra posición o rotarlos, para cambiar la forma de los objetos, para enconjerlos en una dirección, o mover objetos o cambiar la forma de objetos paso a paso por escenas animadas.

Existen básicamente tres operaciones o transformaciones geométricas básicas, a partir de las cuales se pueden realizar todas las demás. Estas transformaciones son la traslación, el escalamiento y la rotación, todas respecto del origen. 
La transformación bidimensional es un concepto fundamental en la geometría computacional y el diseño gráfico que se refiere a las operaciones matemáticas aplicadas a figuras en un plano bidimensional. Estas transformaciones modifican la posición, orientación, tamaño o forma de los objetos sin salir del plano. En el contexto de la gráfica por computadora y otros campos, las transformaciones bidimensionales se utilizan para manipular imágenes, figuras y coordenadas de manera eficiente. Estas transformaciones son fundamentales en áreas como la computación gráfica, el diseño asistido por computadora (CAD) y la geometría computacional. Existen varios tipos de transformaciones, como la traslación, rotación, escalamiento y reflexión, que permiten manipular objetos de manera precisa

<img width="393" height="263" alt="image" src="https://github.com/user-attachments/assets/6f01a2b3-9f9b-4282-ac5c-06a0e1701990" />

----
2.1.1. Traslación.
-----
La traslación o desplazamiento se refiere a mover un punto, un conjunto de puntos o un objeto compuesto, de su ubicación original hacia una nueva ubicación en su marco de referencia. La operación tiene un parámetro: el vector de desplazamiento.
Una traslación es el movimiento en línea recta de un objeto de una posición a otra. Se traslada cada punto P(x,y) dx unidades paralelamente al eje x y dy unidades paralelamente al eje y, hacia el nuevo punto P'(x',y').


Las ecuaciones quedan:
<img width="773" height="78" alt="image" src="https://github.com/user-attachments/assets/d10ae6e1-9417-4026-bf31-12e5c15b9843" />



Si se definen los vectores columna queda:
<img width="704" height="146" alt="image" src="https://github.com/user-attachments/assets/9ddc3262-2dba-4610-996d-b144f0f484bd" />



Entonces la ecuación 1 puede ser expresada como:

<img width="491" height="71" alt="image" src="https://github.com/user-attachments/assets/b6c01711-e588-4b4f-8e4b-6a4f3a6cf207" />



Una forma de efectuar la traslación de un objeto es aplicándole a cada punto del mismo la ecuación 1. Para trasladar todos los puntos de una línea, simplemente se traslada los puntos extremos

<img width="1029" height="413" alt="image" src="https://github.com/user-attachments/assets/0d5e0e6d-8e7e-4315-bf4a-db0d0fc90978" />


------
2.1.2. Escalamiento.
-----
El escalamiento es la operación que nos permite agrandar o empequeñecer un conjunto de puntos o un objeto compuesto. La operación requiere de dos parámetros: el factor de escalamiento a aplicar en x y el factor de escalamiento a aplicar en y. La operación requiere además, de un punto de referencia, típicamente el origen del marco de referencia. En el caso de aplicar escalamiento básico a un punto, se produce el efecto de acercarlo o alejarlo del punto de referencia
Cualquier valor numérico positivo puede asignarse a los factores de escalación Sx y Sy. Los valores menores que 1 reducen el tamaño de los objetos. Los valores mayores que 1 producen un agrandamiento. Si se especifica un valor de 1 para Sx y Sy se mantiene inalterado el tamaño de los objetos. Cuando a Sx y Sy se les asigna el mismo valor, se produce una escalación uniforme, la cual mantiene las propiedades relativas del objeto a escala

---
2.1.3. Rotación.
----
La rotación es la más compleja de las operaciones o transformaciones geométricas básicas. Consiste en girar un punto, un conjunto de puntos o un cuerpo compuesto, al rededor de un punto de referencia (el centro de rotación), típicamente el origen del marco de referencia.
La transformación de puntos de un objeto situados en trayectorias circulares es llama rotación. Este tipo de transformación se especifica con un ángulo de rotación, el cual determina la cantidad de rotación de cada vértice de un polígono. Se pueden hacer que los objetos giren alrededor de un punto arbitrario o el punto pivote de la transformación de rotación puede colocarse en cualquier parte en el interior o fuera de la frontera exterior de un objeto, el efecto de la rotación consiste en oscilar el objeto con respecto a este punto interno. Para rotar un objeto (en este caso bidimensional), se ha de determinar la cantidad de grados en la que ha de rotarse la figura. Para ello, y sin ningún tipo de variación sobre la figura, la cantidad de ángulo ha de ser constante sobre todos los puntos.

<img width="399" height="268" alt="image" src="https://github.com/user-attachments/assets/6760b3f8-2bf4-4e2e-ae8b-3f1705b44fc6" />

-----
2.1.4. Sesgado.
-----
El sesgado es un tipo de transformación no rígida, pues existe una deformación del objeto original al aplicar dicha transformación. Existen dos tipos de sesgo: sesgo horizontal y sesgo vertical.

Sesgo horizontal. Las coordenadas adyacentes al eje x permanecen fijas, los valores de y no cambian.

Sesgo vertical. Las coordenadas adyacentes al eje y permanecen fijas, los valores de x no cambian

<img width="505" height="351" alt="image" src="https://github.com/user-attachments/assets/4a028f43-cda9-4c6b-a308-8af3f9866f6f" />

-------
## 2.2 Representación matricial de las transformaciones bidimensionales
-----
REPRESENTACIÓN MATRICIAL

El uso de coordenadas homogéneas permite tratar todas las transformaciones geométricas como una multiplicación de matrices.
Las coordenadas agregan un tercer componente a las coordenadas bidimensionales.
De tal forma que, un punto (x,y) pasa a ser (x,y,W). El valor de W es generalmente 1.
Coordenadas homogéneas y representación matricial.

El uso de coordenadas homogéneas permite tratar todas las transformaciones geométricas como una multiplicación de matrices.
Las coordenadas agregan un tercer componente a las coordenadas bidimensionales.
De tal forma que, un punto (x,y) pasa a ser (x,y,W).
El valor de W es generalmente 1.
El uso de coordenadas homogéneas permite tratar todas las transformaciones geométricas como una multiplicación de matrices pues no todas las transformaciones son aplicaciones a un punto como una multiplicación de factores.

<img width="548" height="295" alt="image" src="https://github.com/user-attachments/assets/f922f0c1-bd67-44c7-97be-319bdf9decc1" />

----
2.3. Trazo de líneas curvas.
-----
Los puntos y las líneas rectas en la graficación de sistemas son fundamentales, pero las formas y modelados de figuras reales rara vez son únicamente compuestas por polígonos rectos. Así, usamos curvas creadas mediante expresiones matemáticas polinomiales que aproximan o interpolan los vértices o "puntos de control".

Estas expresiones matemáticas garantizan que se genere una línea fluida y sin vértices o puntas drásticas —una propiedad conocida como Continuidad, donde se busca al menos una curvatura suave de primera derivada (la tangente 
C
1
) y de la segunda derivada (
C
2
). El balance y uniones de estos polinomios modelan las "Curvas Spline".

------
2.3.1. Bézier.
------
Por lo general, una parte de una curva de Bézier se puede ajustar a cualquier número de puntos de control, aunque algunos paquetes gráficos limitan el número de puntos de control a cuatro. El grado del polinomio de Bézier se determina con el número de puntos de control que hay que aproximar y con su posición relativa.

<img width="797" height="343" alt="image" src="https://github.com/user-attachments/assets/51605a91-8c5a-402a-a28e-ffbb34c6affc" />

<img width="469" height="338" alt="image" src="https://github.com/user-attachments/assets/ac30c238-4310-4662-846e-95f58891eb0d" />

Una curva cuadrática de Bézier es el camino trazado por la función B(t), dados los puntos: P₀, P₁ y P₂,

B(t) = (1 − t)²P₀ + 2t(1 − t)P₁ + t²P₂, t ∈ [0,1].

Curvas cúbicas de Bézier

Cuatro puntos del plano o del espacio tridimensional, P₀, P₁, P₂ y P₃ definen una curva cúbica de Bézier. La curva comienza en el punto P₀ y se dirige hacia P₁ y llega a P₃ viniendo de la dirección del punto P₂. Usualmente, no pasará ni por P₁ ni por P₂. Estos puntos solo están ahí para proporcionar información direccional. La distancia entre P₀ y P₁ determina «qué longitud» tiene la curva cuando se mueve hacia la dirección de P₂ antes de dirigirse hacia P₃.

La forma paramétrica de la curva es:

B(t) = P₀(1 − t)³ + 3P₁t(1 − t)² + 3P₂t²(1 − t) + P₃t³, t ∈ [0,1].

Entre más puntos tenga el polígono de control más posibilidades hay para manipular las curvas de Bézier. Sin embargo, es igualmente claro que mientras mayor sea el grado, mayor será el coste computacional.

------
2.3.2. B-spline.
----
En el subcampo matemático del análisis numérico, una B-spline o base spline es una función spline que tiene un apoyo mínimo con respecto a un grado, suavidad y partición de dominio. Cualquier función spline de un grado dado se puede expresar como una combinación lineal de B-splines de ese grado. Los B-splines cardinales tienen nudos que son equidistantes entre sí. Los B-splines se pueden utilizar para el ajuste de curvas y la diferenciación numérica de datos experimentales.

En el diseño asistido por computadora y los gráficos por computadora, las funciones spline se construyen como combinaciones lineales de B-splines con un conjunto de puntos de control.

<img width="570" height="267" alt="image" src="https://github.com/user-attachments/assets/f0a59c94-bf5c-480c-b3ef-3f2a8448617a" />

----
2.4. Fractales
----
Un fractal es un objeto geométrico cuya estructura básica, fragmentada o irregular, se repite a diferentes escalas.[1] El término fue propuesto por el matemático Benoît Mandelbrot en 1975 y deriva del latín fractus, que significa quebrado o fracturado. Muchas estructuras naturales son de tipo fractal. La propiedad matemática clave de un objeto genuinamente fractal es que su dimensión métrica fractal es un número no entero.

Si bien el término "fractal" es reciente, los objetos hoy denominados fractales eran bien conocidos en matemáticas desde principios del siglo XX. Las maneras más comunes de determinar lo que hoy denominamos dimensión fractal fueron establecidas a principios del siglo XX en el seno de la teoría de la medida.

<img width="1030" height="245" alt="image" src="https://github.com/user-attachments/assets/d8633b5b-6da1-4a3f-8b2d-74a8fbb8f7b4" />

------
2.5. Uso y creación de fuentes de texto.
----
USO Y CREACIÓN DE FUENTES DE TEXTO También llamada tipografía, es una definición de los distintos caracteres que se pueden usar en un documento; de este modo, las distintas fuentes presentarán las letras con un dibujo o tipo de letra diferente. A cada símbolo individual se le llama caracter o procesador de textos de un tipo y tamaño determinados. Los archivos de tipografía son independientes de las aplicaciones que los usan, que normalmente se instalan en un determinado directorio del sistema operativo para que estén disponibles en todos los programas que los necesiten. Los más comunes son: -TTF (TrueType Font) -PostScript Type 1 -OTF (OpenType Font) Es un lenguaje de descripción de páginas (en inglés: Page Description Language, PDL), utilizado en muchas impresoras y, de manera usual, como formato de transporte de archivos gráficos en talleres de impresión profesional. OTF (Open Type Font) Es un formato de tipos de letra escalables para computadora; su arquitectura esta basada en la de su antecesor (True Type), cuya estructura básica conserva y la cual complementa con tablas de datos que permiten incorporar a un tipo o familia tipográfica funciones tipográficas y lingüísticas avanzadas. CONCLUSIÓN La tipografía depende de varias cosas como el color y la forma para poder reiterar el significado que se está tratando de transmitir; forma una parte importante de un mensaje de comunicación, esto incluye las formas, el color, la retórica de nuestro tipo de letra al escribir un mensaje

-----
## Bibliografía
-----
Foley, J. D., van Dam, A., Feiner, S. K., & Hughes, J. F. (1996). Computer graphics: Principles and practice (2nd ed.). Addison-Wesley.

Hearn, D., & Baker, M. P. (2011). Computer graphics with OpenGL (4th ed.). Pearson.

Rogers, D. F. (2001). An introduction to NURBS: With historical perspective. Morgan Kaufmann.

Piegl, L., & Tiller, W. (1997). The NURBS book (2nd ed.). Springer.

Farin, G. (2002). Curves and surfaces for CAGD: A practical guide (5th ed.). Morgan Kaufmann.

de Casteljau, P. (1986). Outillages méthodes calcul. En G. Farin (Ed.), Geometric modeling: Algorithms and new trends (pp. 7–22). SIAM.

Mandelbrot, B. B. (1983). The fractal geometry of nature. W. H. Freeman.

Barnsley, M. F. (1988). Fractals everywhere. Academic Press






