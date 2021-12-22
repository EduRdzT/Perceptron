# Perceptron
#### `Perceptrón con Matlab`

**Índice**
- [Introducción](#id1)
- [Desarrollo Experimental](#id2)
- [Análisis y Resultados](#id3)
- [Códigos](#id4)
- [Conclusiones](#id5)
- [Referencias](#id6)

## INTRODUCCIÓN<a name="id1"></a>

El perceptrón es la forma más simple de una red neuronal usada para la clasificación de un tipo especial de patrones, los linealmente separables (es decir, patrones que se encuentran a ambos lados de un hiperplano). Básicamente, consiste de una neurona con pesos sinápticos y umbral ajustables, como se muestra en la figura (4.1). El algoritmo usado para ajustar los parámetros libres de esta red neuronal apareció por primera vez en un procedimiento de aprendizaje desarrollado por Rosenblatt (1958) para su modelo de perceptrón del cerebro. En realidad, Rosenblatt demostró que, si los patrones usados para entrenar el perceptrón son sacados de dos clases linealmente separables, entonces el algoritmo del perceptrón converge y toma como superficie de decisión un hiperplano entre estas dos clases. La prueba de convergencia del algoritmo es conocida como el teorema de convergencia del perceptrón.

![Arquitectura ALU](/Img/Imagen1.png)

El perceptrón de una capa descrito en la figura (4.1) tiene sólo una neurona. Dicho perceptrón está limitado a realizar clasificación de patrones con sólo dos clases. Expandiendo la capa de salida del perceptrón para incluir más que una neurona, podemos realizar dicha clasificación con más de dos clases. Sin embargo, las clases tendrían que ser linealmente separables para que el perceptrón trabaje correctamente.

El **funcionamiento** del perceptrón es muy sencillo, simplemente lee los valores de entrada, suma todas las entradas de acuerdo a unos pesos y el resultado lo introduce en una función de activación que genera el resultado final.

El **entrenamiento** del perceptrón no es más que determinar los pesos sinápticos y el umbral que mejor hagan que la entrada se ajuste a la salida. Para la determinación de estas variables, se sigue un proceso adaptativo. El proceso comienza con valores aleatorios y se van modificando estos valores según la diferencia entre los valores deseados y los calculados por la red.

En resumen, el perceptrón aprende de manera iterativa siguiendo estos pasos:

1. Inicializar pesos y umbrales
2. Bucle: hasta resultado de pesos sea aceptable
    - Bucle: para todos los ejemplos
        - Leer valores de entrada
        - Calcular error
        - Actualizar pesos según el error
        - Actualizar pesos de entradas
        - Actualizar el umbral

Conjunto de entradas x1,…xn

    Representan las entradas de la red neuronal.

Pesos sinápticos w1,…wn

    Cada entrada tiene un peso que se va ajustando de forma automática a medida que la red neuronal va aprendiendo.

Función de agregación, Σ

    Realiza el sumatorio de todas las entradas ponderadas por sus pesos.

Función de activación, g (.)

    Se encarga de mantener el conjunto de valores de salida en un rango determinado, normalmente (0,1) o (-1,1)
    Existen diferentes funciones de activación que cumplen este objetivo, la más habitual es la función sigmoide.

Salida, Y

    Representa el valor resultante tras pasar por la red neuronal.
    
![Arquitectura ALU](/Img/Imagen2.png)

## DESARROLLO EXPERIMENTAL<a name="id2"></a>

El análisis de un proceso de destilación fraccionada de la gasolina reveló que un aceite determinado podría clasificarse en dos clases de pureza {P1 y P2} a partir de la medición de tres variables {x1, x2 y x3}, que representan algunas propiedades fisicoquímicas del aceite. El equipo de ingenieros y científicos propuso la aplicación de una red Perceptrón para realizar la clasificación automática de ambas clases.

Así, con base en la información recopilada sobre el proceso, el equipo compuso el conjunto de entrenamiento presentado en el Apéndice A, utilizando una convención donde el valor -1 indica aceite perteneciente a la clase P1 y el valor 1 indica aceite perteneciente a la clase P2.

Por lo tanto, la neurona que implementa el perceptrón tiene tres entradas y una salida, como se ilustra en la figura 3.8.

Utilice el algoritmo de Hebb supervisado (regla de Hebb) para la clasificación de patrones y, suponiendo que la tasa de aprendizaje sea de 0,01, realice las siguientes tareas:

1. Ejecutar cinco procesos de entrenamiento para la red Perceptrón, inicializando el vector de peso {w} con valores aleatorios entre cero y uno para cada proceso de entrenamiento. Si es necesario, actualice el generador de números aleatorios en cada proceso para que los elementos iniciales que componen el vector sean diferentes en cada entrenamiento. El conjunto de entrenamiento se encuentra en el Apéndice A.
2. Registre los resultados de los cinco procesos de capacitación en la Tabla 3.2.

## ANÁLISIS Y RESULTADOS<a name="id3"></a>

#### Tablas de resultados

<table>
<thead>
  <tr>
    <th rowspan="2">&nbsp;&nbsp;&nbsp;<br>Entrenamiento&nbsp;&nbsp;&nbsp;</th>
    <th colspan="4">&nbsp;&nbsp;&nbsp;<br>Vector de&nbsp;&nbsp;&nbsp;pesos (inicial)&nbsp;&nbsp;&nbsp;</th>
    <th colspan="4">&nbsp;&nbsp;&nbsp;<br>Vector de&nbsp;&nbsp;&nbsp;pesos (final)&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>Numero de épocas&nbsp;&nbsp;&nbsp;</th>
  </tr>
  <tr>
    <th colspan="2">&nbsp;&nbsp;&nbsp;<br>w0&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>w2&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>w3&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>w0&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>w1&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>w2&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br>w3&nbsp;&nbsp;&nbsp;</th>
    <th>&nbsp;&nbsp;&nbsp;<br> &nbsp;&nbsp;&nbsp;</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>#1 (T1)&nbsp;&nbsp;&nbsp;</td>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>0.3&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.5&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.6&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-30.5&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>15.4997  &nbsp;&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>24.5969  &nbsp;&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-7.2811&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>405&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>#2 (T2)&nbsp;&nbsp;&nbsp;</td>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>0.6787&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.7431&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.3922&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-30.7213&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>15.3368&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>24.6232&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-7.3041&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>390&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>#3 (T3)&nbsp;&nbsp;&nbsp;</td>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>0.2769&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.0971&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.8235&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-30.9231&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>15.6811&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>24.8693&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-7.3783&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>402&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>#4 (T4)&nbsp;&nbsp;&nbsp;</td>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>0.4387&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.7655&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.7952&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-30.5613&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>15.8224&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>24.7890&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-7.3134&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>400&nbsp;&nbsp;&nbsp;</td>
  </tr>
  <tr>
    <td>&nbsp;&nbsp;&nbsp;<br>#5 (T5)&nbsp;&nbsp;&nbsp;</td>
    <td colspan="2">&nbsp;&nbsp;&nbsp;<br>0.1869&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.4456&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>0.6463&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-29.4131&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>14.1869&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>24.3706&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>-7.0430&nbsp;&nbsp;&nbsp;</td>
    <td>&nbsp;&nbsp;&nbsp;<br>355&nbsp;&nbsp;&nbsp;</td>
  </tr>
</tbody>
</table>

_Tabla 3.2 Resultados para el entrenamiento del perceptron_

|     Muestra    |        x1      |        x2      |       x3      |     y (T1)    |     y (T2)    |     y (T3)    |     y (T4)    |     y (T5)    |
|:--------------:|:--------------:|:--------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
|        1       |     -0.3665    |      0.0620    |     5.9891    |       P2      |       P2      |       P2      |       P2      |       P2      |
|        2       |     -0.7842    |      1.1267    |     5.5912    |       P2      |       P2      |       P2      |       P2      |       P2      |
|        3       |      0.3012    |      0.5611    |     5.8234    |       P2      |       P2      |       P2      |       P2      |       P2      |
|        4       |      0.7757    |      1.0648    |     8.0677    |       P2      |       P2      |       P2      |       P2      |       P2      |
|        5       |      0.1570    |      0.8028    |     6.3040    |       P2      |       P2      |       P2      |       P2      |       P2      |
|        6       |     -0.7014    |      1.0316    |     3.6005    |       P2      |       P2      |       P2      |       P2      |       P2      |
|        7       |      0.3748    |      0.1536    |     6.1537    |       P2      |       P2      |       P2      |       P2      |       P2      |
|     8          |     -0.6920    |     0.9404     |     4.4058    |     P2        |     P2        |     P2        |     P2        |     P2        |
|     9          |     -1.3970    |     0.7141     |     4.9263    |     P2        |     P2        |     P2        |     P2        |     P2        |
|     10         |     -1.8842    |     -0.2805    |     1.2548    |     P1        |     P1        |     P1        |     P1        |     P1        |

_Tabla 3.3 Muestra de aceite para validar la red Perceptrón_

3. Después del entrenamiento el Perceptrón puso en funcionamiento la red para clasificar las muestras de aceite de la Tabla 3.3, indicando en esta tabla los valores de salida (clases) de los cinco procesos de entrenamiento realizados en el ítem 1.

## CÓDIGOS<a name="id4"></a>

#### Código de Perceptrón
```M
%---------------------- Inicializar constantes ----------------------------
teta = -1;
p1 = [1:1];
p2 = [1:1];
%--------------------- Inicializar los valores ----------------------------
a = xlsread('muestras','B2:D11');
[b,c] = size(a);
%-------------------- Inicializacion de las matrices ----------------------
t = teta*ones(b,1);                         %Matriz de teta = -1
x = cat(2,t,a);                %Matriz de los valores de entrada concatenado con la matriz de teta
% w = [0.3,0.4,0.5,0.6];                      %Matriz de pesos
%------------------------- Codigo principal -------------------------------
for j = 1:b                                 %Este for pasa de muestra en muestra
    y = 0.0000;
%--------------- Multiplicacion de las entradas y los pesos ---------------
    for k = 1:c
        u = w(1,k) * x(j,k);
        y = y + u;
     end
%---------------- Acerca el valor de y a valores de 1 o -1 ----------------
     if y >= 0.0000
         p2 = cat(1, p2, j);
     else
         p1 = cat(1, p1, j);
     end
end
[d,e] = size(p1);                     % Obtencion de la cantidad de valores de 1
[f,g] = size(p2);                    % Obtencion de la cantidad de valores de -1
p1(2:d,e)
p2(2:f,g)
```
#### Código de pesos del perceptrón
```m
clear all
clc
%---------------------- Inicializar constantes ----------------------------
n = 0.1;
teta = -1;
epoch = 0;
i = 1;
%--------------------- Inicializar los valores ----------------------------
a = xlsread('Iris','A2:D101');
[b,c] = size(a);
%-------------------- Inicializacion de las matrices ----------------------
t = teta*ones(b,1);                         %Matriz de teta = -1
x = cat(2,t,a(1:b,1:(c-1)));                %Matriz de los valores de entrada concatenado con la matriz de teta
d = a(1:b,c);                               %Matriz de valores esperados
% w = rand(1,c)                              %Matriz de pesos aleatorios
w = [10.5, 1, 1, 1];                      %1.1000    2.9942    6.4002   -0.8599 ; 0.5000    2.9600    8.4604   -1.1504
%------------------------- Codigo principal -------------------------------
while i > 0                                 %Mientras no coincidan los pesos con cada punto no sale del while
    i = 0;
    for j = 1:b                             %Este for pasa de punto en punto
        y = 0.0000;
%--------------- Multiplicacion de las entradas y los pesos ---------------
        for k = 1:c                         
            u = w(1,k) * x(j,k);
            y = y + u;
        end
%---------------- Acerca el valor de y a valores de 1 o -1 ----------------
            if y >= 0.0000
                y = 1;
            else
                y = -1;
            end
%- Si el valor obtenido es diferente al esperado se actualizan los pesos --
        if y ~= d(j,1)
            for k = 1:c
                w(1,k) = w(1,k) + n * (d(j,1) - y) * x(j,k);
            end
           i = 1;                          %Si se actualizan los pesos, 'i' no dejara que se salga del while principal 
                                            %para repetir todo el proceso denuevo
        end
    end
    epoch = epoch + 1;                     %Iteracion de las epocas
end
w                                          %Impresion de los pesos finales
epoch
```

## CONCLUSIONES<a name="id5"></a>

La teoría de Redes Neuronales Artificiales presenta grandes ventajas con respecto a otros modelos típicos de solución de problemas de Ingeniería, una de ellas es su inspiración en modelos biológicos del funcionamiento del cerebro, lo que facilita su estudio debido a las analogías que pueden introducirse para su análisis.

Los modelos matemáticos en que han sido desarrollados los algoritmos para todos los tipos de redes son modelos sencillos, que, aunque exigen cierto grado de conocimientos de cálculo diferencial, pueden ser asimilados y desarrollados en cualquier lenguaje de programación.

Las redes neuronales son una teoría relativamente nueva que junto a otras técnicas de inteligencia artificial ha generado soluciones muy confiables a problemas de Ingeniería, los cuales, a pesar de poder ser solucionados por métodos tradicionales, encuentran en las redes neuronales una alternativa fácil de implementar y altamente segura.

## REFERENCIAS<a name="id6"></a>

> Diego Calvo. (2018). Perceptrón – Red neuronal. Noviembre 09, 2020, de Diego Calvo Sitio web: https://www.diegocalvo.es/perceptron/

> Anónimo. (2018). El perceptrón. Diciembre 09,2020, de Bibling Sitio web: http://bibing.us.es/proyectos/abreproy/11084/fichero/Memoria+por+cap%C3%ADtulos+%252FCap%C3%ADtulo+4.pdf+

> Introduction to Statistical Learning Gareth James, Daniela Witten, Trevor Hastie and Robert Tibshirani Support Vector Machines Succinctly by Alexandre Kowalczyk
