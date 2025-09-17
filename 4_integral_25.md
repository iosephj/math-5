---
title: "Cálculo Integral"
autor: "José Juarez"
version: "02/09/25"
---

<span hidden>Local path of the file: "H:/im/mat5/"</span>
<span hidden>Local path of images: "H:/im/mat5/_i/"</span>

<br>
<span hidden>Image</span>
   <center>![](https://img.freepik.com/vector-gratis/gente-colaborando-hacer-puzzle_23-2148077315.jpg?semt=ais_hybrid&w=740&q=80){width=400px}</center>
<br>


<span hidden>--- Guide Start ---</span>

## 1. Introducción al Cálculo Integral: El Arte de Medir Áreas

<br>
<span hidden>Image</span>
   <center>![](https://openstax.org/apps/image-cdn/v1/f=webp/apps/archive/20250522.165258/resources/53c0a0372b67f40fea8088b72c7834cb549342c4){width=300px}</center>
   <center>
      <span class="grey3 size70">. </span>
      <span class="grey3 size50">Fuente: </span>
   </center>
<br>

Imagina que quieres conocer el **área de un terreno con forma irregular**. No basta con medir largo y ancho por que el contorno no es recto. Aquí entra el **cálculo integral**. Su idea central es **dividir una región bajo una curva en infinitos pedacitos diminutos**, calcular el área de cada uno y sumarlos todos. Así, incluso las formas más complicadas pueden medirse con precisión.

El cálculo integral no solo sirve para medir áreas: es una herramienta fundamental en física, economía, biología y muchas otras ciencias, donde las cantidades **cambian de manera continua**. <span hidden>A lo largo de esta guía, exploraremos cómo usar la integral para resolver problemas prácticos y entender mejor el mundo que nos rodea.</span>


<br><br>


## 2. La integral definida como el límite de una suma de Riemann

<br>
<span hidden>Image</span>
   <center>![](integr_def_riemann.png){width=400px}</center>
   <center>
      <span class="grey3 size70">Integral definida. </span>
      <span class="grey3 size50">Fuente: Khan Academy</span>
   </center>
<br>

<br><span class="grey3 size70">🔁 Repaso:</span>

Para calcular el **área bajo una curva** $f(x)$ entre $x=a$ y $x=b$, podemos aproximarla sumando áreas de **rectángulos** sobre subintervalos:

$$
S_n = \sum_{i=1}^n f(x_i^*) \, \Delta x, \quad \Delta x = \frac{b-a}{n}
$$

Al aumentar el número de rectángulos ($n \to \infty$), la suma se acerca al valor exacto del área:

$$
\int_a^b f(x)\, dx = \lim_{n \to \infty} \sum_{i=1}^n f(x_i^*) \, \Delta x
$$

**Idea clave:** La integral definida es el **límite de estas sumas**, conectando la geometría (área) con el cálculo.

Puedes repasarlo [aquí](https://www.youtube.com/watch?v=lKV1IS2-OAk&t=59s)

<br><span class="grey3 size70">📝 Práctica:</span>

Resuelve estas sumas de Riemann. Aunque aun no sabes como calcularla se agrega el valor de la integral para que veas hasta donde te aproximaste.

**1.** Sea $f(x) = x$ en el intervalo $[0, 2]$. Calcula una suma de Riemann siguiendo los siguientes pasos:

- Divide el intervalo en 4 rectángulos ($\Delta x = 0.5$).
- Toma la altura de cada rectángulo en el extremo derecho: $f(0.5)=0.5, f(1)=1$...
- Calcula la suma de áreas como: $S_4 = 0.5 \cdot (0.5 + 1 + ...) = ...$
- Si aumentas los rectángulos, la suma se acerca al valor exacto de la integral: $\int_0^2 x \, dx = 2$

**2.** Sea la función cuadrática $f(x) = x^2$. Calcula el área bajo la curva entre $x=0$ y $x=2$.

- Divide el intervalo $[0,2]$ en 4 partes iguales: $\Delta x = 0.5$.
- El resultado al que deberías llegar es 3,75 mientras que el resultado exacto con integral es $\tfrac{8}{3} \approx 2.67$.


<br><br>


## 3. Teorema fundamental del cálculo

<br><span class="grey3 size70">🔁 Repaso:</span>

El **teorema fundamental del cálculo** conecta dos mundos:

* El de la acumulación (integrales definidas).
* El del cambio instantáneo (derivadas).

Si $F(t)$ es una primitiva (antiderivada) de $f(t)$, entonces:

$$
\int_a^b f(t)\,dt = F(b) - F(a)
$$

Esto nos permite calcular el área o la acumulación **sin necesidad de aproximar con infinitos rectángulos**: basta con encontrar una función cuya derivada sea $f(t)$.


<br><span class="grey3 size70">📝 Práctica:</span>

Resuelve estos ejercicios pero no pierdas de vista que estás calculando el área bajo la curva que representa la función.

**1.** Encuentra la solución exacta para la integral de los ejercicios **1** y **2** de la sección anterior.

**2.** Resuelve las siguientes integrales ingeniándotelas para encontrar la primitiva (o antiderivada):

- **a)** $\int_0^4 5 \, dx$

- **b)** $\int_1^3 (2x+1) \, dx$

- **c)** $\int_0^2 x^2 \, dx$

