# Tarea 2. Producto de matrices triangulares

## Entradas de la matriz

### Pregunta 1

Los elementos estrictamente inferiores son los que se encuentran por debajo de la diagonal principal.

$A = 
 \begin{pmatrix}
  a_{11} & a_{12} & a_{13} & a_{14} & a_{15} \\
  \bf{a_{21}} & a_{22} & a_{23} & a_{24} & a_{25} \\
  \bf{a_{31}} & \bf{a_{32}} & a_{33} & a_{34} & a_{35} \\
  \bf{a_{41}} & \bf{a_{42}} & \bf{a_{43}} & a_{44} & a_{45} \\
  \bf{a_{51}} & \bf{a_{52}} & \bf{a_{53}} & \bf{a_{54}} & a_{55}
 \end{pmatrix}$
 
Que son los elementos $a_{ij}$, $\forall \text{ } i > j$.
 
### Pregunta 2
 
$a_{11} \to$ diagonal principal

$a_{23} \to$ diagonal superior

$a_{15} \to$ diagonal superior

$a_{21} \to$ diagonal inferior

$a_{32} \to$ diagonal inferior

$a_{44} \to$ diagonal principal

$a_{53} \to$ diagonal inferior

### Pregunta 3

$A_{ij}$ está en la diagonal principal $\Leftrightarrow$ i = j

$A_{ij}$ está por encima de la diagonal principal $\Leftrightarrow$  i < j

$A_{ij}$ está por debajo de la diagonal principal $\Leftrightarrow$  i > j

## Definiendo los conjuntos de matrices triangulares superiores e inferiores

### Pregunta 4

Conjunto de las matrices triangulares inferiores:

$L_n(\mathbb{K}) := \{A \in \mathcal{M}_n(\mathbb{K}) \text{ }: \text{  } \forall \text{ } i, j \in \{1, \dots , n\} \text{, si }i < j, \text{ entonces } A_{ij} = 0\}$

Conjunto de las matrices triangulares superiores:

$U_n(\mathbb{K}) := \{A \in \mathcal{M}_n(\mathbb{K}) \text{ }: \text{  } \forall \text{ } i, j \in \{1, \dots , n\} \text{, si }i > j, \text{ entonces } A_{ij} = 0\}$

### Pregunta 5

$A \in U_m(\mathbb{K}) \Leftrightarrow A^t \in L_m(\mathbb{K})$

## Producto de matrices triangulares superiores

### Pregunta 6

$AB = 
 \begin{pmatrix}
  a_{11} b_{11} + a_{12} b_{21} + a_{13} b_{31} & a_{11} b_{12} + a_{12} b_{22} + a_{13} b_{32} & a_{11} b_{13} + a_{12} b_{23} + a_{13} b_{33} \\
  a_{21} b_{11} + a_{22} b_{21} + a_{23} b_{31} & a_{21} b_{12} + a_{22} b_{22} + a_{23} b_{32} & a_{21} b_{13} + a_{22} b_{23} + a_{23} b_{33} \\
  a_{31} b_{11} + a_{32} b_{21} + a_{33} b_{31} & a_{31} b_{12} + a_{32} b_{22} + a_{33} b_{32} & a_{31} b_{13} + a_{32} b_{23} + a_{33} b_{33}
 \end{pmatrix}$

$AB = 
 \begin{pmatrix}
  a_{11} b_{11} + a_{12} · 0 + a_{13} · 0 & a_{11} b_{12} + a_{12} b_{22} + a_{13} · 0 & a_{11} b_{13} + a_{12} b_{23} + a_{13} b_{33} \\
  0 · b_{11} + a_{22} · 0 + a_{23} · 0 & 0 · b_{12} + a_{22} b_{22} + a_{23} · 0 & 0 · b_{13} + a_{22} b_{23} + a_{23} b_{33} \\
  0 · b_{11} + 0 · 0 + a_{33} · 0 & 0 · b_{12} + 0 · b_{22} + a_{33} · 0 & 0 · b_{13} + 0 · b_{23} + a_{33} b_{33}
 \end{pmatrix}$

$AB = 
 \begin{pmatrix}
  a_{11} b_{11} & a_{11} b_{12} + a_{12} b_{22} & a_{11} b_{13} + a_{12} b_{23} + a_{13} b_{33} \\
  0 & a_{22} b_{22} & a_{22} b_{23} + a_{23} b_{33} \\
  0 & 0 & a_{33} b_{33}
 \end{pmatrix}$

### Pregunta 7

