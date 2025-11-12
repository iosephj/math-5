---
title: "Cálculo numérico y aplicaciones de las integrales"
autor: "José Juarez"
version: "10/11/25"
---

<span hidden>Local path of the file: "H:/im/mat5/"</span>
<span hidden>Local path of images: "H:/im/mat5/_i/"</span>

<!-- Image -->
<br>
   <center>![](https://imgs.search.brave.com/HRZI_u0C1ybj6_1x8ntKc7QE9HArmFFb2AhREeG3zBQ/rs:fit:860:0:0:0/g:ce/aHR0cDovL2Zhcm04/LnN0YXRpY2ZsaWNr/ci5jb20vNzAzOC82/OTg3NzQ2Mzk1X2Uw/NzNkOGRiODJfby5w/bmc){width=400px}</center>
   <center>
      <span class="grey3 size70"></span>
      <span class="grey3 size50"></span>
   </center>
<br>



<!-- *** GUIDE START *** -->


## 1. Introducción

En ingeniería y electrónica, muchas veces necesitamos calcular **áreas, energías, cargas o volúmenes** que no se pueden obtener con fórmulas exactas.
En esos casos usamos la **integración numérica**, que aproxima la integral sumando áreas pequeñas.

Cuando una magnitud depende de **dos o tres variables** (por ejemplo, densidad en una superficie o volumen), usamos **integrales dobles o triples**.


<br><br>


## 2. Integración numérica

### A) Concepto

El valor de una integral definida $\int_a^b f(x),dx$ representa el **área bajo la curva** de (f(x)) entre (a) y (b).

Cuando no podemos obtenerla analíticamente, la aproximamos mediante **métodos numéricos**.

<br>

### B) Regla de los trapecios

La explicación de clase está basada en esta [fuente](https://es.khanacademy.org/math/ap-calculus-ab/ab-integration-new/ab-6-2/a/understanding-the-trapezoid-rule) que consultar como repaso. También puedes repasar estos conceptos en este [video](https://www.youtubetrimmer.com/view/?v=S8Htl7olCjA&start=387&end=526&loop=0)

La idea es aproximar la curva por tramos rectos formando pequeños trapecios y así podemos obtener aproximaciones más precisas que al utilizar rectángulos (es decir, "sumas de Riemann")

En resumen:

$\int_a^b f(x),dx \approx \frac{h}{2},[f(x_0) + 2f(x_1) + 2f(x_2) + \dots + 2f(x_{n-1}) + f(x_n)]$

donde $(h = \dfrac{b - a}{n})$ es el ancho de cada subintervalo.

<br>
 
### C) Ejercicios aplicando regla de los trapecios

**1.** Resolver el problema de práctica y el problema desafío que aparecen en nuestra [fuente principal](https://es.khanacademy.org/math/ap-calculus-ab/ab-integration-new/ab-6-2/a/understanding-the-trapezoid-rule)

**2.** Resuelve [estos ejercicios](https://es.khanacademy.org/math/ap-calculus-ab/ab-integration-new/ab-6-2/e/trapezoid-rule) aplicando regla de los trapecios


<div hidden>


### 2.3 Regla de Simpson

Aproxima la curva por arcos de parábola (más precisa).
Requiere que el número de subintervalos (n) sea **par**.

[
\int_a^b f(x),dx \approx \frac{h}{3},[f(x_0) + 4f(x_1) + 2f(x_2) + 4f(x_3) + \dots + f(x_n)]
]

---

## 3. Integración numérica con Python

Python permite aplicar estos métodos fácilmente y visualizar resultados.

### 🔧 Preparación

Podés usar **Google Colab** ([https://colab.research.google.com](https://colab.research.google.com)) o instalar **Python + SciPy**.

---

### 3.1 Ejemplo: carga eléctrica en un condensador

Supongamos que la **corriente de carga** de un condensador varía con el tiempo como:

[
I(t) = 2t \quad [A]
]

Queremos calcular la **carga total** acumulada entre (t=0) y (t=4) segundos:

[
Q = \int_0^4 I(t),dt
]

---

### 3.2 Código en Python (sin lambda)

```python
import numpy as np
from scipy import integrate
import matplotlib.pyplot as plt

# Función corriente en función del tiempo
def I(t):
    return 2 * t   # amperios

a, b = 0, 4        # intervalo de integración (segundos)
n = 4               # cantidad de subintervalos (puede variarse)

# Generamos los puntos
t = np.linspace(a, b, n + 1)
i = I(t)

# Reglas de integración
Q_trap = np.trapz(i, t)
Q_simp = integrate.simpson(i, t)

print("Carga por regla de los trapecios:", Q_trap, "C")
print("Carga por regla de Simpson:", Q_simp, "C")

# Visualización
plt.plot(t, i, 'o-', label='I(t) = 2t')
plt.fill_between(t, i, color='lightblue', alpha=0.5)
plt.title("Corriente durante la carga de un condensador")
plt.xlabel("Tiempo (s)")
plt.ylabel("Corriente (A)")
plt.grid(True)
plt.legend()
plt.show()
```

🔹 Probá cambiar `n = 4` por `n = 20` y observá cómo el resultado se aproxima más al valor exacto (Q = 16,C).

---

### 3.3 Interpretación

* Cuantos más intervalos uses (`n` grande), más pequeña será (h) y más precisa la aproximación.
* En electrónica, esto sirve para estimar **energía**, **carga** o **potencia media** a partir de **datos experimentales discretos** (por ejemplo, mediciones con sensores o ADC).

---

## 4. Integrales múltiples

### 4.1 Integral doble

Se usa para calcular **volúmenes** o **magnitudes distribuidas** sobre una **superficie**.

[
\iint_R f(x,y),dx,dy
]

Representa el volumen bajo la superficie (z = f(x,y)) en una región (R).

**Ejemplo:**
[
I = \int_0^1 \int_0^2 (x + y),dy,dx
]

1. Integramos respecto de (y):
   (\int_0^2 (x + y),dy = 2x + 2)
2. Luego respecto de (x):
   (\int_0^1 (2x + 2),dx = [x^2 + 2x]_0^1 = 3)

📘 **Resultado:** (I = 3)

---

### 4.2 Integral triple

Se usa cuando una magnitud depende de tres variables (x, y, z), por ejemplo densidad en un volumen.

[
\iiint_V f(x,y,z),dx,dy,dz
]

Si (f(x,y,z) = 1), el resultado es el **volumen** del cuerpo.
Ejemplo: sobre un cubo de lado (a):
[
\iiint 1,dx,dy,dz = a^3
]

---

### 4.3 Propiedades principales

1. **Linealidad:**
   (\int (a f + b g) = a \int f + b \int g)
2. **Aditividad:**
   Si (R = R_1 \cup R_2), entonces
   (\int_R f = \int_{R_1} f + \int_{R_2} f)
3. **Cambio de orden:**
   En regiones simples, se puede cambiar el orden de integración ((dx,dy \leftrightarrow dy,dx)).

---

## 5. Aplicaciones y modelización

### 🔹 En electrónica

* **Energía consumida:** (E = \int P(t),dt)
* **Carga eléctrica:** (Q = \int I(t),dt)
* **Potencia media:** (P_m = \frac{1}{T}\int_0^T P(t),dt)
* **Densidad superficial de carga:**
  (\sigma(x,y)) integrada en una superficie:
  (Q = \iint_S \sigma(x,y),dA)

---

### 🔹 En física y tecnología

* **Integral doble:** volumen bajo una superficie de temperatura o potencial.
* **Integral triple:** masa total de un objeto con densidad variable.
* **Modelización real:**

  * Cálculo del volumen de líquido en un tanque con forma irregular.
  * Carga total distribuida en un capacitor no uniforme.
  * Estimación de energía acumulada en una batería a partir de mediciones de corriente.

---

## 6. Actividades sugeridas

1. **Python:** reproducir el ejemplo de integración de (I(t)=2t) y probar con otras funciones, como (I(t)=5\sin(t)).
2. **Comparación:** variar el número de intervalos `n` y analizar la precisión.
3. **Manual:** calcular un área con la regla de los trapecios en Excel o en papel.
4. **Integrales dobles:** resolver problemas de volumen o masa con densidad variable.
5. **Modelización:** plantear un problema técnico real (por ejemplo, energía total en un ciclo de corriente alterna) y describir cómo lo resolverías por integración numérica.

</div>




<!-- *** GUIDE END *** -->


<!-- *** GUIDE AUXILIARY TEMPLATES *** -->


<div hidden>


<!-- Learning objectives very briefly -->
<span class="grey3 size85">.</span>

<!-- Image -->
<br>
   <center>{width=400px}</center>
   <center>
      <span class="grey3 size70">. </span>
      <span class="grey3 size50">Fuente: </span>
   </center>
<br>

<!-- Videos: change XXX to the video-id and put time (seconds) -->
<!-- Yotube with start point -->
👉 [Mira este momento clave en el video](https://www.youtube.com/watch?v=XXX&t=123s)
🎬 [Un fragmento que vale la pena ver](https://www.youtube.com/watch?v=XXX&t=123s)
🔎 [Este detalle del video te va a interesar](https://www.youtube.com/watch?v=XXX&t=123s)
⚡ [Dale play a esta parte y fijate qué pasa](https://www.youtube.com/watch?v=XXX&t=123s)
<!-- Youtubetrimmer with start and end point -->
👉 [Mirá este momento puntual del video](https://youtubetrimmer.com/view/?v=XXX&start=120&end=150&loop=0)
🎬 [Este fragmento explica justo lo que necesitamos](https://youtubetrimmer.com/view/?v=XXX&start=120&end=150&loop=0)
⚡ [Dale play a esta parte y sacá tus conclusiones](https://youtubetrimmer.com/view/?v=XXX&start=120&end=150&loop=0)
🔎 [Fijate qué pasa en este momento](https://youtubetrimmer.com/view/?v=XXX&start=120&end=150&loop=0)

<!-- Visible story or anecdote -->
<span class="grey3 size85">...</span>

<!-- Sections -->
<br><span class="grey3 size70">🔁 Repaso:</span>
<br><span class="grey3 size70">🛠️ Trabajo:</span>
<br><span class="grey3 size70">📘 Teoría:</span>
<br><span class="grey3 size70">✅ Autoevaluación:</span>
<br><span class="grey3 size70">📝 Práctica:</span>
**1.**  **:**
**2.** **:** 

<!-- Solutions -->
<div class="grey3 size70">.</div>


</div>


<!-- Guide style definitions -->
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
