# Matematics
* https://www.markdownlang.com/advanced/math.html

## Basic Math Elements 

<!-- Superscripts -->
$x^2$, $e^{i\pi}$, $2^{10}$

<!-- Subscripts -->
$x_1$, $a_{ij}$, $\log_2 n$

<!-- Combined -->
$x_1^2$, $a_{i,j}^{(k)}$, $\sum_{i=1}^n x_i^2$


## Fractions 
**Markdown**
```markdown
<!-- Basic fractions -->
$\frac{1}{2}$, $\frac{a}{b}$, $\frac{x+y}{x-y}$

<!-- Continued fractions -->
$\frac{1}{1 + \frac{1}{2 + \frac{1}{3 + \cdots}}}$

<!-- Complex fractions -->
$\frac{\partial^2 f}{\partial x^2}$, $\frac{d}{dx}\left(\frac{1}{x}\right)$
```

**Rendered Output**
$\frac{1}{2}$, $\frac{a}{b}$, $\frac{x+y}{x-y}$

$\frac{1}{1 + \frac{1}{2 + \frac{1}{3 + \cdots}}}$

$\frac{\partial^2 f}{\partial x^2}$, $\frac{d}{dx}\left(\frac{1}{x}\right)$

## Operators
```markdown
<!-- Basic operations -->
$+$, $-$, $\times$, $\div$, $\pm$, $\mp$

<!-- Relational operations -->
$=$, $\neq$, $<$, $>$, $\leq$, $\geq$, $\ll$, $\gg$

<!-- Logical operations -->
$\land$, $\lor$, $\lnot$, $\implies$, $\iff$

<!-- Set operations -->
$\in$, $\notin$, $\subset$, $\supset$, $\cup$, $\cap$, $\emptyset$

<!-- Other symbols -->
$\infty$, $\partial$, $\nabla$, $\propto$, $\approx$, $\equiv$
```

<!-- Basic operations -->
$+$, $-$, $\times$, $\div$, $\pm$, $\mp$

<!-- Relational operations -->
$=$, $\neq$, $<$, $>$, $\leq$, $\geq$, $\ll$, $\gg$

<!-- Logical operations -->
$\land$, $\lor$, $\lnot$, $\implies$, $\iff$

<!-- Set operations -->
$\in$, $\notin$, $\subset$, $\supset$, $\cup$, $\cap$, $\emptyset$

<!-- Other symbols -->
$\infty$, $\partial$, $\nabla$, $\propto$, $\approx$, $\equiv$


## Matrices and Determinants
### Basic matrix
**Markdown**
```markdown
<!-- Basic matrix -->
$$
\begin{matrix}
a & b \\
c & d
\end{matrix}
$$
```

**Rendered Output**
$$
\begin{matrix}
a & b \\
c & d
\end{matrix}
$$

### Matrix with parentheses
**Markdown**
```markdown
<!-- Matrix with parentheses -->
$$
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix}
$$
```
**Rendered Output**
$$
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix}
$$


### Determinant
**Markdown**
```markdown
<!-- Determinant -->
$$
\begin{vmatrix}
a & b \\
c & d
\end{vmatrix} = ad - bc
$$
```
**Rendered Output**
$$
\begin{vmatrix}
a & b \\
c & d
\end{vmatrix} = ad - bc
$$



### System of equations
**Markdown**
```markdown
<!-- System of equations -->
$$
\begin{cases}
x + y = 1 \\
2x - y = 0
\end{cases}
$$
```
**Rendered Output**

$$
\begin{cases}
x + y = 1 \\
2x - y = 0
\end{cases}
$$


### Large matrix
**Markdown**
```markdown
<!-- Large matrix -->
$$
\begin{bmatrix}
1 & 0 & \cdots & 0 \\
0 & 1 & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & 1
\end{bmatrix}
$$
```
**Rendered Output**

$$
\begin{bmatrix}
1 & 0 & \cdots & 0 \\
0 & 1 & \cdots & 0 \\
\vdots & \vdots & \ddots & \vdots \\
0 & 0 & \cdots & 1
\end{bmatrix}
$$