- Las entradas por debajo de la diagonal principal son **nulas**.
- La matriz $AB \in \mathcal{M}_n (\mathbb{K})$.
- El elemento $(i, i)$−ésimo de la diagonal principal es **el producto del elemento $(i, i)$−ésimo de la matriz $A$ por el elemento $(i, i)$−ésimo de la matriz $B$**.

## Calculando las entradas del producto por debajo de la diagonal principal, en la diagonal principal y por encima de la diagonal principal

### Pregunta 8

Entradas por debajo de la diagonal principal:

- $AB_{75} = \displaystyle\sum_{i=1}^{8} a_{7i}b_{i5} = a_{71}b_{15} + a_{72}b_{25} + a_{73}b_{35} + a_{74}b_{45} + a_{75}b_{55} + a_{76}b_{65} + a_{77}b_{75} + a_{78}b_{85} =\\
\text{        } = 0 · b_{15} + 0 · b_{25} + 0 · b_{35} + 0 · b_{45} + 0 · b_{55} + 0 · 0 + a_{77} · 0 + a_{78} · 0 = 0$

- $AB_{61} = \displaystyle\sum_{i=1}^{8} a_{6i}b_{i1} = a_{61}b_{11} + a_{62}b_{21} + a_{63}b_{31} + a_{64}b_{41} + a_{65}b_{51} + a_{66}b_{61} + a_{67}b_{71} + a_{68}b_{81} =\\
\text{        } = 0 · b_{11} + 0 · 0 + 0 · 0 + 0 · 0 + 0 · 0 + a_{66} · 0 + a_{67} · 0 + a_{68} · 0 = 0$

- $AB_{32} = \displaystyle\sum_{i=1}^{8} a_{3i}b_{i2} = a_{31}b_{12} + a_{32}b_{22} + a_{33}b_{32} + a_{34}b_{42} + a_{35}b_{52} + a_{36}b_{62} + a_{37}b_{72} + a_{38}b_{82} =\\
\text{        } = 0 · b_{12} + 0 · b_{22} + a_{33} · 0 + a_{34} · 0 + a_{35} · 0 + a_{36} · 0 + a_{37} · 0 + a_{38} · 0 = 0$

- $AB_{74} = \displaystyle\sum_{i=1}^{8} a_{7i}b_{i4} = a_{71}b_{14} + a_{72}b_{24} + a_{73}b_{34} + a_{74}b_{44} + a_{75}b_{54} + a_{76}b_{64} + a_{77}b_{74} + a_{78}b_{84} =\\
\text{        } = 0 · b_{14} + 0 · b_{24} + 0 · b_{34} + 0 · b_{44} + 0 · 0 + 0 · 0 + a_{77} · 0 + a_{78} · 0 = 0$

- $AB_{87} = \displaystyle\sum_{i=1}^{8} a_{8i}b_{i7} = a_{81}b_{17} + a_{82}b_{27} + a_{83}b_{37} + a_{84}b_{47} + a_{85}b_{57} + a_{86}b_{67} + a_{87}b_{77} + a_{88}b_{87} =\\
\text{        } = 0 · b_{17} + 0 · b_{27} + 0 · b_{37} + 0 · b_{47} + 0 · b_{57} + 0 · b_{67} + 0 · b_{77} + a_{88} · 0 = 0$

Entradas de la diagonal principal:

- $AB_{77} = \displaystyle\sum_{i=1}^{8} a_{7i}b_{i7} = a_{71}b_{17} + a_{72}b_{27} + a_{73}b_{37} + a_{74}b_{47} + a_{75}b_{57} + a_{76}b_{67} + a_{77}b_{77} + a_{78}b_{87} =\\
\text{        } = 0 · b_{17} + 0 · b_{27} + 0 · b_{37} + 0 · b_{47} + 0 · b_{57} + 0 · b_{67} + a_{77}b_{77} + a_{78} · 0 = a_{77}b_{77}$

- $AB_{11}\displaystyle\sum_{i=1}^{8} a_{1i}b_{i1} = a_{11}b_{11} + a_{12}b_{21} + a_{13}b_{31} + a_{14}b_{41} + a_{15}b_{51} + a_{16}b_{61} + a_{17}b_{71} + a_{18}b_{81} =\\
\text{        } = a_{11}b_{11} + a_{12} · 0 + a_{13} · 0 + a_{14} · 0 + a_{15} · 0 + a_{16} · 0 + a_{17} · 0 + a_{18} · 0 = a_{11}b_{11}$

