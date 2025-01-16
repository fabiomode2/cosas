#### Principio inclusión-exclusión
$$ |A \cup B| = |A| + |B| - |A \cap B|$$
# Combinatoria

|                | Importa el orden                | No importa el orden               | n = r                                             |
| -------------- | ------------------------------- | --------------------------------- | ------------------------------------------------- |
| Sin repetición | $V(n, r) = \frac{n!}{(n - r)!}$ | $C(n, r) = \binom{n}{r}$          | $P(n) = n!$                                       |
| Con repetición | $VR(n, r) = n^r$                | $CR(n, r) = \binom{n - 1 + r}{r}$ | $PR(n; n1, n2, n3...) = \frac{n!}{n1!  n2!  n3!}$ |
##### Binomio de Newton

$$ (a + b)^n  = \sum_{k = 0}^n \binom{n}{k} a^k b^{n - k} $$

#### Fórmula de Pascal

$$ \binom{n}{k} = \binom{n - 1}{k - 1} + \binom{n - 1}{k} $$

#### Multinomio de Leibniz

$$ n_1 + n_2 .. + n_k = n ;(x_1 + x_2 + ... x_k)^k = \sum{\binom{n}{n_1 n_2 .. n_k} x_1^{n_1}x_2^{n_2}..x_k^{n_k}} $$

# Recursividad

RRLHCC de orden K    $a_n = c_1 a_{n - 1} + c_2 a_{n - 2} + .. + c_k a_{n - k}$
$a_n = 2a_{n - 1} + 1$       No homogénea
$a_n = n a_{n - 1}$             Sin coeficientes constantes
$a_n = 2 a_{n - 1}^2$             No lineal

#### Ecuación característica de RR de grado X

$r^{n - k} (r^k - c_1 r^{k - 1} - ... - c_{k - 1}r^1 - c_k) = 0$
Ej.: $x^5 - x + 1 = 0$

#### Solución RRLHCC  -  raíces distintas (y reales)

Sean $r_1, r_2, r_3 ... r_k$ las raíces, la solución es: $a_n = \alpha_1 r_1^n + ... + \alpha_k r_k^n$  siendo $\alpha_i$ constantes 
$\alpha_i$ se obtienen sustituyendo las condiciones iniciales. nº condiciones iniciales = nº raíces

#### Solución RRLHCC  -  raíces repetidas (y reales)

$(r - 2)^3 (r - 1)^2 (r + 3)^1 = 0$

$r_1 = 2$ multiplicidad 3 (triple)

$r_2 = 1$ multiplicidad 2 (doble)

$r_3 = -3$ multiplicidad 1 (simple)

Siendo $r_i, i=1..s$ las raíces y $m_i, i=1..s$ su multiplicidad, la solución es:

$a_n = (\alpha_{10} + \alpha_11 n + ... + \alpha_{1,m_{1-1}}n^{m_1 - 1})r_1^n + (\alpha_{20} + \alpha_{21}n + ... + \alpha_{2, m_{2 - 1}} n^{m_{2 - 1}})r_2^n + ... + (\alpha_{s0} + \alpha_{s1}n + ... + \alpha_{s, m_{s - 1}}n^{m_{s - 1}}) r_s^n$

Ej.: $a_n = 4a_{n - 1} - 4a_{n-2}$ , $a_0 = 2, a_1 = 8$ || $r^2 - 4r + 4 = 0$ || $(r-2)^2$ || $r_1 = 2, m_1 = 2$ 

$a_n = (\alpha_{1,0} + \alpha_{1,1}n)2^n$  

$a_0 = (\alpha_{10} + \alpha_{11}0)2^0$ = 2 => $\alpha_{10} = 2$

$a_1 = (2 + \alpha_{11}1)2^1 = (2 + \alpha_{11})2 = 8 => \alpha_{11} = 2$

$a_n = (2 + 2n)2^n$



#### No homogénea

$H_n = 2H_{n-1} + 1$ -> RRLCC no homogénea

$a_n = c_1 a_{n - 1} + ... + c_k a_{n - k} + L(n)$ siendo $L(n)$ la parte no-homogénea.

