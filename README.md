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

$\dot{x}(t)$ = $\begin{bmatrix} 0 & 1 \\ \frac{-k}{M}& \frac{-b}{M} \\ \end{bmatrix}$x(t) +  $\begin{bmatrix} 0\\ \frac{1}{M} \end{bmatrix}$F(t))

가 된다. 

## P.3-3
문제를 바탕으로 전달함수를 식으로 작성하면 
$\frac{Y(s)}{R(s)} =\frac{k}{s+50}$

이때 $R(s)=\frac{1}{s}$이므로 

$Y(s) =\frac{k}{s(s+50)}$

이를 역라플라스 변환을 통해 나타내면 

$y(t)=\frac{k}{50}(1-e^{-50t})$

$t\to inf \frac{k}{50}$이 된다.

이를 정리하면

$\displaystyle \lim_{t \to inf}y(t) =\displaystyle \lim_{s \to 0}sY(s)=\frac{k}{50}=1$

따라서 k=50이다.


## P.3-5


$m\ddot{x}(t)+b\dot{x}(t)+kx(t)=u(t)$

이를 라플라스 변환을 하면

$ms^{2}X(s)+bsX(s)+kX(s)=U(s)$

$X(s)=\frac{1}{s^{2}+\frac{b}{m}s+\frac{k}{m}}$

이를 역라플라스변환을 하면

$x(t)=e^{-\sqrt(\frac{b}{2m})t}\frac{1}{\sqrt(\frac{2k-b}{2m})}sin(\frac{2k-b}{2m}t)$

가 된다.


## P.3-12


다음 문제를 미분방정식으로 나타내면

$M\ddot{x}+b(\dot{x}-\dot{y})+k(x-y)=F(t)$

$m\ddot{y}+b(\dot{y}-\dot{x})+k(y-x)=0$

이를 라플라스 변환시키고 행렬로 나타내면

$$
\begin{vmatrix}
(Ms^2+bs+k) & -(bs+k) \\
-(bs+k) & (ms^2+bs+k) \\
\end{vmatrix}
$$

$$
\begin{vmatrix}
(X(s)) \\ (Y(s)) 
\end{vmatrix}
$$

=

$$\begin{vmatrix}
F(s) \\ 0
\end{vmatrix}
$$

$\frac{Y(s)}{F(s)}=\frac{\frac{1}{Mm}(bs+k)}{s^2[s^2=(1+\frac{m}{M})(\frac{b}{m}s+\frac{k}{m})]}$

이라는 전달함수가 된다.

## P.3-17


a) 다음 미분방정식을 구하면

$m_{1}\ddot{x}=-(k_{1}+k_{2})x+k_{2}y$

$m_{2}\ddot{y}=k_{2}(x-y)+u(t)$

이라는 2개의 미분방정식이 완성된다.

이를 라플라스 변환시켜서 전달함수를 구하면

$m_{1}s^2X(s)+2X(s)-Y(s)=0$

$m_{2}s^2Y(s)-X(s)+Y(s)=U(s)$

$X(s)=\frac{Y(s)}{m_{1}s^2+2}$

위의 식을 Y(s)를 대입하면 전달함수를 구할 수 있다. 이를 정리하면

$\frac{Y(s)}{U(s)}=\frac{1}{m_{2}s^2-\frac{1}{m_{1}^2s+2}+1}$

이 된다.