- $AB_{33}\displaystyle\sum_{i=1}^{8} a_{3i}b_{i3} = a_{31}b_{13} + a_{32}b_{23} + a_{33}b_{33} + a_{34}b_{34} + a_{35}b_{35} + a_{36}b_{36} + a_{37}b_{37} + a_{38}b_{38} =\\
\text{        } = 0 · b_{13} + 0 · b_{23} + a_{33}b_{33} + a_{34} · 0 + a_{35} · 0 + a_{36} · 0 + a_{37} · 0 + a_{38} · 0 = a_{33}b_{33}$

- $AB_{44}\displaystyle\sum_{i=1}^{8} a_{4i}b_{i4} = a_{41}b_{14} + a_{42}b_{24} + a_{43}b_{34} + a_{44}b_{44} + a_{45}b_{54} + a_{46}b_{64} + a_{47}b_{74} + a_{48}b_{84} =\\
\text{        } = 0 · b_{14} + 0 · b_{24} + 0 · b_{34} + a_{44}b_{44} + a_{45} · 0 + a_{46} · 0 + a_{47} · 0 + a_{48} · 0 = a_{44}b_{44}$

- $AB_{88}\displaystyle\sum_{i=1}^{8} a_{8i}b_{i8} = a_{81}b_{18} + a_{82}b_{28} + a_{83}b_{38} + a_{84}b_{48} + a_{85}b_{58} + a_{86}b_{68} + a_{87}b_{78} + a_{88}b_{88} =\\
\text{        } = 0 · b_{18} + 0 · b_{28} + 0 · b_{38} + 0 · b_{48} + 0 · b_{58} + 0 · b_{68} + 0 · b_{78} + a_{88}b_{88} = a_{88}b_{88}$

Entradas por encima de la diagonal principal:

- $AB_{78} = \displaystyle\sum_{i=1}^{8} a_{7i}b_{i8} = a_{71}b_{18} + a_{72}b_{28} + a_{73}b_{38} + a_{74}b_{48} + a_{75}b_{58} + a_{76}b_{68} + a_{77}b_{78} + a_{78}b_{88} =\\
\text{        } = 0 · b_{18} + 0 · b_{28} + 0 · b_{38} + 0 · b_{48} + 0 · b_{58} + 0 · b_{68} + a_{77}b_{78} + a_{78}b_{88} = a_{77}b_{78} + a_{78}b_{88}$

- $AB_{15} = \displaystyle\sum_{i=1}^{8} a_{1i}b_{i5} = a_{11}b_{15} + a_{12}b_{25} + a_{13}b_{35} + a_{14}b_{45} + a_{15}b_{55} + a_{16}b_{65} + a_{17}b_{75} + a_{18}b_{85} =\\
\text{        } = a_{11}b_{15} + a_{12}b_{25} + a_{13}b_{35} + a_{14}b_{45} + a_{15}b_{55} + a_{16} · 0 + a_{17} · 0 + a_{18} · 0 = a_{11}b_{15} + a_{12}b_{25} + a_{13}b_{35} + a_{14}b_{45} + a_{15}b_{55}$

- $AB_{36} = \displaystyle\sum_{i=1}^{8} a_{3i}b_{i6} = a_{31}b_{16} + a_{32}b_{26} + a_{33}b_{36} + a_{34}b_{46} + a_{35}b_{56} + a_{36}b_{66} + a_{37}b_{76} + a_{38}b_{86} =\\
\text{        } = 0 · b_{16} + 0 · b_{26} + a_{33}b_{36} + a_{34}b_{46} + a_{35}b_{56} + a_{36}b_{66} + a_{37} · 0 + a_{38} · 0 = a_{33}b_{36} + a_{34}b_{46} + a_{35}b_{56} + a_{36}b_{66}$

- $AB_{24} = \displaystyle\sum_{i=1}^{8} a_{2i}b_{i4} = a_{21}b_{14} + a_{22}b_{24} + a_{23}b_{34} + a_{24}b_{44} + a_{25}b_{54} + a_{26}b_{64} + a_{27}b_{74} + a_{28}b_{84} =\\
\text{        } = 0 · b_{14} + a_{22}b_{24} + a_{23}b_{34} + a_{24}b_{44} + a_{25} · 0 + a_{26} · 0 + a_{27} · 0 + a_{28} · 0 = a_{22}b_{24} + a_{23}b_{34} + a_{24}b_{44}$

