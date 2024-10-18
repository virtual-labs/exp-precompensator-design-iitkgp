# Theory

Linear time invariant system may be represented in state space form by the following equations:<br/>
State equation:
$$ \dot{x}(t)=A x(t)+B u(t) \tag{1a} $$
Output equation:
$$ y(t)= C x(t) \tag{1b} $$
<b><i>State feedback design:</i></b> <br>
A necessary and sufficient condition for arbitrary pole placement is that the pair (A, B) must be controllable.<br/>
Control input:
$$ u(t)= - K x(t) \tag{2} $$
where, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">K</span> is the state feedback gain vector,i.e.,
$$ K = [k_1 \ k_2 \ ... \ k_n]  $$
With this control input, the closed loop system is as follows:
$$ \dot{x}(t)=(A-BK) x(t)  $$
The characteristic equation of the closed loop system is,
$$ |sI-(A-BK)|=0  $$
For <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">n</span>th order system, the characteristic equation is,
$$ s^n + k_n s^{n-1} + k_{n-1} s^{n-2} + ... + k_1=0 \tag{3} $$
The desired closed loop poles are <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">P</span><sub><span style="font-family:Bodoni MT;font-style:italic;font-size:18px">1</span></sub>, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">P</span><sub><span style="font-family:Bodoni MT;font-style:italic;font-size:18px">2</span></sub>, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">P</span><sub><span style="font-family:Bodoni MT;font-style:italic;font-size:18px">3</span></sub>, ... , <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">P</span><sub><span style="font-family:Bodoni MT;font-style:italic;font-size:18px">n</span></sub>.
Then the desired characteristic equation is:
$$ (s-P_1)(s-P_2)(s-P_3)...(s-P_n)=0 \tag{4} $$
The required state feedback gain (<span style="font-family:Bodoni MT;font-style:italic;font-size:18px">K</span>) vector elements are obtained by comparing the matching coefficients of (3) and (4).
<br/><br/>

<b><i>Pre-compensator design:</i></b> <br>
Control input:
$$ u(t)= - K x(t)+Nr(t) \tag{5} $$
With this control input, the closed loop system is as follows:
$$ \dot{x}(t)=(A-BK) x(t)+ B N r(t) \tag{6} $$
In steady state,
$$ r(t)=r_s, \ x(t)=x_s, \ u(t)=u_s, \ y(t)=y_s, \ \dot{x}(t)=0 \ and \ y_s=r_s \tag{7} $$
From (6) and (7),
$$ 0=(A-BK) x_s+ B N r_s \tag{8} $$
$$ y_s= C x_s \tag{9} $$
From (8),
$$ (A-BK) x_s = - BN r_s $$
$$ x_s = -(A-BK)^{-1}BN r_s \tag{10} $$
From (9) and (10),
$$ y_s = - C (A-BK)^{-1} BN r_s \tag {11}$$
From (7) and (11),
$$ y_s = - C (A-BK)^{-1} BN y_s $$
$$ 1 = - C (A-BK)^{-1} BN $$
$$ N = \frac{-1}{C (A-BK)^{-1} B} \tag{12} $$
where, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">N</span> is the pre-compensator gain. <br/><br/>

<b><i>State Space Model of Inverted Pendulumn on cart:</i></b> <br>
The system consists of an inverted pendulum mounted to a motorized cart. Its popularity derives in part from the fact that it is unstable without control, that is, the pendulum will simply fall over if the cart isn't moved to balance it. 
Additionally, the dynamics of the system are nonlinear. The objective of the control system is to balance the inverted pendulum by applying a force to the cart that the pendulum is attached. A real-world example that relates directly to this inverted pendulum system is the attitude control of a booster rocket at takeoff.</br>
In this case we will consider a two-dimensional problem where the pendulum is constrained to move in the vertical plane shown in the figure below. For this system, the control input is the force <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">F</span> that moves the cart horizontally and the outputs are the angular position of the pendulum &theta; and the horizontal position of the cart <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">x</span>. </br>
<div align="center">
<img class="img-fluid"  src="./images/Inverted_Pendulum.png" alt=""><br>        
<figcaption style="color:black"> Fig.1. Invereted Pendulum on Cart</figcaption>						  
</div><br/>
where, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">M</span> is mass of the cart (kg), <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">m</span> is mass of the pendulum (kg), 
<span style="font-family:Bodoni MT;font-style:italic;font-size:18px">b</span> is coefficient of friction for cart (N/m/sec), <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">l</span> is length to pendulum center of mass (meters), <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">I</span> is mass moment of inertia of the pendulum (kg.m<sup>2</sup>)
<span style="font-family:Bodoni MT;font-style:italic;font-size:18px">F</span> is force applied to the cart, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">x</span> is cart position coordinate, &theta; is pendulum angle from vertical (down).</br></br>
The linearized equations of motion can also be represented in state-space form:</br>
Let &Phi; represent the deviation of the pedulum's position, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">u</span> has been substituted for the input <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">F</span>.
<div align="center">
<img class="img-fluid"  src="./images/SS_Pendulum_Cart.png" alt=""><br>  


</div><br/>





<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>