Si $a_n^{(p)}$ es una solución particular de RRLnHCC y $a_n^{(h)}$ cualquier solución de la parte homogénea, entonces:  $a_n = a_n^{(h)} + a_n^{(p)}$ es solución de la RRLnHCC. 


###### Soluciones particulares

$L(n) = (p_0 + p_1 n + ... + p_t n^t)s^n$ donde $s, p_i$ son constantes.

- Si $s$ no es raíz de la ecuación característica.
  	$a_n ^{(p)} = (\beta_0 + \beta_1 n + ... + \beta_t n^t)s^n$ donde $\beta_i$ son constantes que hay que calcular.

- Si $s$ es raíz de la ec. car.
  	$a_n ^{(p)} = (\beta_0 + \beta_1 n + ... + \beta_t n^t)s^n n^m$ siendo $m$ la multiplicidad de la raíz $s$.

Ej.:

$a_n = a_{n-2} + n3^n$    3 no es raíz de la ec. car.  $x^2 - 1$

$L(n) = (0 + 1n)3^n$

$a_n^{(p)} = (\beta_0 + \beta_1 n )3^n$ 

Sustituyendo $a_n^{(p)}$ en la ec.:

$(\beta_0 + \beta_1 n)3^n = (\beta_0 + \beta_1 (n-2) )3^{n-2} + n3^n$ 

$\beta_0 3^n + \beta_1 n 3^n = \beta_0 3^{n-2} + \beta_1 n3^{n-2} - 2\beta_1 3^{n-2} + n3^n$

Dividimos todo por $3^{n-2}$

$\beta_0 3^2 + \beta_1 n 3^2 = \beta_0 + \beta_1 n - 2\beta_1 + n3^2$

$9\beta_0 + 9\beta_1 n = \beta_0 + \beta_1 n - 2\beta_1 + 9n$ 

$9\beta_0 + 9\beta_1 n = (\beta_0 - 2\beta_1) + (9 + \beta_1)n$

- $9\beta_0 = \beta_0 - 2\beta_1 \rightarrow \beta_0 = -\frac{9}{32}$
- $9\beta_1 n = (9 + \beta_1 )n \rightarrow \beta_1 = \frac{9}{8}$

La solución será:

$a_n = \alpha 1^n + \beta (-1)^n + (-\frac{9}{32} + \frac{9}{8}n)3^n$

#### RRLnHCC

$a_n = a_{n-1} + n$ RRLnHCC de orden 1.

$a_n = a_n^{(h)} + a_n^{(p)}$

ec. car. :  $r-1$, $r_1 = 1 \rightarrow a_n^{(h)} = \alpha 1^n = alpha$

$n = (0 + 1n)1^n$

$a_n^{(p)} = (\beta_0 + \beta_1 n)1^n n^m$ siendo m la multiplicidad de la raíz 1, que es 1.

$a_n^{(p)} = (\beta_0 + \beta_1 n)n$

$(\beta_0 + \beta_1 n )n = (\beta_0 + \beta_1 (n-1) )(n-1) + n$

$\beta_0 n + \beta_1 n^2 = (\beta_0 + \beta_1 n - \beta_1)(n - 1) + n$

$\beta_0 n + \beta_1 n^2 = \beta_0 n + \beta_1 n^2 -\beta_1 n -\beta_0 -\beta_1 n + \beta_1 + n$

$\beta_0 n + \beta_1 n^2 = \beta_1 n^2 + n(\beta_ 0 - 2\beta_1 + 1) + (\beta_1 - \beta_0)$

- $\beta_0 = \beta_0 -2\beta_ 1 + 1 \rightarrow \beta_1 = \frac{1}{2}$
- $0 = \beta_1 - \beta_0 \rightarrow \beta_1 = \beta_0 = \frac{1}{2}$

$a_n = a_n^{(h)} + a_n^{(p)} = \alpha + \frac{(1 + n)n}{2}$

# Grafos

