---
title: "Unidad 2: Derivadas"
autor: "José Juarez"
version: "17/06/25"
---

<span hidden>Local path of the file: "H:/im/mat5/"</span>
<span hidden>Local path of images: "H:/im/mat5/_i/"</span>


<br>

<span hidden>Image</span>
   <center>![](https://i.pinimg.com/736x/71/64/18/7164184bf63088c42087214ebd6d41a5.jpg){width=500px}</center>
   <center><span class="grey3 size70">Neumático de un dragster al acelerar a fondo. Las derivadas nos permiten estudiar la rapidez con que cambia la velocidad. Fuente: Pinterest.com</span></center>

<br>

## ¿Por qué estudiar derivadas?

Las derivadas son una herramienta poderosa para **entender y predecir cómo cambian las cosas**.

En las carreras de dragsters, dos autos compiten acelerando en línea recta durante solo 305 metros (1/4 de milla). No gana el que tiene mayor velocidad final, sino el que acelera más rápido desde el inicio.

En la vida real hay muchas situaciones que, como en los dragsters, lo importante es la **rapidez con que se pasa de una situación a otra**. Por ejemplo la agresividad de un virus está relacionada con la **rapidez** con que puede infectar un misma cantidad de población.

El estudio preciso de estos fenómenos es posible gracias al cálculo diferencial o derivadas. 


<br><br>


## 1. Conceptos Previos

### 1.a) Pendiente de una recta a partir de su gráfica

<br><span class="grey3 size70">🔁 Repaso:</span>

<center>![](deriv_pendiente_recta_grafic.png){width=400px}</center>
 
La pendiente mide la inclinación de una recta y se calcula como: $
Pendiente = \frac{\Delta y}{\Delta x}$

donde:

* $\Delta y$ es el cambio en la variable vertical (eje y),
* $\Delta x$ es el cambio en la variable horizontal (eje x),

Puedes repasar esto en este [video](https://es.khanacademy.org/math/algebra/x2f8bb11595b61c86:linear-equations-graphs/x2f8bb11595b61c86:slope/v/positive-and-negative-slope) donde además verás como puede ser positiva y negativa.

<br><span class="grey3 size70">📝 Práctica:</span>

Resuelve estos [ejercicios](https://es.khanacademy.org/math/algebra/x2f8bb11595b61c86:linear-equations-graphs/x2f8bb11595b61c86:slope/e/slope-from-a-graph)

<br>

### 1.b) Pendiente de una recta a partir de dos puntos

<br><span class="grey3 size70">🔁 Repaso:</span>

<center>![](deriv_pendiente_recta_2ptos.svg){width=400px}</center>
 
En una recta que pasa por dos puntos $(x_1, y_1)$ y $(x_2, y_2)$, se calcula como: $m = \frac{y_2 - y_1}{x_2 - x_1}$

**Relación con la tangente:** La pendiente de la recta es igual a la tangente del ángulo "α" que forma la recta con la horizontal.

<br><span class="grey3 size70">📝 Práctica:</span>

Resuelve estos [ejercicios](https://es.khanacademy.org/math/algebra/x2f8bb11595b61c86:linear-equations-graphs/x2f8bb11595b61c86:slope/e/slope-from-two-points)

<br>

### 1.c.) Recta tangente

<br><span class="grey3 size70">🔁 Repaso:</span>

<center>![](deriv_recta_tangente.svg){width=400px}</center>

La recta tangente a una curva en un punto es la recta que:

- toca la curva solo en ese punto (o en un entorno muy pequeño),
- y tiene la misma dirección instantánea que la curva en ese lugar.

> Es como apoyar una regla sobre una curva sin que la atraviese: la dirección que toma la regla en ese punto es la de la recta tangente.


<br><br>


## 2. Definir tasas de cambio promedio e instantáneas en un punto

<br><span class="grey3 size70">🔁 Repaso:</span>

- La tasa de cambio promedio se corresponde con la velocidad promedio de Usain Bolt y es una pendiente en la gráfica. Pero la velocidad que tiene realmente en cada instante es distinta a la velocidad promedio. Esta velocidad en cada instante se puede pensar como la tasa instantánea de cambio y coincide con la pendiente de la recta tangente en un punto dado y esto es la derivada. Puedes repasarlo en detalle [aquí](https://www.youtube.com/watch?v=z0pdqj3zH3s).

- La tasa de cambio promedio es la pendiente de una recta secante que pasa por dos puntos. Cuando acercamos más y más los dos puntos la recta secante pasa a ser la recta tangente. Puedes repasarlo [aquí](https://www.youtube.com/watch?v=-9sVJ4--YTE)

<br><span class="grey3 size70">📝 Práctica:</span>

Resuelve estos [ejercicios](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-1-new/ab-2-1/e/secants-and-average-rate-of-change) en la carpeta.


<br><br>


## 3. Cálculo de la derivada por definición

<br><span class="grey3 size70">🔁 Repaso:</span>

La derivada de una función $f(x)$ en un punto $x = a$ es:

$$
f'(a) = \lim_{h \to 0} \frac{f(a + h) - f(a)}{h}
$$

**Ejemplo:**

Calcular la derivada de $f(x) = x^2$ en $x = 2$ usando la definición.

$$
f'(2) = \lim_{h \to 0} \frac{(2+h)^2 - 4}{h} = \lim_{h \to 0} \frac{4 + 4h + h^2 - 4}{h} = \lim_{h \to 0} \frac{4h + h^2}{h} = \lim_{h \to 0}(4 + h) = 4
$$

<br><span class="grey3 size70">📝 Práctica:</span>

1. Calcula la derivada de $f(x) = 3x + 1$ usando la definición.
2. Calcula la derivada de $f(x) = x^2 + 2x$ en $x = 1$.


<br><br>


## 4. Reglas de derivación

<br><span class="grey3 size70">🔁 Repaso:</span>

Recuerda que dada una función $y(x)$ se puede indicar su derivada como $y'$ o como $\frac{dy}{dx}$.

**Tabla de derivadas básicas:**

| Función         | Derivada      |
| --------------- | ------------- |
| $a$ (constante) | $0$           |
| $ax$            | $a$           |
| $x^n$           | $nx^{n-1}$    |
| $\sin x$        | $\cos x$      |
| $\cos x$        | $-\sin x$     |
| $e^x$           | $e^x$         |
| $\ln x$         | $\frac{1}{x}$ |
| $\log_b(x)$     | $\dfrac{1}{x \ln b}$ |
| $a^x$           | $a^x \ln a$   |

**Reglas de combinación:**

Dadas las funciones $f$ y $g$:

* **Suma/resta**: $(f \pm g)' = f' \pm g'$
* **Producto**: $(fg)' = f'g + fg'$
* **Cociente**: $\left(\frac{f}{g}\right)' = \frac{f'g - fg'}{g^2}$

<br><span class="grey3 size70">📝 Práctica:</span>

1. Encuentra el error en los cálculos de derivadas [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-1-new/ab-2-6a/e/differentiating-linear-functions). No hace falta hacerlo en la carpeta.

2. Encuentra estas derivadas de polinomios [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-1-new/ab-2-6b/e/power-rule-basic).

3. Encuentra estas derivadas donde la x puede aparecer en el denominador [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-1-new/ab-2-6b/e/differentiate-radical-functions-intro).

4. Encuentra estas derivadas donde aparece senos y cosenos [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-1-new/ab-2-7/e/differentiate-sine-and-cosine)

5. Aplicar la regla del producto [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-1-new/ab-2-8/e/differentiate-products).

6. Aplica la regla de la división [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-1-new/ab-2-9/e/differentiate-quotients).

7. Aplica todo lo aprendido [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-1-new/ab-2-9/e/differentiate-rational-functions).


<br><br>


## 5. Regla de la cadena

<br><span class="grey3 size70">🔁 Repaso:</span>

Se usa cuando hay funciones compuestas:

$$
\frac{d}{dx}[f(g(x))] = f'(g(x)) \cdot g'(x)
$$

**Ejemplo:**

$$
y = \sin(x^2) \Rightarrow y' = \cos(x^2) \cdot 2x
$$

Puedes repasarlo [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-2-new/ab-3-1a/v/chain-rule-introduction). También este [video](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-2-new/ab-3-1a/v/common-chain-rule-misunderstandings) te va a orientar sobre algunos errores comunes.

<br><span class="grey3 size70">📝 Práctica:</span>

1. Resuelve estos 4 [ejercicios](https://es.khanacademy.org/math/ap-calculus-ab/ab-differentiation-2-new/ab-3-1a/e/differentiate-composite-functions-intro)

2. Resuelve:

   - **a)** $f(x) = (3x + 2)^4$
   - **b)** $f(x) = \sin(5x^2)$
   - **c)** $f(x) = e^{\ln(x^2 + 1)}$
   - **d)** $f(x) = \sqrt{\tan(2x)}$
   - **e)** $f(x) = \ln\left[\left(2x^2 + 3\right)^5 \cdot \sqrt{\sin x}\right]$


<div hidden>

## **5. Regla de L’Hôpital**

Se usa en límites indeterminados como $\frac{0}{0}$ o $\frac{\infty}{\infty}$.

$$
\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)} \quad \text{(si el límite existe)}
$$