- **d)** $\int_{-1}^2 (x^3 + 2x) \, dx$


<br><br>


## 4. Problemas contextualizados

<br><span class="grey3 size70">📝 Práctica:</span>

Resuelve estos problemas en donde la **integral definida** representa una magnitud física. Aquí verás cómo el área bajo la curva se conecta con la realidad:

**1.** **Distancia recorrida en bicicleta (velocidad-tiempo):**

Un ciclista parte del reposo y su velocidad (en m/s) está dada por la función:

$$
v(t) = 2t, \quad 0 \leq t \leq 5 \quad \text{(tiempo en segundos).}
$$

¿Cuál es la **distancia recorrida** en esos 5 segundos?

*(Pista: la distancia es el área bajo la curva velocidad-tiempo).*


**2.** **Volumen de agua (caudal-tiempo)**

El caudal de agua que entra en un tanque varía según:

$$
Q(t) = 10 + 5t \quad \text{(litros/min)}, \quad 0 \leq t \leq 6 \quad \text{(min)}.
$$

¿Cuántos **litros de agua** ingresaron en total durante los 6 minutos?

*(Pista: volumen = área bajo la curva caudal-tiempo).*


<br><br>


## 5. Propiedades de la integral definida

<br><span class="grey3 size70">🔁 Repaso:</span>

Sea $f(x)$ y $g(x)$ funciones integrables en $[a,b]$ y $c$ un número real:

1. **Linealidad**

$$
\int_a^b [cf(x) + g(x)] \, dx = c \int_a^b f(x)\, dx + \int_a^b g(x)\, dx
$$

2. **Cambio de límites**

$$
\int_a^b f(x)\, dx = -\int_b^a f(x)\, dx
$$

3. **Intervalo nulo**

$$
\int_a^a f(x)\, dx = 0
$$

4. **Aditividad de intervalos**

$$
\int_a^c f(x)\, dx + \int_c^b f(x)\, dx = \int_a^b f(x)\, dx
$$

5. **Positividad** (si $f(x) \geq 0$ en $[a,b]$)

$$
\int_a^b f(x)\, dx \geq 0
$$

6. **Orden** (si $f(x) \leq g(x)$ en $[a,b]$)

$$
\int_a^b f(x)\, dx \leq \int_a^b g(x)\, dx
$$

Estas propiedades permiten simplificar cálculos y entender el **significado geométrico** de la integral como área.


<br><span class="grey3 size70">📝 Práctica:</span>

Resuelve aplicando propiedades:

**1.** $\int_2^2 (x^2+1)\,dx + \int_0^1 x\,dx$

**2.** Usa la **linealidad** para separar: $\int_0^1 (3x^2 + 4x)\,dx$

**3.** Verificar la siguiente igualdad resolviendo ambos miembros y comprobando la igualdad: $\int_0^4 x\,dx = \int_0^2 x\,dx + \int_2^4 x\,dx$

**4.** Verificar la propiedad de orden para $f(x) = x$ y $g(x) = x+1$ en el intervalo $[0,2]$, demostrando que: $\int_0^2 f(x)\,dx \; < \; \int_0^2 g(x)\,dx$


