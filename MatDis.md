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
$$ a_n = (\alpha_{10} + \alpha_11 n + ... + \alpha_{1,m_{1-1}}n^{m_1 - 1})r_1^n + (\alpha_{20} + \alpha_{21}n + ... + \alpha_{2, m_{2 - 1}} n^{m_{2 - 1}})r_2^n + ... + (\alpha_{s0} + \alpha_{s1}n + ... + \alpha_{s, m_{s - 1}}n^{m_{s - 1}}) r_s^n$$
Ej.: $a_n = 4a_{n - 1} - 4a_{n-2}$ , $a_0 = 2, a_1 = 8$ || $r^2 - 4r + 4 = 0$ || $(r-2)^2$ || $r_1 = 2, m_1 = 2$ 
$a_n = (\alpha_{1,0} + \alpha_{1,1}n)2^n$  
$a_0 = (\alpha_{10} + \alpha_{11}0)2^0$ = 2 => $\alpha_{10} = 2$
$a_1 = (2 + \alpha_{11}1)2^1 = (2 + \alpha_{11})2 = 8$ =>$\alpha_{11} = 2$
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