# HW-3
## P.3-1

(a)

적당한 변수로 
 x_{1}=y(t), 
$x_{2}=\dot{y}(t)$

라 두고 식을 작성하면

(b)

$M_{1}\frac{\partial^2 y(t)}{\partial t^2}+b_{1}\dot{y}(t)+ky(t)=F(t)$

라는 미분방정식이 완성된다.

(c)

이제 상태미분방정식으로 표현하면 
이를 라플라스 변환하면

$\dot{x}(t)$ = 

$$
\begin{vmatrix} 
0 & 1 \\ 
\frac{-k}{M}& \frac{-b}{M} \\ 
\end{vmatrix}
x(t) $$
 +
 $$
\begin{vmatrix}
0\\  \frac{1}{M} \\ 
\end{vmatrix} 
 F(t)
 $$

가 된다. 

## P.3-3
문제를 바탕으로 전달함수를 식으로 작성하면 
$L\frac{\mathrm{di} }{\mathrm{d} t}-V_{c}+V_{2}-V_{1}=0$

$C\frac{\partial V}{\partial t}=-i_{L}+i_{R}$

이 둘을 연립하면 다음과 같은 식이 나온다. 

$\frac{\mathrm{di} }{\mathrm{d} t}=V_{c}/L-V_{2}/L+V_{1}/L$

$\frac{\partial V}{\partial t}=-V_{c}/RC-i_{L}/C+V_{2}/RC$

이를 토대로 문제에서 x1은 인덕터 전류 x2는 커패시터 전압이라 하였으므로 위식을 이용해 상태방정식으로 나타내면 

$\dot{x}(t)$
 
=

$$\begin{vmatrix}
 0&1/L  \\
 -1/C&-1/RC  \\
\end{vmatrix} x(t)$$
 +
$$\begin{vmatrix}
 1/L&-1/L  \\
 0&1/RC  \\
\end{vmatrix}$$

$$\begin{vmatrix}
V1 
\\ V2
\end{vmatrix}$$

가 된다.


## P.3-5


$T_{s}=\frac{Y(s)}{U(s)}=\frac{(s+2)}{s(s+8)(s-3)})$

상태변수모델을 구하면 

$$A=\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
0 & -24 & 5 \\
\end{bmatrix}$$

$$b=\begin{bmatrix}
0  \\
0  \\
-1  \\
\end{bmatrix}$$


$$c=\begin{bmatrix}
2 & 1 & 0 \\
\end{bmatrix}$$

가 된다.


## P.3-12


다음 문제를 전달함수를 토대로 상태공간을 모델하

$$A=\begin{bmatrix}
0 & 1 & 0 \\
0 & 0 & 1 \\
-48 & -44 & -12 \\
\end{bmatrix} x$$

 +

$$\begin{bmatrix}
0  \\
0  \\
1  \\
\end{bmatrix} r
$$

이를 상태천이 행렬을 구하기 위해서는 다음과 같은 과정이 필요하다.

$$
det(sI-A)=\begin{bmatrix}
s & -1 & 0 \\
0 & s & -1 \\
48 & 44 & -s-12 \\
\end{bmatrix}
$$

$$
adj(sI-A)=\begin{bmatrix}
s & 0 & 48 \\
-1 & s & 44 \\
0 & -1 & -s-12 \\
\end{bmatrix}
$$

adj와 det을 나누면 [sI-A]의 역행렬이 되고 이를 역라플라스 변환을 하면 상태천이 행렬이 나오게 된다.
1열은 

$$\begin{bmatrix}
-1/14e^-2t + 2/7e^-4t-3/14e^-6t \\
 -1/12e^-2t+ 1/24e^-4t+1/12e^-6t \\
0 \\
\end{bmatrix}
$$

2행은 

$$
\begin{bmatrix}
0 \\
-1/12e^-2t+ 1/24e^-4t+1/12e^-6t \\
11/3e^-2t - 11/6e^-4t-11/6e^-6t \\
\end{bmatrix}
$$

3행은 

$$\begin{bmatrix}
4e^-2t-2e^-4t-2e^-6t \\
-1/12e^-2t+ 1/24e^-4t+1/12e^-6t \\
5/4e^-2t - 2e^+3/G4e^-6t \\
\end{bmatrix}
$$

이 된다.

## P.3-17


전달함수는 
$G(s)=C(sI-A)^{-1}B$
이라는 식으로 구한다.
이를 하기 위해서는 det(sI-A)값을 구하면 
$s^3-14s^2+37s+20$이 되고 
이를 토대로 전달함수에 대한 식을 구하면

$G(s)=\frac{4(s-3)}{s^3-14s^2+37s+20}$

이 된다.


