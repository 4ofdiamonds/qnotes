# FTC, part 2
## Theorem (Fundamental theorem of calculus, part 2) If $f$ is continuous on $[a,b]$, and F(x) is an antiderivative of f, then

$$\begin{align}
\int _{a}^b f(x) dx=F(b)-F(a) =: F(x)\Bigg|_{a}^b\\
\end{align}$$
# FTC, part 1
## Theorem (The fundamental theorem of calculus, Part 1):
- If f is continuous on $[a,b]$, then the function g defined by
$$\begin{align}
g(x)=\int _{a}^xf(t) dt &  & a\leq x\leq b
\end{align}$$
- Is continuous on $[a,b]$ and differentiable on (a,b) with g'(x)=f(x)
## Proof sketch from FTC(2)
- Assume F(x) is antiderivative of f
$$\begin{align}
F'(x) & =f(x) \\
g(x) & = \int_{a}^xF'(t)dt=F(x)-F(a) \\
\implies g'(x) & =F'(x)=f(x)
\end{align}$$
# Application of FTC(1)
## Find the derivative of each of the following functions
$$\begin{align}
f(x) & =\int_{0}^x \sqrt{ 1+t^2 } dt \\
f'(x) &  =\sqrt{ 1+x^2 }  \\
 \\
g(x) & = \int_{x}^5 e^{-t^2}dt \\
g'(x) & =-e^{-x^2} \\
 \\
h(x) & =\int_{2}^{x^3}\sin(\ln t)dt \\
 & = F(x^3)-F(2) \\
h'(x) & =\frac{d}{dx} F(x^3) \\
 & =F'(x^3) \cdot 3x^2 \\
 & =\sin \ln x^3 \cdot 3x^2 \\
 \\
k'(x) & = \int_{\sin x}^{\ln x} e^t \arcsin t dt \\
 & =-\int_{0}^{\sin x} e^t \arcsin t dt+\int_{0}^{\ln(x)} e^t \arcsin t dt \\
k'(x) & =-(e^{\sin x}\arcsin(\sin x))\cos x+e^{\ln x}\arcsin(\ln x) \cdot \frac{1}{x} \\
 & =-e^{\sin x}\cdot x \cos x+\arcsin(\ln x)
\end{align}$$
## Curve Sketching of antiderviatives
![[Untitled 5-1762275321594.jpeg]]
$$\begin{align}
\text{Let }g(x) & =\int_{0}^x f(t) dt \\
g(7) & =A_{1}-A_{2}+A_{3} \\
 & = 3
\end{align}$$
### Sketch g
- y-intercept: $g(0)=0 \implies (0,0)$
- x-intercepts: $g(x)=0 \implies x=0,4,6$
- Increasing/decreasing
$$\begin{align}
g'(x)=\frac{d}{dx}\left( \int_{0}^x f(t )dt \right)=f(x)
\end{align}$$