- $AB_{58} = \displaystyle\sum_{i=1}^{8} a_{5i}b_{i8} = a_{51}b_{18} + a_{52}b_{28} + a_{53}b_{38} + a_{54}b_{48} + a_{55}b_{58} + a_{56}b_{68} + a_{57}b_{78} + a_{58}b_{88} =\\
\text{        } = 0 · b_{18} + 0 · b_{28} + 0 · b_{38} + 0 · b_{48} + a_{55}b_{58} + a_{56}b_{68} + a_{57}b_{78} + a_{58}b_{88} = a_{55}b_{58} + a_{56}b_{68} + a_{57}b_{78} + a_{58}b_{88}$

## Deduciendo la fórmula general para las entradas del producto de matrices triangulares superiores

### Pregunta 9

Si A,B $\in \mathcal{M}_8 \mathbb{(K)}$, entonces

$AB_{85} = a_{81}b_{15} + a_{82}b_{25} + \dots + a_{88}b_{85} = \displaystyle\sum_{k=1}^{8} a_{8k}b_{k}5$

Si A,B $\in \mathcal{M}_9 \mathbb{(K)}$, entonces

$AB_{36} = a_{31}b_{16} + a_{32}b_{26} + \dots + a_{39}b_{96} = \displaystyle\sum_{k=1}^{9} a_{3k}b_{k6}$

Siguiendo lo anterior, la fórmula general para

$AB_{ij} = a_{i1}b_{1j} + a_{i2}b_{2j} + \dots + a_{in}b_{nj} = \displaystyle\sum_{k=1}^{n} a_{ik}b_{kj}$

## Partición de la suma

### Pregunta 10

$\displaystyle\sum_{k=1}^{20} s_k = \displaystyle\sum_{k=1}^{7} s_k + \displaystyle\sum_{k=8}^{20} s_k$

$\displaystyle\sum_{k=1}^{29} s_k = \displaystyle\sum_{k=1}^{8} s_k + \displaystyle\sum_{k=9}^{20} s_k + \displaystyle\sum_{k=21}^{29} s_k$

$\displaystyle\sum_{k=1}^{17} = \displaystyle\sum_{k=1}^{10} s_k + \displaystyle\sum_{k=11}^{17} s_k = 10 · 2 + 7 · 3 = 41$

$\displaystyle\sum_{k=1}^{25} = \displaystyle\sum_{k=1}^{12} s_k + \displaystyle\sum_{k=13}^{19} s_k + \displaystyle\sum_{k=20}^{25} s_k = 12 · 7 + 7 · 9 + 6 · 5 = 177$

$\displaystyle\sum_{k=1}^{31} = \displaystyle\sum_{k=1}^{9} s_k + \displaystyle\sum_{k=25}^{31} s_k = 9 · 0 + 7 · 0 = 0$

$\displaystyle\sum_{k=1}^{27} = \displaystyle\sum_{k=1}^{7} s_k + \displaystyle\sum_{k=12}^{19} s_k + \displaystyle\sum_{k=24}^{27} s_k = 7 · 0 + 8 · 0 + 4 · 0 = 0$

## Entradas del producto por debajo de la diagonal principal con partición de sumas

### Pregunta 11

$AB_{93} = \displaystyle\sum_{k=1}^{3} a_{9,k}b_{k,3} + \displaystyle\sum_{k=4}^{8} a_{9,k}b_{k,3} + \displaystyle\sum_{k=9}^{15} a_{9,k}b_{k,3}$

El primer sumando cumple que $a_{9,k} = 0 \text{ } \forall \text{ } k \in \{1, \dots, 3\}$ ya que, $A \in U_{15}$, con lo cual $a_{ij} = 0$ si, y solo si, $i > j$.

El segundo sumando cumple tanto que $a_{9,k} = 0 \text{ } \forall \text{ } k \in \{4, \dots, 8\}$ como que $b_{k,3} = 0 \text{ } \forall \text{ } k \in \{4, \dots, 8\}$ porque en ambos casos $i > j$.

El tercer sumando cumple que $b_{k,3} = 0 \text{ } \forall \text{ } k \in \{9, \dots, 15\}$ ya que de nuevo se cumple que $i > j$.

Por tanto,

$AB_{93} = \displaystyle\sum_{k=1}^{3} 0 · b_{k,3} + \displaystyle\sum_{k=4}^{8} 0 · 0 + \displaystyle\sum_{k=8}^{9} a_{9,k} · 0 = 0$

---