<br><br>


## 6. Integral indefinida

<br><span class="grey3 size70">🔁 Repaso:</span>

La **integral indefinida** de una función es el conjunto de sus **antiderivadas** o **primitivas**:

$$
\int f(x)\,dx = F(x) + C \quad \text{con } F'(x)=f(x).
$$

**Ejemplo:**

$$
\int x^2 \, dx = \tfrac{x^3}{3} + C
$$

**Diferencia con la definida:**

* **Definida**: da un **número** (área entre $a$ y $b$).
* **Indefinida**: da una **función** (todas las primitivas).

También puedes repasar esto [aquí.](https://www.youtube.com/watch?v=Is6dH965Q6w&t=224s)

<br><span class="grey3 size70">📝 Práctica:</span>

**a)** Encontrar estas integrales indefinidas:

**1.** $\int 3,75x \, dx$
**2.** $\int 3\cos(x)\, dx$
**3.** $\int \frac{6}{x}\, dx$

**b)** Resuelve ahora estos [ejercicios](https://es.khanacademy.org/math/ap-calculus-ab/ab-integration-new/ab-6-7/e/antiderivatives).


<br><br>


## 7. Reglas básicas para encontrar integrales indefinidas

### 7a) Regla de la potencia inversa y propiedades

<br><span class="grey3 size70">🔁 Repaso:</span>

$$
\int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad \text{(si \(n \neq -1\))}.
$$

Puedes repasar [aquí](https://www.youtube.com/watch?v=JdsgI7lXoNk&t=349s).


<br><span class="grey3 size70">📝 Práctica:</span>

**1.** Haz al menos dos ejercicios de [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-integration-new/ab-6-8a/e/intro-to-integration).

**2.** Haz al menos dos ejercicios con potencia negativa de [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-integration-new/ab-6-8a/e/basic-integration). 

<br>

### 7b) Propiedades básicas (linealidad)

<br><span class="grey3 size70">🔁 Repaso:</span>

$$
\int \big(f(x) + g(x)\big)\,dx = \int f(x)\,dx + \int g(x)\,dx
$$

$$
\int k \cdot f(x)\,dx = k \cdot \int f(x)\,dx \quad (k \in \mathbb{R})
$$

<br><span class="grey3 size70">📝 Práctica:</span>

Haz al menos dos ejercicios de [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-integration-new/ab-6-8a/e/integration).

<br>

### 7c) Simplificar algebraicamente antes de integrar

<br><span class="grey3 size70">🔁 Repaso:</span>

Puedes repasarlo [aquí]().

<br>
<span hidden>Image</span>
   <center>![](integr_indef_simplificar_antes.png){width=400px}</center>
   <center>
      <span class="grey3 size70"></span>
      <span class="grey3 size50">Fuente: Khan Academy</span>
   </center>
<br>

<br><span class="grey3 size70">📝 Práctica:</span>

Haz **"todos"** los ejercicios de [aquí](https://es.khanacademy.org/math/ap-calculus-ab/ab-integration-new/ab-6-8a/e/reverse-power-rule-rewriting).


<div hidden>


---

---

## 5. Cambio de variables

<br><span class="grey3 size70">🔁 Repaso:</span>

Es una técnica de integración muy poderosa. Consiste en reemplazar la variable original por otra más simple. Formalmente, si $u=g(x)$, entonces:

$$
\int f(g(x))g'(x)\, dx = \int f(u)\, du
$$

**Ejemplo:**

$$
\int 2x\cos(x^2)\, dx
$$

Hacemos el cambio $u = x^2 \Rightarrow du = 2x\, dx$.

$$
\int 2x\cos(x^2)\, dx = \int \cos(u)\, du = \sin(u) + C = \sin(x^2) + C
$$


<br><span class="grey3 size70">📝 Práctica:</span>


1. $\int x e^{x^2}\, dx$
2. $\int \frac{1}{x \ln x}\, dx$


## 6. Integrales racionales

<br><span class="grey3 size70">🔁 Repaso:</span>

Una **función racional** es el cociente de dos polinomios, por ejemplo:

$$
\frac{3x^2+1}{x^3+2x}
$$

Resolver integrales de este tipo no siempre es directo. Una técnica central es la **descomposición en fracciones parciales**, que permite transformar una fracción complicada en la suma de fracciones más simples, cada una integrable.

**Ejemplo:**

$$
\int \frac{1}{x^2-1}\, dx
$$

Se factoriza el denominador:

$$
x^2-1 = (x-1)(x+1)
$$

Entonces:

$$
\frac{1}{x^2-1} = \frac{A}{x-1} + \frac{B}{x+1}
$$

Resolviendo el sistema, $A = \tfrac{1}{2}$, $B = -\tfrac{1}{2}$.

$$
\int \frac{1}{x^2-1}\, dx = \frac{1}{2}\int \frac{1}{x-1}\, dx - \frac{1}{2}\int \frac{1}{x+1}\, dx
$$

$$
= \tfrac{1}{2}\ln|x-1| - \tfrac{1}{2}\ln|x+1| + C
$$

<br><span class="grey3 size70">📝 Práctica:</span>

1. $\int \frac{2x+3}{x^2+x}\, dx$
2. $\int \frac{1}{x^2+4x+3}\, dx$



### 5. Integrales trigonométricas

Aquí aparecen funciones como $\sin^n x$, $\cos^m x$ o productos de senos y cosenos.

Las principales herramientas son:

* Usar **identidades trigonométricas** para simplificar.
* Reducir potencias con fórmulas como:

  $$
  \sin^2 x = \frac{1-\cos(2x)}{2}, \quad \cos^2 x = \frac{1+\cos(2x)}{2}
  $$

**Ejemplo:**

$$
\int \sin^2 x\, dx
$$

$$
= \int \frac{1-\cos(2x)}{2}\, dx = \frac{x}{2} - \frac{\sin(2x)}{4} + C
$$

**Para practicar:**

1. $\int \sin^3 x \cos x \, dx$
2. $\int \cos^2 x \, dx$

### 7. Integrales impropias

Son integrales definidas donde el intervalo es infinito o la función presenta discontinuidades.

Dos casos típicos:

1. **Intervalo infinito**

$$
\int_1^{\infty} \frac{1}{x^2}\, dx
$$

Se interpreta como un límite:

$$
\lim_{b\to\infty} \int_1^b \frac{1}{x^2}\, dx = \lim_{b\to\infty} \left[-\frac{1}{x}\right]_1^b
$$

$$
= \lim_{b\to\infty}\left(-\frac{1}{b}+1\right) = 1
$$

2. **Función con discontinuidad**

$$
\int_0^1 \frac{1}{\sqrt{x}}\, dx
$$

En $x=0$ la función se “dispara”. Tomamos límite:

$$
\lim_{\epsilon\to 0^+} \int_\epsilon^1 \frac{1}{\sqrt{x}}\, dx = \lim_{\epsilon\to 0^+} \left[2\sqrt{x}\right]_\epsilon^1
$$

$$
= 2 - 0 = 2
$$

**Para practicar:**

1. $\int_1^{\infty} \frac{1}{x}\, dx$ (¿converge o diverge?)
2. $\int_{-1}^1 \frac{1}{x^2}\, dx$

---

---

</div>





<span hidden>--- Guide End ---</span>


<span hidden>--- Guide Auxiliary Templates ---</span>

<div hidden>

<span hidden>Learning objectives very briefly</span>
   <span class="grey3 size85">.</span>

<br>
<span hidden>Image</span>
   <center>![](){width=400px}</center>
   <center>
      <span class="grey3 size70">. </span>
      <span class="grey3 size50">Fuente: </span>
   </center>
<br>

... [fragmento de video](https://www.youtubetrimmer.com/view/?v=82mTNbPFTnw&start=46&end=103&loop=0)...

<span hidden>Visible story or anecdote</span>
   <span class="grey3 size85">...</span>

<br><span class="grey3 size70">🔁 Repaso:</span>

<br><span class="grey3 size70">📝 Práctica:</span>

**1.**  **:**

**2.** **:** 

</div>


<span hidden>--- Guide  Styles ---</span>

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
.size60 {font-size: 0.6em;}
.size50 {font-size: 0.5em;}
/* Document General Font Size */
body {font-size: 1.3em;}
</style>
<!-- Use <span> inline and <div> with several lines --->