Un grafo es un par $G=(V, E)$. $V$ es un conjunto finito no vacío de vértices y $E$ de ejes.
- Orden de un grafo: $|V|$, tamaño: $|E|$ 
- Un par de vértices son adyacentes si los une un ejes.
- Un vértice aislado no está conectado a nada
- Un par de v. conectados por más de 1 e. tiene ejes paralelos
- Un e. que tiene como extremos el mismo v. es un lazo
- Un grafo sin e. paralelos ni lazos es un grafo simple
- El grado de un vértice $\delta(v)$ es el nº de e. incidentes. **Lazos cuentan por dos**.
- Sucesión de grados de un grafo:
	$(v_1, v_2, v_3, v_4, v_5)$
	$(0, 3, 1, 2, 4)$
- **Lema del apretón de manos**: $\sum_{i=1}^{|V|} \delta(v_i) = 2|E|$
- Un grafo completo es el que cada v. está conectado a los demás. $K_n$ siendo $n$ el nº de v. Orden de $K_n$ es $n$, tamaño es $\binom{n}{2}$
- Ciclos $C_n$. $|C_n| = n$
- Dos grafos son **isomorfos** si existen aplicaciones biyectivas que relacionen sus ejes y vértices. Son invariantes el orden, tamaño y sucesión de grados.
- Tabla de adyacencia:

| $v_1$ | $v_2, v_3$ |
| ----- | ---------- |
| $v_2$ | $v_1$      |
| $v_3$ | $v_1$      |
- **Matriz de adyacencia**. Es una matriz $nxn$ siendo $n$ el grado del grafo en la cual la entrada $a_{ij}$ es el nº de ejes que conectan $v_i$ con $v_j$. Para un grafo simple, la matriz es binaria y la diagonal son $0s$.
- **Matriz de incidencia**. Es una matriz $B \in \mathbb{M}_{n \times m}, n=|V|, m=|E|$. La entrada $b_{ij}$ es:
  $\begin{cases}
0 \text{ si $v_1$ es incidente en el eje $j$} \\
1 \text{ si $v_1$ no es incidente en el eje $j$} \\
\end{cases}$
- Un camino de longitud $\geq 1$ donde los extremos coinciden es un ciclo.
- Un camino en el que todos los e. son distintos se llama simple.
- El número de caminos de longitud $K$ entre $v_i$ y $v_j$ es la entrada $a_{ij}$ de la matriz de adya. $A^K$
- Se dice que dos v. están conectados si existe un camino que los une.
- Un grafo se dice conexo cuando todos los v. están conectados.
- Un grafo es conexo $\Leftrightarrow$ todas las entradas no diagonales de $A + A^2 \cdots A^{n-1}$ son no nulas.
- **Un circuito euleriano es un camino simple cerrado que contiene a todos los e. del grafo.**
- Un grafo se dice Euleriano si tiene un circuito euleriano.
- Un grafo se dice semi-euleriano si tiene un camino euleriano: un camino simple no cerrado que contiene todos los e. del grafo.
- **Un grafo es Euleriano si todos los v. tienen grado PAR**
- **Un grafo es semi-euleriano si todos lo v. tienen grado PAR menos exactamente 2**
- **Algoritmo de Fleury** para encontrar un camino euleriano. 
	- Cada eje se elimina una vez pasado por él.
	- Solo se selecciona un eje puente cuando es la única opción.
- Un camino se dice **Hamiltoniano** si es un camino simple que contiene a todos los v. solo una vez. Si es cerrado, se dice ciclo Hamiltoniano.
- Un grafo se dice Hamiltoniano si tiene un ciclo hamilt. y semi-hamiltoniano si tiene un camino hamilt.
- **Teorema de Dirac**. Sea $G$ un grafo simple y conexo con $n$ v. Si $\delta(v) \geq \frac{n}{2}$ para todos los v. entonces es hamiltoniano.
- **Teorema de Ore**. Sea $G$ un grafo simple y conexo con $n$ v., $n \geq 3$. Si $\delta(v) + \delta(w) \geq n$ para cualquier para de v. **no adyacentes**, entonces es hamiltoniano.
- **Teorema (condición necesaria)** si $G = (V, E)$ es Hamiltoniano, entonces para cada conjunto $U, U \subset V$, el grafo $G - U$ tiene, a lo sumo, $|U|$ componentes conexas.  
- El número de ejes de un grafo simple es igual a $\binom{n}{2}$ siendo $n = |V|$.