$AB_{31} = \displaystyle\sum_{k=1}^{1} a_{3,k}b_{k,1} + \displaystyle\sum_{k=2}^{2} a_{3,k}b_{k,1} + \displaystyle\sum_{k=3}^{15} a_{3,k}b_{k,1}$

El primer sumando cumple que $a_{3,k} = 0 \text{ } \forall \text{ } k \in \{1\}$ ya que, $A \in U_{15}$, con lo cual $a_{ij} = 0$ si, y solo si, $i > j$.

El segundo sumando cumple tanto que $a_{3,k} = 0 \text{ } \forall \text{ } k \in \{2\}$ como que $b_{k,1} = 0 \text{ } \forall \text{ } k \in \{2\}$ porque en ambos casos $i > j$.

El tercer sumando cumple que $b_{k,1} = 0 \text{ } \forall \text{ } k \in \{3, \dots, 15\}$ ya que de nuevo se cumple que $i > j$.

Por tanto,

$AB_{31} = \displaystyle\sum_{k=1}^{1} 0 · b_{k,1} + \displaystyle\sum_{k=2}^{2} 0 · 0 + \displaystyle\sum_{k=3}^{15} a_{3,k} · 0 = 0$

---

$AB_{15,3} = \displaystyle\sum_{k=1}^{3} a_{15,k}b_{} + \displaystyle\sum_{k=4}^{14} a_{15,k}b_{} + \displaystyle\sum_{k=15}^{15} a_{15,k}b_{}$

El primer sumando cumple que $a_{15,k} = 0 \text{ } \forall \text{ } k \in \{1, 2, 3\}$ ya que, $A \in U_{15}$, con lo cual $a_{ij} = 0$ si, y solo si, $i > j$.

El segundo sumando cumple tanto que $a_{15,k} = 0 \text{ } \forall \text{ } k \in \{4, \dots 14\}$ como que $b_{k,3} = 0 \text{ } \forall \text{ } k \in \{4, \dots, 14\}$ porque en ambos casos $i > j$.

El tercer sumando cumple que $b_{k,3} = 0 \text{ } \forall \text{ } k \in \{15\}$ ya que de nuevo se cumple que $i > j$.

Por tanto,

$AB_{15,3} = \displaystyle\sum_{k=1}^{3} 0 · b_{k,1} + \displaystyle\sum_{k=4}^{14} 0 · 0 + \displaystyle\sum_{k=15}^{15} a_{15,k} · 0 = 0$

## Entradas diagonales del producto con partición de sumas

### Pregunta 12

$AB_{55} = \displaystyle\sum_{k=1}^{4} a_{5,k}b_{k,5} + a_{55}b_{55} + \displaystyle\sum_{k=6}^{15} a_{5,k}b_{k,5} = 0 + a_{55}b_{55} + 0 = a_{55}b_{55}$

$AB_{10,10} = \displaystyle\sum_{k=1}^{9} a_{10,k}b_{k,10} + a_{10,10}b_{10,10} + \displaystyle\sum_{k=11}^{15} a_{10,k}b_{k,10} = 0 + a_{10,10}b_{10,10} + 0 = a_{10,10}b_{10,10}$

$AB_{15,15} = \displaystyle\sum_{k=1}^{14} a_{15,k}b_{k,15} + a_{15,15}b_{15,15} = 0 + a_{15,15}b_{15,15}= a_{15,15}b_{15,15}$

## Entradas del producto por encima de la diagonal principal con partición de sumas

### Pregunta 13

$AB_{15} = \displaystyle\sum_{k=1}^{5} a_{1,k}b_{k,5} + \displaystyle\sum_{k=6}^{15} a_{1,k}b_{k,5} = \displaystyle\sum_{k=1}^{5} a_{1,k}b_{k,5}$

$AB_{10,13} = \displaystyle\sum_{k=1}^{9} a_{10,k}b_{k,13} + \displaystyle\sum_{k=10}^{13} a_{10,k}b_{k,13} + \displaystyle\sum_{k=14}^{15} a_{10,k}b_{k,13} = \displaystyle\sum_{k=10}^{13} a_{10,k}b_{k,13}$

$AB_{69} = \displaystyle\sum_{k=1}^{5} a_{6,k}b_{k,9} + \displaystyle\sum_{k=6}^{9} a_{6,k}b_{k,9} + \displaystyle\sum_{k=10}^{15} a_{6,k}b_{k,9} = \displaystyle\sum_{k=6}^{9} a_{6,k}b_{k,9}$

## Demostración del caso general

### Pregunta 14

