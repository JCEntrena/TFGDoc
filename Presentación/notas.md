---
---

# Introducción

Este trabajo consta de dos partes. La primera de ellas es la parte matemática,
que trata la teoría de homología singular sobre espacios topológicos. La segunda
parte es la parte informática, donde se hablará del problema del clique máximo,
exponiendo distintas formas de resolverlo y analizando los resultados que ofrecen.

En primer lugar se expondrá la parte sobre homología singular, y después seguiremos
con el problema del clique máximo. Cada parte del trabajo puede verse como un trabajo
independiente del otro.

<!---
Homología Singular.
--->


# Motivación

En esta parte, el objetivo principal es construir y estudiar la teoría de homología singular.
Para su construcción, se definirá el concepto de p-símplice singular, y a partir de él se
harán construcciones algebraicas que nos lleven a los grupos de homología.


Una vez los tengamos construídos, estudiaremos algunas de sus propiedades
y demostraremos una serie de resultados, siendo el más importante de ellos el teorema de subdivisión
baricéntrica. Este teorema nos permite obtener herramientas para el cálculo de la homología singular,
las cuales se han aplicado al caso particular de las esferas. Tras esto se probarán algunos resultados
clásicos, usando los grupos de homología de las esferas, los resultados previos e introduciendo
nuevos conceptos.

# Objetivos

Los objetivos que se plantearon al principio de la memoria fueron dos; el primero de ellos es
la construcción de los grupos de homología sobre un espacio topológico y el estudio de sus propiedades,
para después utilizar lo obtenido sobre casos concretos, en particular el cálculo de la homología de
las esferas y la obtención de resultados clásicos de matemáticas.

# Definiciones

Comenzamos con las definiciones iniciales, de forma resumida. Partimos del concepto de p-símplice,
que es la envolvente convexa de p+1 puntos afínmente independientes. A las aplicaciones continuas
de un p-símplice en un espacio topológico las llamaremos p-símplices singulares. Si tomamos el conjunto
de los p-símplices singulares, el grupo abeliano libre generado por este conjunto es el llamado
grupo de p-cadenas singulares del espacio topológico en el que estemos trabajando.

Sobre el grupo de p-cadenas singulares podemos definir un homomorfismo al que llamaremos borde,
que lleva una p-cadena a una p-1 - cadena sin borde. De esta forma, al componer el borde con sí
mismo obtendremos como resultado el homomorfismo cero.

A la familia formada por el grupo de p-cadenas singulares y el homomorfismo borde la llamaremos el
complejo de cadenas singular asociado a un espacio topológico. Gracias a que al aplicar el borde
dos veces a una cadena da como resultado la cadena cero, se pueden definir los grupos de los ciclos
y los bordes.




<!---
  Problema del clique máximo
--->


# Motivación

Vamos a empezar definiendo el concepto de clique. Dado un grafo cualquiera, diremos que un subgrafo
suyo es un clique si todos sus vértices están conectados entre sí. Un clique puede ser maximal, cuando
no está contenido dentro de un clique mayor, y puede ser máximo, si no existe ningún clique de mayor
tamaño dentro del grafo.

El problema del clique máximo consiste en encontrar el clique de mayor tamaño dentro de un grafo.
En este ejemplo podemos ver como existen varios cliques dentro del grafo, como el formado por los
nodos a, b y d, o el clique máximo de tamaño cuatro formado por b, d, e y g.


Se sabe que es un problema NP-difícil, y de hecho no es aproximable con factor 1 - épsilon salvo que
la clase NP y la clase ZPP sean la misma, donde ZPP es la clase de complejidad de los problemas
que se pueden reconocer con un algoritmo polinómico aleatorizado.

Debido a que el problema es NP-difícil, a la hora de resolverlo no lo haremos de forma exacta, sino
utilizando técnicas heurísticas que puedan conseguir buenas soluciones en un tiempo razonable.
En este trabajo se han implementado algoritmos basados en distintas metaheurísticas con la idea
de evaluar su rendimiento a la hora de resolver el problema.


# Objetivos

Al principio del trabajo se plantearon cuatro objetivos. El primero de ellos es la recopilación
de información sobre el problema, tanto teórica como de las formas ya existentes de resolverlo.
Como segundo objetivo tenemos el estudio de las técnicas obtenidas anteriormente y una selección
de un número de ellas para implementar en este trabajo. El tercer objetivo es el diseño e
implementación de estas técnicas, El último objetivo es ejecutar los algoritmos para obtener
resultados y poder evaluarlos.

De todos los objetivos, el primero se ha cumplido parcialmente, pues me he centrado más en la
parte de las heurísticas que se aplican al problema que en la parte teórica. He priorizado
los algoritmos por ser lo que se utiliza en el resto del trabajo. El resto de objetivos se
han llevado a cabo satisfactoriamente, mediante el estudio de artículos que implementaban algoritmos,
la elección de un total de 14 técnicas a implementar, su implementación, ejecución y análisis de resultados.

Aquí no detallaré todo el trabajo realizado, sino que me centraré en hacer una descripción breve
de todos los algoritmos y en ver los resultados que nos ofrecen. Para evaluar los resultados he utilizado
los grafos del repositorio DIMACS, que son los que utiliza la comunidad científica a la hora de probar
nuevos algoritmos.

# Algoritmos

Paso ya a explicar los distintos algoritmos considerados para este trabajo. Como he dicho antes, he
tomado 14 algoritmos, que están divididos en 7 categorías distintas, habiendo 2 algoritmos en cada
una de ellas. Las vemos una a una:

## Greedy

Los algoritmos greedy son aquellos que resuelven problemas tomando las decisiones óptimas
en cada instante, lo que no lleva necesariamente a un óptimo global, pero en ocasiones
nos permite aproximarlo de forma razonable en un periodo de tiempo pequeño, en comparación a
otros algoritmos.

Normalmente los algoritmos greedy no permiten deshacer acciones ya realizadas, aunque en ocasiones
esta condición puede no tomarse, lo que nos hace distinguir entre algoritmos puros y relajados.
Los dos algoritmos considerados pertenecen uno a cada clase.

El algoritmo básico trata de usar de forma sencilla los conceptos de los algoritmos greedy,
proporcionando un algoritmo que nos permite hacernos una idea de cómo funcionan los greedy
en este problema. Para resolverlo, parte desde un clique vacío y añade nodos hasta que no
se pueden añadir más.

El segundo algoritmo difiere del primero en que permite hacer intercambios, además de añadir nodos.
Esto hace que las decisiones tomadas se puedan deshacer, pues si un nodo ha entrado en el clique,
puede salir mediante un intercambio.

## Búsqueda local

La búsqueda local se centra en el entorno de una solución para buscar nuevas soluciones que mejoren a
la actual.  


# Implementación

(Breve)


# Resultados
