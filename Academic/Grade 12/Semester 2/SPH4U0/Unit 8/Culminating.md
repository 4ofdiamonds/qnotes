---
lastSync: Fri Jun 13 2025 03:39:25 GMT-0400 (Eastern Daylight Time)
---
 ## Rough Notes

Vertical Components:
$$\begin{align}
a & =\frac{dv}{dt} \\
 & =\frac{R}{\frac{1}{FPS}} \\
 & =RFps \\ \\

a_{\text{total}} & =\vec{a}_{gravity}+\vec{a}_{\text{round}} \\
 & \boxed{a=800+Rfps} \\ \\

\frac{dv}{dt} & =800+Rfps \\
\int_{v_{0}}^v \,dv & =\int_{t_{0}}^t 800+Rfps \,dt \\
v\Bigg|_{v_{0}}^v & =(800+Rfps)t \Bigg|_{t_{0}}^t\\
v-v_{0} & =(800+Rfps)(t-t_{0}) \\
 & \boxed{v=v_{0}+(800+Rfps)(t-t_{0}) } \\ \\

\frac{dx}{dt} & = v_{0}+(800+Rfps)(\Delta t) \\
\int_{x_{0}}^x \,dx & = \int_{t_{0}}^tv_{0}+(800+Rfps)(\Delta t)\,dt \\
x\Bigg|_{x_{0}}^x & = v_{0}+(800+Rfps)\left( \frac{1}{2}\Delta t^2\right) \Bigg|_{t_{0}}^t \\
 & \boxed{ \Delta x =v_{0}+\frac{1}{2}(800+Rfps)\Delta t^2 }
\end{align}$$
Horizontal Components (x or y)
$$\begin{align}
a & =\frac{dv}{dt} \\
\text{Current Speed} & = \vec{v} \cdot \vec{w} \\
\text{Add Speed} & = \text{Current Speed} \\
& =\frac{\text{AccelSpeed} \times \text{WishVelocity}}{\frac{1}{fps}} \\
& =\frac{(\text{Grounded Wish Speed} \times \text{sv accelerate} \times \text{frametime}) \times \text{WishVelocity}}{\frac{1}{fps}} \\
& =\frac{\left( 190 \times 1\times \frac{1}{fps} \right) \times \text{WishVelocity}}{\frac{1}{fps}}
\end{align}$$
Components
$$\begin{align}
\vec{v} & =[x, y]\\
\vec{w} & =[190 \cos \theta, 190\sin \theta] \\
\text{Dot Speed} & = \vec{v} \cdot \vec{w} \\
\text{Add Speed} & = |\vec{w}|-\text{Dot Speed} \\
\text{Accel Speed} & = 1\times 190 \times \frac{1}{fps} \\ \\
 & \text{If Add speed < 0} \\ \\

\Delta v  & \boxed{ =0 } \\ \\
& \text{If Accel Speed > Add Speed} \\ \\
\Delta v & =\text{Add Speed} \times \vec{w} \\
& =(|\vec{w}|-\text{Dot Speed}) \times \vec{w} \\
& \boxed{ =(|\vec{w}|-\vec{v} \cdot \vec{w}) \times \vec{w} } \\ \\

 & \text{If Accel Speed < Add Speed} \\  \\

\Delta v & =\text{Accel Speed} \times \vec{w} \\
& \boxed{ = 1\times 190 \times \frac{1}{fps} \times \vec{w} } \\ \\
\end{align}$$
Expanded
$$\begin{align}
\Delta v & =(\sqrt{ 190\cos \theta^2+190 \sin \theta^2 }-v_{x} \times 190\cos \theta+v_{y} \times 190 \sin \theta)\times (190\cos \theta, 190 \sin \theta) \\ \\
 & \text{Horizontal} \\
\Delta v & = (\sqrt{ 190\cos \theta^2+190 \sin \theta^2 }-v_{x} \times 190\cos \theta+v_{y} \times 190 \sin \theta)\times (190\cos \theta) \\
\Delta v & = (190-|\vec{v}||\vec{w}|\cos \theta)\times (190, \theta)\\ \\
\Delta v & =\frac{190}{fps}\times (190 \cos \theta, 190 \sin \theta)
\end{align}$$
Optimal Angle
$$\begin{align}
 & \text{When Add Speed = Accel Speed is the optimal angle} \\
190-|w||v|\cos \theta  & = \frac{1 \times 190}{fps} \\
190-\frac{1 \times190}{fps} & =v \cos \theta \\
\frac{190fps-1 \times190}{fps} & =v\cos \theta \\
\frac{190fps-1 \times190}{v fps} & =\cos \theta \\
\frac{190-\frac{1 \times190}{fps}}{v} & =\cos \theta
\end{align}$$
$$$$
## Circle Strafe
$$\begin{align}
\text{Variables: } &  c=5.5 \\
 & a=
\end{align}$$
## Bounce
$$\begin{align}

\end{align}$$
## Air Acceleration
$$\begin{align}
cos(θ) & =\frac{320−a}{v} \\
\frac{​dv}{dt}​ & =a⋅cos(θ) \\
\frac{​dv}{dt} & ​=a⋅\frac{320−a}{v} \\
v\,dv & =a(320−a)\,dt \\
∫v\,dv & =∫a(320−a)\,dt \\
\frac{1}{2}v^2 & =a(320−a)t+C \\
\frac{1}{2}v^2 & =\cancel{ a(320−a)(0) }+C \\
c & =\frac{1}{2}v^2 \\ \\

\frac{1}{2}v^2 & =a(320−a)t+\frac{1}{2}v_{0}^2​ \\
v& =\sqrt{ 2a(320−a)t+v_{0}^2 }
\end{align}$$
$$\begin{align}
a & =190 \\
\theta  & =\text{angle between accel and velocity} \\
T & = \text{frame time} \\
 \\
 & \text{Here only the component of acceleration perpendicular to velocity } \\
a⊥​& =a⋅sin(θ) \\
\frac{dv}{dt} & =a \cdot \sin \theta \\ \\

 & \text{Since:} \\
sin(θ) & =\sqrt{ 1−cos^2(θ) } \\ \\

 & \text{and at the optimal angle:} \\
cos(θ) & =\frac{320−a}{v} \\
 & \text{Then:} \\ \\

\frac{dv}{dt} & =a \sqrt{ 1-\left( \frac{320-a}{v(t)} \right)^2 } \\
\frac{1}{\sqrt{ 1-\left( \frac{320-a}{v} \right)^2 }}\,dv & =a \,dt \\
 & \text{Let }k=320−a​: \\
\int\frac{1}{\sqrt{ 1-\left( \frac{k}{v} \right)^2 }}\,dv & =a \int\,dt  \\
\int\frac{1}{\sqrt{ 1-\left( \frac{k}{v} \right)^2 }}\,dv & = at+C \\
\int\frac{v}{\sqrt{ v^2-k^2}}\,dv & = at+C \\ \\

 & \text{On the left hand side} \\
u=v^2-k^2  & \implies du=2v\,dv \\
\int\frac{v}{\sqrt{ v^2-k^2}}\,dv & =\frac{1}{2}\int \frac{du}{\sqrt{ u }} \\
 & =\sqrt{ v^2-k^2 } \\
 \\
 & \text{So:} \\
\sqrt{ v^2-k^2 } & =at+C \\

\end{align}$$