En el caso de que $A, B \in U_n(\mathbb{K})$, calcula la fórmula para las entradas diagonales $AB_{ii}$.

$AB_{ii} = \displaystyle\sum_{k=1}^{i-1} a_{ik}b_{ki} + a_{ii}b_{ii} + \displaystyle\sum_{k=i+1}^{n} a_{ik}b_{ki} = 0 + a_{ii}b_{ii} + 0 = a_{ii}b_{ii}$

---

En el caso de que $A, B \in U_n(\mathbb{K})$, calcula la fórmula para las entradas no triviales $AB_{ij}$ con $i \leq j$.

$AB_{ij} = \displaystyle\sum_{k=1}^{i-1} a_{ik}b_{kj} + \displaystyle\sum_{k=i+1}^{j} a_{ik}b_{kj} + \displaystyle\sum_{k=j+1}^{n} a_{ik}b_{kj} = \displaystyle\sum_{k=i+1}^{j} a_{ik}b_{kj}$

---

Enuncia y demuestra el resultado para matrices triangulares inferiores. Calcula para este caso las fórmulas de las entradas diagonales y las entradas no triviales.

El Teorema enuncia lo siguiente: *El producto de dos matrices triangulares inferiores es una matriz triangular inferior*.

Por lo tanto, lo que queremos demostrar es que dadas $A, B \in L_n(\mathbb{K})$, el producto $AB \in L_n(\mathbb{K})$.

Sean $i, j \in \{1, 2,\dots, n\}$ tales que $i < j$. Demostremos pues que las entradas $AB_{ij} = 0$.

Por definición del producto de matrices, la entrada $(i, j)$−ésima de la matriz producto $AB$ se da del siguiente modo:

$AB_{ij} = \displaystyle\sum_{k=1}^{n} a_{ik}b_{kj}$

Como las matrices $A,B$ son triangulares inferiores, tenemos que

$A_{ik} = 0 \text{ } \forall \text{ } i, k \in {1, 2,\dots, n} \text{ tales que } i < k$

$B_{kj} = 0 \text{ } \forall \text{ } j, k \in {1, 2,\dots, n} \text{ tales que } k < j$

De este modo, partimos la suma en 3 sumandos:

$AB_{ij} = \displaystyle\sum_{k=1}^{j} a_{ik}b_{kj} + \displaystyle\sum_{k=j+1}^{i-1} a_{ik}b_{kj} + \displaystyle\sum_{k=i}^{n} a_{i}b_{kj} = 0 + 0 + 0 = 0$

Donde el primer sumando vale 0 porque para todo $k \in \{1,\dots, j\}, k \geq j > i$; el segundo sumando es 0 porque $\forall k \in \{j + 1,\dots, i − 1\}, j > k > i$; y, finalmente, el último sumando es nulo porque para todos los valores de $k, k \in \{i,\dots, n\}, j > i \geq k$.

Entradas diagonales $AB_{ii}$.

$AB_{ii} = \displaystyle\sum_{k=1}^{i-1} a_{ik}b_{ki} + a_{ii}b_{ii} + \displaystyle\sum_{k=i+1}^{n} a_{ik}b_{ki} = 0 + a_{ii}b_{ii} + 0 = a_{ii}b_{ii}$

Entradas no triviales $AB_{ij}$ con $i \geq j$.

$AB_{ij} = \displaystyle\sum_{k=1}^{i-1} a_{ik}b_{kj} + \displaystyle\sum_{k=i+1}^{j} a_{ik}b_{kj} + \displaystyle\sum_{k=j+1}^{n} a_{ik}b_{kj} = \displaystyle\sum_{k=i+1}^{j} a_{ik}b_{kj}$

---

Enuncia y demuestra el resultado para matrices diagonales.

El Teorema enuncia lo siguiente: *El producto de dos matrices diagonales es una matriz diagonal*.

Como se ha demostrado que la suma de matrices triangulares superiores es una matriz triangular superior y que la suma de matrices triangulares inferiores es una matriz inferior, el producto de dos matrices diagonales se puede descomponer en la suma de tres sumandos donde el primer sumando represente el producto de los elementos de las matrices inferiroes, el segundo sumando represente el producto de las matrices diagonales y el trecer sumando represente el producto de los elemetnos de las matrices superiores. Sabiendo que el resultado del producto de los elementos de las matrices inferiroes es igual a 0 y que el resultado del producto de los elementos de las matrices superiores es igual a 0, el resultado final será el producto de los elementos de las matrices diagonales.
