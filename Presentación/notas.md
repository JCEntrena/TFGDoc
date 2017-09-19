---
---

# Introducción

Buenos días, soy José Carlos Entrena, y voy a presentar mi trabajo de fin de grado
titulado Introducción a la homología singular, análisis y resolución del problema
del clique máximo. Como se puede apreciar, el trabajo consta de dos partes.
La primera de ellas es la parte matemática, que es una introducción a la teoría de
homología singular sobre espacios topológicos. La segunda
parte es la parte informática, donde hablaré del problema del clique máximo,
exponiendo distintos algoritmos para resolverlo y analizando los resultados que ofrecen.
<!---
Homología Singular.
--->

# Motivación

En esta parte, queremos estudiar la homología singular, para lo que necesitaremos primero construirla,
y después ser capaces de calcularla en ciertos casos, que se hará usando herramientas que se obtienen
a partir de su definición. Una vez tengamos esto, usaremos los grupos de homología de
las esferas, que habremos calculado, para obtener nuevos resultados.  

# Objetivos

Los objetivos que se plantearon al principio del trabajo fueron dos; el primero de ellos es
la construcción de la homología sobre un espacio topológico y el estudio de sus propiedades,
y el segundo de ellos aplicar estos resultados para calcular la homología de las esferas y obtener
una serie de teoremas a partir de esto.

Los dos objetivos se han completado y los iremos viendo a lo largo de la presentación.

# Definiciones

Vamos a comenzar definiendo la homología, para lo que necesitaremos introducir nuevos conceptos.
El primero de ellos es el concepto de p-símplice, que no es más que la envolvente convexa de p+1
puntos afínmente independientes. Si los puntos tienen el 0 en todas las coordenadas salvo en una,
en la que tienen un 1, lo llamaremos el p-símplice estándar y lo notaremos sigma sub p. Es equivalente
considerar símplices cualesquiera o símplices estándar, ya que podemos ir de unos a otros mediante
isomorfismos. En la imagen podemos ver representado el 2-símplice estándar.

Hecha esta definición, pasamos a los p-símplices singulares sobre un espacio topológico, que son
las aplicaciones continuas que parten de un p-símplice y van a parar a dicho espacio. Nos quedaremos
con el conjunto de p-símplices singulares, que notaremos f sub p.

Si tomamos una aplicación continua entre espacios topológicos, podemos llevarla al conjunto de p-símplices
singulares sin más que componerla con el p-símplice singular. Lo denotaremos poniendo una almohadilla a
la aplicación en cuestión.

Ya que el conjunto F sub p no tiene estructura algebraica, podemos tomar un Z-módulo sobre él, lo que nos
da como resultado el llamado grupo de p-cadenas singulares, que notaremos s sub p. Sobre este grupo es posible
definir un homomorfismo que llamamos borde, que viene dada por la suma de las caras de una cadena, en la que
vamos alternando el signo. Este homomorfismo verifica que al componerlo con sí mismo el resultado es siempre
cero. Esta propiedad será la que nos permita definir los grupos de homología.

Si nos volvemos a situar en el conjunto de p-cadenas s sub p, consideramos dos subconjuntos suyos; el grupo
de los p-ciclos, formado por las p-cadenas que tienen borde cero, y el grupo de los p-bordes, formado por las
p-cadenas que son el borde de una p+1 cadena.

Dado que el borde aplicado dos veces nos da la cadena cero, el grupo de los p-bordes es un subgrupo del grupo de
los p-ciclos, por lo que se puede tomar el conjunto cociente, que será el p-ésimo grupo de homología del espacio X.

Dada una aplicación entre espacios topológicos, esta induce un homomorfismo en los grupos de homología, que notamos
con un asterisco, y que se define utilizando el concepto de f almohadilla que veíamos antes.

Podemos realizar la misma construcción si en lugar de una espacio topológico tomamos un par, formado por un espacio
topológico X y un subconjunto suyo A. Se definen los grupos de p-cadenas del par sin más que tomar el cociente
entre los grupos de p-cadenas de X sobre los de A. La aplicación borde también puede tomarse aquí, y verifica
las mismas propiedades, lo que permite volver a tomar el cociente de los ciclos sobre los bordes y definir
la homología del par. Nuevamente, dada una aplicación de pares, que no es más que una aplicación continua que
verifica que la imagen de A está contenida en B, se define el homomorfismo inducido en la homología igual
que en el caso anterior.

# Axiomas

La construcción que hemos hecho cumple ciertas propiedades, que se pueden demostrar utilizando las construcciones hechas
y un resultado muy importante, el teorema de subdivisión baricéntrica. Estas propiedades aparecen en la literatura como
los axiomas de Eilenberg-Steenrod para la teoría de homología. El hecho de que se verifiquen estas propiedades hace
que tengamos una teoría de homología.

El primero de ellos es el axioma de identidad, por el cual la aplicación de pares identidad induce el
homomorfismo identidad en la homología.

