---
geometry: margin=2cm
title: "**Teoremas y resultados de Cálculo I**"
author: "Alejandro Villanueva Prados"
---

# Funciones 

## Índice.
* [Sobre Funciones](#sobre-funciones)
	* [Teorema de los ceros de Bolzano.](#teorema-de-los-ceros-de-bolzano)
	* [Teorema del valor intermedio.](#teorema-del-valor-intermedio-consecuencia-de-bolzano)	
* [Sobre Sucesiones](#sobre-sucesiones)

\pagebreak

# Sobre funciones

## Teorema de los ceros de Bolzano

_Toda función continua en un intervalo que toma valores positivos y negativos se anula en algún punto del intervalo_

**Demostración**

1. Objetivo: probar que si $f: [a,b] \to \mathbb{R}$ es continua y $f(a) < 0 < f(b)$, entonces $f$
se anula en algún punto del intervalo $]a,b[$. Buscamos $c\in]a,b[$ tal que $f(c)=0$.

2. A la izquierda de $c$ la función es negativa, y a la derecha positiva. Se define: 
$$
E=\{x\in[a.b]: f(t) < 0, \forall t\in[a,x]\}
$$
	- Nota: $E\subset[a,b]$ y $a\in E$

3. Usando el principio del supremo, llamamos $c = sup(E)$, y $a \le c \le b$. Vamos a probar que la desigualdad es estricta.

4. Para ello, usamos la propiedad local de conservación del signo (porque $f$ es continua): se tiene que para $\delta > 0$, $f(a + \delta) < 0$ y $f(b - \delta) > 0$. Ahora suponemos que $a=c$, si eso fuese cierto, $a + \delta > c$ y $a + \delta \in E$, lo cual es imposible porque $c=sup(E)$ y por tanto se prueba que $a < c$. Análogamente $c < b$, por lo tanto nos queda: $a < c < b$

5. Ahora vamos a probar que $f(t) < 0, \forall t \in [a, c[$, equivalente a $[a,c[ \subset E$. Esto se hace usando que $c$ es supremo de E, tomamos un $x: a < x_0 < c$ dado que $c$ es supremo de $E$, entonces existe un $z_0\in E$ tal que $x_0 < z_0 \le c$. Así que cualquier elemento de $[a, x_0]$ pertenence también a $[a,z_0]$, y como $z_0\in E$, probamos que $f(t) < 0, \forall t \in [a,c[$.
	- Aclaración: como los números que escogemos ($x_0$ y $z_0$) son arbitrarios, eso significa que el intervalo $[a,c[ \subset E$.

6. Paso final: $f(c)=0$. A la izquierda de $c$, la función toma valores negativos, así que por la continuidad de $f$ y la conservación local del signo, no puede ser $f(c) > 0$, con lo cual $f(c) \le 0$, pero como a la derecha es positiva, no puede ser $f(c) < 0$, así que $f(c) \ge 0$ y **también** $f(c) \le 0$. Por tanto, $f(c) = 0$, con $c\in]a,b[$

$\square$

**Consecuencias**

1. Existencia de raíces: _Dados $a>0$ y $k\in\mathbb{N}$ hay un único número $c>0$ tal que $c^k=a$, en otras palabras, $\log_c a = k$ es único._

	* Demostración: La función $f:\mathbb{R}^{+}_0 \to \mathbb{R}$ tal que $f(x) = x^k - a$ es continua y con distinto signo entre $0$ y $1+a$, con lo cual $\exists c > 0: f(c)=0$. Este número es único porque $f$ es estrictamente creciente. (sea $\varepsilon > 0$, $f(x) < f(x+\varepsilon)$).

2. Ceros de polinomio de grado impar: _Toda función polinómica de grado impar se anula en algún punto_

**Demostración**: _WIP_

\pagebreak

## Teorema del valor intermedio consecuencia de Bolzano

_La imagen de un intervalo por una función continua es un intervalo._

**Demostración**

1. Objetivo: Probar que dado $I \ne \emptyset, I \subset \mathbb{R}$, entonces $f(I) = J$ siendo $J$ un intervalo.

2. Sea un intervalo $I$ y $f: I \to \mathbb{R}$ continua. Probar el teorema equivale a probar que dados dos puntos cualesquiera de $J = f(I)$, todos los puntos entre ellos también pertenecen a $J$ (Definición de intervalo). Sean pues, $u, v: u < v$ elementos de $J$.

3. Al ser $u$ y $v$ imágenes de puntos de $I$, deben existir $\alpha \in I: f(\alpha)=u$ y $\beta \in I : f(\beta)=v$, no puede ser $\alpha = \beta$ por ser $f$ función. Suponngamos que $\alpha <\beta$

4. Tomamos un $z$ tal que $u < z < v$ y definimos $h: I \to \mathbb{R}$, $h(x) = z - f(x)$ para todo $x \in I$. $h$ es continua (composición de funciones continuas) en $I$.

5. Ahora realizamos $h(\alpha)=z-f(\alpha)=z-u > 0$ (recordemos $z > u$). Del mismo modo $h(\beta) < 0$. Así que por el Teorema de los ceros de Bolzano, existe $\lambda$ tal que $\alpha < \lambda < \beta$ y $h(\lambda) = z - f(\lambda) = 0 \implies f(\lambda) = 0$

6. Dado que $\lambda \in ]\alpha,beta[ \subset I$, debe ocurrir que $f(\lambda) = z \in J$ como esto ocurre para cualquier $u < z < v$, deducimos que $]u,v[ \subset J$ y que $J$ es un intervalo.

$\square$

Además, se da el recíproco: si suponemos que la imagen de un intervalo por una función continua es un intervalo, y la función toma valores positivos y negativos, entonces la función debe anularse en algún punto del intervalo.

# Sobre sucesiones

## Teorema de Complitud de $\mathbb{R}$. Límites superior e inferior.

* **Definición**: Condición de Cauchy.
	Se dice que una sucesión $\{x_n\}$ satisface la condición de Cauchy, si para cada númmero positivo $\varepsilon>0$, existe un número natural $m_\varepsilon$, tal que para todos $p,q\in \mathbb{N}$ con $p\ge m_\varepsilon$ y $q\ge m_\varepsilon$ se verifica que  $|x_p - x_q| < \varepsilon$

**Teorema de Complitud de $\mathbb{R}$**

*Una sucesión de números reales converge si, y sólo si, verifica la condición de Cauchy.*

**Demostración**

1. Partimos de $\{x_n\}$ cumple la condición de Cauchy. Vamos a probar que está acotada.

2. La condición de Cauchy implica que existe $m_0 \in \mathbb{N}$ tal que $|x_p-x_{m_0}|<1$ para todo $p\ge m_0$. Manipulando la desigualdad se obtiene $|x_p|\le|x_p-x_{m_0}|+|x_{m_0}| \implies |x_p|<1+|x_{m_0}|$

3. Definimos $M=máx\{|x_1|,|x_2|,\dots,|x_{m_0}|,1+|x_{m_0}|\}$. Así que obtenemos que $x_n\le M$ para todo $n\in\mathbb{N}$, por lo tanto, concluimos que $\{x_n\}$ está acotada.

4. Ahora, aplicamos el teorema de Bolzano-Weierstrass, que nos garantiza que existe una sucesión parcial que converge a $x\in\mathbb{R}$, a la que notamos como $\{x_{\sigma(n)}\}\to x \in \mathbb{R}$.Hemos de probar que $\{x_n\}$ también converge a $x$.

5. Sea $\varepsilon > 0$, existe un cierto $n_0\in\mathbb{N}$ tal que $|x_p-x_q|<\frac{\varepsilon}{2}$ siempre que $p,q\ge n_0$ (Esto se obtiene aplicando la hipótesis de que $\{x_n\}$ es de Cauchy).También se tiene que existe $n_1\in\mathbb{N}$ tal que $|x_{\sigma(n)}-x|<\frac{\varepsilon}{2}$ (Porque la sucesión parcial es convergente a $x$). Si tomamos $m=máx\{n_0,n_1\}$, entonces para todo $n\ge m$ se tiene que $\sigma(n)\ge n \ge m$ por lo cual se verifican ambas igualdades. Las sumamos:

$$
|x_n - x|\le|x_n - x_{\sigma(n)}| + |x_{\sigma(n)} - x| < \frac{\varepsilon}{2}+\frac{\varepsilon}{2} = \varepsilon
$$