### **Ejemplo:**

$$
\lim_{x \to 0} \frac{\sin x}{x} = \frac{\cos x}{1} = 1
$$

---

## **6. Aplicaciones: Máximos y mínimos**

Se usa la derivada para encontrar **extremos relativos**.

### **Pasos:**

1. Derivar la función: $f'(x)$
2. Igualar a cero: $f'(x) = 0$
3. Analizar los signos de la derivada antes y después de cada raíz.

### **Ejemplo:**

$f(x) = -x^2 + 4x$

* $f'(x) = -2x + 4$
* $f'(x) = 0 \Rightarrow x = 2$
* Máximo relativo en $x=2$, ya que cambia de positivo a negativo.

---

## **7. Ejercicios**

### **7.1. Derivadas por definición**

1. Calcula la derivada de $f(x) = 3x + 1$ usando la definición.
2. Calcula la derivada de $f(x) = x^2 + 2x$ en $x = 1$.

### **7.2. Reglas de derivación**

3. Deriva $f(x) = x^3 - 5x + 6$
4. Deriva $f(x) = \frac{1}{x}$
5. Deriva $f(x) = e^{2x} + \ln(x^2)$

### **7.3. Regla de la cadena**

6. Deriva $f(x) = \sqrt{3x + 2}$
7. Deriva $f(x) = \ln(\sin x)$