El segundo axioma es el axioma de composición. Dadas dos aplicaciones de pares que puedan componerse, el
homomorfismo que induce la composición coincide con la composición de los homomorfismos inducidos.

El tercer axioma, llamado de exactitud, nos dice que dadas las inclusiones i y j, existe un homomorfismo delta
tal que la sucesión que vemos es exacta, esto es, que en cada punto la imagen del homomorfismo de entrada
coincide con el núcleo del homomorfismo de salida. A delta lo llamaremos el homomorfismo de conexión, y a
la sucesión, la sucesión exacta del par.

El cuarto axioma es el axioma de conmutatividad. Si consideramos una aplicación de pares f y su restricción a
A, estas conmutan con el homomorfismo delta del axioma anterior, lo que hace conmutativo el diagrama que vemos en pantalla.

El quinto axioma es el de homotopía, que nos dice que dos aplicaciones homotópicas inducen el mismo homomorfismo en la homología.

El sexto axioma, el axioma de escisión, toma U un subconjunto de X, que verifica que el cierre de U se queda dentro de A.
Bajo esta condición, si tomamos la inclusión entre el par (X-U, A-U) y (X, A), el homomorfismo inducido es un isomorfismo,
por lo que los grupos de homología de ambos pares coinciden.

El último axioma es el axioma de dimensión, que simplemente dice que todos los grupos de homología de un espacio puntual,
que aquí notamos con el 0, son el grupo trivial, salvo el 0-ésimo grupo de homología.

# Resultados

Con esto hemos construído una teoría de homología, y tenemos ciertas herramientas, como el teorema de escisión, con las
que se pueden obtener resultados. El primero de ellos será la homología de las esferas. Dada una esfera s n, se verifica
que tanto sus grupos 0-ésimo como n-ésimo son isomorfos a Z, y en otro caso son cero.

Usando la homología de las esferas podemos demostrar el teorema del punto fijo de Brower, por el cual se demuestra
que toda función continua de un disco en sí mismo tiene un punto fijo.

Además, se pueden demostrar los llamados teoremas de invarianza, entre los que destacan el teorema de invarianza de
la dimensión y el teorema de invarianza del dominio. El teorema de invarianza de la dimensión establece que si tenemos
dos abiertos homeomorfos de dos espacios euclídeos, entonces dichos espacios euclídeos tienen la misma dimensión.
Por otra parte, el teorema de invarianza del dominio nos dice que, dados dos subconjuntos de una esfera, uno de ellos
será abierto en la esfera sí y solo sí el otro lo es.

Finalmente, tenemos el teorema de separación de Jordan-Brower, por el cual si tenemos un embebimiento de la esfera n-1 ésima
en la esfera n-ésima, la imagen de dicho embebimiento divide a la esfera n-ésima en dos componentes conexas, cuya frontera común
es la propia imagen del embebimiento. Como consecuencia directa de este resultado, se obtiene una generalización del teorema
de la curva de Jordan para cualquier dimensión, en el cual el espacio de llegada es ahora R n.

Con esto concluye la parte de homología singular. Paso ahora al problema del clique máximo.


<!---
  Problema del clique máximo
--->


# Motivación

Vamos a empezar definiendo el concepto de clique, que es un grafo en el cual todos sus vértices están
conectados entre sí.

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
otros algoritmos. Distinguiremos entre algoritmos puros, que no permiten deshacer acciones
ya realizadas, y algoritmos relajados, que sí lo permiten.

El algoritmo básico trata de usar de forma sencilla los conceptos de los algoritmos greedy,
proporcionando un algoritmo que nos permite hacernos una idea de cómo funcionan los greedy
en este problema. Para resolverlo, parte desde un clique vacío y añade nodos hasta que no
se pueden añadir más.

El segundo algoritmo difiere del primero en que permite hacer intercambios, además de añadir nodos.
Esto hace que las decisiones tomadas se puedan deshacer, pues si un nodo ha entrado en el clique,
puede salir mediante un intercambio.

## Búsqueda local

La búsqueda local se centra en el entorno de una solución para buscar nuevas soluciones que mejoren
la actual. Este entorno puede definirse de diversas formas. En este caso, tenemos tres operadores
que nos permiten construir el entorno de una solución, los operadores add, swap y drop.

El primero de los algoritmos implementados es 1LS, que utiliza los tres operadores anteriores para
crear el entorno, ordenándolos por prioridad. Primero intentará añadir un nodo a la solución, y si
no es posible, tratará de hacer un intercambio, siempre que este permita añadir nodos al clique
resultante. Si no es posible, quitará un nodo del grafo.

El segundo algoritmo, DLS, utiliza solo los operadores add y swap, además de considerar una lista
tabú, para que los nodos que salgan del clique mediante un intercambio no puedan volver a él,
salvo que sea la única opción disponible. Se vuelve a dar prioridad a add sobre swap.

## Enfriamiento simulado

