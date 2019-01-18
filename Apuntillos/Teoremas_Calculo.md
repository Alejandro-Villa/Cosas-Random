---
geometry: margin=2cm
title: "**Teoremas y resultados de Cálculo I**"
author: "Alejandro Villanueva Prados"
---

# Funciones 

## Teorema de los ceros de Bolzano.
_Toda función continua en un intervalo que toma valores positivos y negativos
se anula en algún punto del intervalo_

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

**Consecuencias**

1. Existencia de raíces: _Dados $a>0$ y $k\in\mathbb{N}$ hay un único número $c>0$ tal que $c^k=a$, en otras palabras, $\log_c a = k$ es único._

	* Demostración: La función $f:\mathbb{R}^{+}_0 \to \mathbb{R}$ tal que $f(x) = x^k - a$ es continua y con distinto signo entre $0$ y $1+a$, con lo cual $\exists c > 0: f(c)=0$. Este número es único porque $f$ es estrictamente creciente. (sea $\varepsilon > 0$, $f(x) < f(x+\varepsilon)$).

2. Ceros de polinomio de grado impar: _Toda función polinómica de grado impar se anula en algún punto_