### **7.4. L’Hôpital**

8. $\lim_{x \to 0} \frac{e^x - 1}{x}$
9. $\lim_{x \to \infty} \frac{x}{e^x}$

### **7.5. Máximos y mínimos**

10. Determina los extremos relativos de $f(x) = x^3 - 3x^2 + 2$

---

## **8. Problemas desafiantes**

### **A. Función no explícita**

> Sea $x^2 + y^2 = 25$. Halla $\frac{dy}{dx}$.

(Sugerencia: derivación implícita)

---

### **B. Optimización**

> Una hoja rectangular tiene que tener 20 cm² de área. ¿Qué dimensiones minimizan el perímetro?

(Sugerencia: usar función de perímetro y derivar)

---

### **C. Límite difícil**

$$
\lim_{x \to 0} \frac{\ln(1 + \sin x)}{x}
$$

(Usar L’Hôpital o expansión)

---

## **9. Recomendaciones de estudio**

* **Visualizá** la función y su tangente en gráficos.
* **Comprobá tus resultados** derivando con software (GeoGebra, Desmos).
* **Resolvé primero a mano**, luego verificá con calculadora o app.
* **Practicá cada tipo de ejercicio por separado.**

</div>


<!-- HTML style definitions -->
<style>
/* Colors */
.grey1 {color: #b3b3b3;} /* my light-grey */
.grey2 {color: #999999;} /* my middle-grey */
.grey3 {color: #808080;} /* my dark-grey */
.blue1 {color: #6495ed;} /* nvim blue */
.blue2 {color: #276cdf;} /* Andrew Ng Blue */
.sky1 {color: #7dbed8;} /* nvim sky */
.sky2 {color: #27a2db;}   /* my sky */
.green {color: #81b524;} /* my green */
.red1 {color: #ec5469;} /* my coral-red */
.red2 {color: #f44336;} /* my red */
.rose {color: #ec9998:} /* nvim rose */
.gold {color: #df9d43;} /* Andrew Ng gold */
.orange1 {color: #fda556;} /* nvim orange */
.orange2 {color: #ff9505;} /*Andrew Ng orange */
.purple1 {color: #ff40ff;} /* Andrew Ng purple */
.purple2 {color: #d164d7;} /* Andrew Ng purple */
/* Font Size */
.size90 {font-size: 0.9em;}
.size85 {font-size: 0.85em;}
.size80 {font-size: 0.8em;}
.size70 {font-size: 0.7em;}
/* Document General Font Size */
body {font-size: 1.3em;}
</style>
<!-- Use <span> inline and <div> with several lines --->