Los algoritmos de enfriamiento simulado también se basan en la búsqueda en el entornos, que difiere de
la búsqueda local en que utiliza un criterio probabilístico para aceptar las soluciones del entorno,
llamado el criterio de Metrópolis. Así, se permite aceptar soluciones peores, lo que puede hacer que el
algoritmo escape de óptimos locales. Al principio permitiremos que se acepten soluciones peores con
mayor frecuencia, para diversificar la búsqueda, mientras que al final la probabilidad será baja,
favoreciendo la intensificación.

El primer algoritmo implementado es un enfriamiento simulado básico, que utiliza los tres operadores
anteriores para crear el entorno, solo que en este caso elije un movimiento al azar en lugar de dar
distintas prioridades.

El segundo algoritmo es una versión adaptada, que trabaja con grafos cualesquiera en lugar de con cliques.
Así, aplicando los tres operadores, iremos obteniendo nuevos grafos, de los cuales obtendremos cliques
sin más que eliminar nodos hasta quedarnos con uno. Al igual que antes, los operadores se tomarán de
forma aleatoria.

## ILS

La búsqueda local iterada, o ILS, es un algoritmo de búsqueda local multiarranque, que utiliza una perturbación
de soluciones para obtener nuevas soluciones de partida de la búsqueda local. Así, partiendo de una solución
inicial, aplica una búsqueda local, después perturba la solución, le vuelve a aplicar una búsqueda local, etc.

En los dos algoritmos implementados, que usan las búsquedas locales que ya tenemos, la perturbación se hace
introduciendo un nuevo nodo a una solución y quitando los nodos que no estén conectados con él.

## GRASP

Los algoritmos GRASP son otro tipo de algoritmos multiarranque, que, en lugar de generar la solución de partida
mediante una perturbación, lo hacen construyéndola con un algoritmo greedy aleatorizado. En este caso, partirá
desde un clique vacío, y añadirá nodos al clique eligiendo uno aleatorio entre el 50% superior de los candidatos,
es decir, la mitad que tenga más adyacencias. Después, aplica una búsqueda local, que en nuestro caso serán
1LS y DLS, dando lugar a dos algoritmos.

## ACO

Los algoritmos de colonia de hormigas están basados en el comportamiento de las hormigas, utilizando un
recurso que simula a las feromonas que estas depositan cuando se desplazan. Cada nodo del grafo tendrá
un valor de feromonas, que nos permitirá calcular la probabilidad de que este nodo se añada al clique que
se esté construyendo, si es posible.

El primer algoritmo utiliza únicamente el valor de feromona para asignar probabilidades a cada nodo, dando
más probabilidad a los nodos con mayor nivel de feromonas.

El segundo algoritmo utiliza enfriamiento simulado para añadir un término que intervenga en el cálculo de la
probabilidad. Así, además del valor de feromonas se utiliza información del grafo, cuya importancia desciende
en conforme avanza el algoritmo.

## Genéticos

Finalmente, tenemos los algoritmos genéticos, que están basados en los procesos evolutivos presentes en la
naturaleza. Partiremos de una población formada por soluciones, y las combinaremos dos a dos para obtener
nuevas soluciones que pasen a la siguiente generación.

En nuestro algoritmo, los hijos competirán directamente con los padres, y serán los dos mejores los que avancen
a la siguiente generación.

Combinando los algoritmos genéticos con búsqueda local, obtenemos los algoritmos meméticos. Partiendo del
algoritmo genético anterior, se ha construído un algoritmo memético combinando este con la búsqueda local DLS,
para intentar mejorar los elementos de la población. Aplicaremos DLS a todos los individuos cada vez que se
cree una nueva generación.

# Implementación

Estos son todos los algoritmos considerados. Para la obtención de resultados, se han programado todos ellos
en el lenguaje de programación Ruby, un lenguaje orientado a objetos e interpretado. Todos ellos se han ejecutado
sobre 35 grafos del benchmark DIMACS, que es el utilizado por la comunidad científica a la hora de evaluar
nuevos algoritmos.

# Resultados

Pasamos ya a los resultados. En la tabla vemos los resultados que da cada algoritmo al considerarlo individualmente;
como medidas, se han tomado el número de grafos en los que el algoritmo alcanza el óptimo, y el tamaño medio
de los cliques que encuentra en comparación con el óptimo.

Para comparar los algoritmos entre sí, hemos tomado los tres mejores algoritmos en cada uno de los grafos considerados,
tomando los que daban cliques de mayor tamaño, y quedándonos con el más rápido en caso de empate. Se han recopilado
el número de posiciones totales en esta tabla. Los algoritmos basados en búsquedas locales consiguen buenos resultados
gracias a su velocidad, lo que les hace quedar por delante en los grafos sencillos. En los grafos más complejos,
son el genético y el memético los que obtienen mejores cliques y quedan por delante del resto.

# Vías futuras

Para ampliar este trabajo se pueden considerar dos vías distintas; la primera sería enfatizar en un tipo concreto de
algoritmos, introduciendo nuevas componentes y ajustando mejor los parámetros. La segunda consiste en añadir nuevos
algoritmos para poder hacer una comparación más amplia.

Eso ha sido todo, gracias por su atención y estoy abierto a cualquier pregunta.
