## Introduction

<div align="center">
<img src="experiment/images/iitkgp.png" width="10%">
</div>

<b>Discipline | <b>Electrical Engineering 
:--|:--|
<b> Lab | <b> Digital Control Laboratory
<b> Experiment|     <b> Control design via pole placement for pendulum on cart with Pre-compensator design and Exp 7

### About the Experiment 

Linear time invariant system may be represented in state space form by the following equations:
</br>
State equation:

$$\dot{x}(t)=A x(t)+B u(t) \tag{1a}$$

Output equation:

$$y(t)= C x(t) \tag{1b}$$

where, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">x</span>(<span style="font-family:Bodoni MT;font-style:italic;font-size:18px">t</span>) is state vector, <span style="font-family:Sitka Text;font-style:italic">y</span>(<span style="font-family:Bodoni MT;font-style:italic;font-size:18px">t</span>) is output vector, 
<span style="font-family:Bodoni MT;font-style:italic;font-size:18px">u</span> is input or control vector, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">A</span> is system matrix, 
<span style="font-family:Bodoni MT;font-style:italic;font-size:18px">B</span> is input matrix, <span style="font-family:Bodoni MT;font-style:italic;font-size:18px">C</span> is output matrix.</br></br>
The controller design for the state variable models involves feeding back all the state variables using appropriate weights to generate the error signal. State feedback allows arbitrary placement of roots of the closed-loop characteristic polynomial. 
It is more powerful and offers greater flexibility than the output feedback that allows only selective placement of closed-loop roots. State feedback assumes that the complete set of state variables is available for feedback. <br/>
The pole placement design refers to the selection of feedback gains for placing the roots of the closed-loop characteristic polynomial at the desired locations in the complex plane. 
The state feedback controller design refers to the selection of individual feedback gains for the complete set of state variables. It is assumed that all the state variables are available for observation. 
The design goal is to improve the transient response of the system. <br/>
Controller design in state-space involves selection of suitable feedback gain vector (K) that imparts desired stability and performance characteristics to the closed-loop system.

        
<div align="center">
<img class="img-fluid"  src="experiment/images/Block diagram for state feedback.png" alt="">

<figcaption style="color:black"> Fig.1. Plant with state feedback </figcaption>
</div>
<br/>
The designed state feedback controller meets transient requirements, but need to address the steady-state error. Pre-compensator will address the steady state error issue. 
The reference signal can be used with a pre-compensator to cancel the steady state error.
<br/>
<div align="center">
<img class="img-fluid"  src="experiment/images/Block diagram with precompensator.png" alt="">

<figcaption style="color:black"> Fig.2. Plant with state feedback and pre-compensator </figcaption>
</div> 



	

<b>Subject matter expertise | <b> **Prof. Alok Kanti Deb**
:--|:--|
<b> Institute | <b>  **Indian Institute of Technology Kharagpur**
<b> Email id|     <b>  **alokkanti@ee.iitkgp.ac.in**
<b> Department |  **Department of Electrical Engineering**
<b>Webpage| <b> http://www.iitkgp.ac.in/department/EE/faculty/ee-alokkanti

### Contributors List

SrNo | Name | VLabs Developer or Integration Engineer | Designation | Department| Institute
:--|:--|:--|:--|:--|:--|
1 | **Kamal Sandeep Karreddula** | Developer | Research Scholar | Department of Electrical Engineering | IIT Kharagpur | 
2 | **Piyali Chattopadhyay** | Integration Engineer | Project Scientist | Department of Mechanical Engineering | IIT Kharagpur |


<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>