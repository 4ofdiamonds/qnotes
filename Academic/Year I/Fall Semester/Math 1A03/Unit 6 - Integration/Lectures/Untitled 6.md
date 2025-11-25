# How to use the substitution rule
$$\begin{align}
 & \int 2x\sqrt{ 1+x^2 }dx \\
 \\
u & =1+x^2 \\
du & =2x \cdot dx \\
 \\
\int \sqrt{ u } \,du&= \int u^{1/2}du \\
 & =\frac{u^{3/2}}{\frac{3}{2}} \\
 & =\frac{2u^{3/2}}{3} \\
 & =\frac{2}{3}(1+x^2)^{3/2} 
\end{align}$$
# Why it works
## Theorem (substitution rule for indefinite integrals)
If $u=g(x)$ is differentiable function whose range is an interval I and f is continuous of I, then
$$\begin{align}
\int f(g(x))g'(x)dx & =\underbrace{ \int f(u)du }_{ F(u)+c } \\
\frac{d}{dx}F(u) & =f(u)=f(g(x)) \\
\frac{d}{dx}F(g(x)) & =F'(g(x)) \cdot g'(x)=f(g(x))g'(x)
\end{align}$$
## Theorem (substitution rule for definite integrals)
If g' is continuous on $[a,b]$ and f is continuous on the range of u=g(x), then
# More advanced examples
## On choosing u
>[!NOTE] Do not mix x and u in integrals

$$\begin{align}
 & \int_{2}^3\sqrt{ 1+x^2 }x^3 \,dx \\
 \\
u & =1+x^2 \iff x^2=u-1\\
du & =2x \,dx \\
 \\
 & =\int_{2}^3 \sqrt{ 1+x^2 }x^2 x\, dx \\
 \\
x & =2 \implies u=1+2^2=5 \\
x & =3 \implies u=1+3^2 =10 \\
 \\
 & =\int_{5}^{10} \sqrt{ u } (u-1) \cdot \frac{1}{2} du \\
 & =\frac{1}{2} \int_{5}^{10} u^{5/2}-u^{3/2} \Bigg|_{5}^{10} \\
 & =\left( \frac{10}{5}^{5/2} -\frac{10}{3}^{3/2}-\left( \frac{5}{5}^{5/2} -\frac{5}{3}^{3/2} \right)\right)
\end{align}$$
## Example
$$\begin{align}
\int \tan x\,dx & =\int \frac{\sin x}{\cos x}dx \\
 \\
u & =\cos x \\
du & =-\sin x \,dx \\
 \\
 & =\int\frac{-1}{u} \,du \\
 & =-\ln|u| +c \\ \\
 & =-\ln(\cos x)+c \\
 & \boxed{ =\ln|\sec x|+c }
\end{align}$$
$$\begin{align}
\int \frac{x^2}{\sqrt{ 1-x }}\,dx \\ \\
u & =1-x \implies x=1-u \\
du & =-dx \\
 \\
\int\frac{(1-u)^2}{\sqrt{ u }} \cdot -1\,du  & = \int\frac{1-2u+u^2}{\sqrt{ u }}du \\
 & =\int-u^{-1/2}+2u^{1/2}-u^{3/2}du \\
 & =\frac{-u^{1/2}}{\frac{1}{2}}+2 \frac{u^{3/2}}{\frac{3}{2}}-\frac{u^{5/2}}{\frac{5}{2}}+c
\end{align}$$
$$\begin{align}
\int\frac{\ln x}{x}dx \\
u & =\ln x \\
du & =\frac{1}{x}dx \\
\int u\,du  & = \frac{\ln x^2}{2}+c
\end{align}$$
# Integrating odd/even functions
![[Untitled 6-1762448018426.jpeg]]
Proof of ii
$$\begin{align}
 & \text{Suppose }f\text{ is odd: }f(-x) =-f(x) \\
\int_{-a}^{a}f(x)\,dx & =\underbrace{ \int_{-a}^0f(x)\,dx }_{ I_{1} }+\underbrace{ \int_{0}^af(x)\,dx }_{ I_{2} } \\
 & \text{We show that }I_{1}=-I_{2} \\
I_{1} & =\int_{-a}^0 f(x)\,dx \\
 & =\int_{0}^{-a} -f(x)\,dx \\
 & = \int_{0}^- f(-x)\,dx \\ \\
u & =-x \\
du & =-dx \\
x =0  & \implies u=0 \\
x =-u  & \implies u=u
\\ \\
 & = \int_{0}^a f(u) (-1)\,du \\
 & =-\int_{0}^a f(u) \,du \\
 & =-I_{2}
\end{align}$$
![[Untitled 6-1762448460889.jpeg]]
