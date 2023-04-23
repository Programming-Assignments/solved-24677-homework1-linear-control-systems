Download Link: https://assignmentchef.com/product/solved-24677-homework1-linear-control-systems
<br>
<h1><strong>Exercise 1. </strong>Types of Systems</h1>

A system has an input <em>u</em>(<em>t</em>) and an output <em>y</em>(<em>t</em>)<em>, </em>which are related by the information provided below. Classify each system as linear or non-linear and time invariant or time-varying, and explain why.

<ol>

 <li><em>y</em>(<em>t</em>) = 0 for all <em>t </em><strong>(4 points)</strong></li>

 <li><em>y</em>(<em>t</em>) = <em>u</em><sup>3</sup>(<em>t</em>) <strong>(4 points)</strong></li>

 <li><em>y</em>(<em>t</em>) = <em>u</em>(3<em>t</em>) <strong>(4 points)</strong></li>

 <li><em>y</em>(<em>t</em>) = <em>e</em><sup>−<em>t</em></sup><em>u</em>(<em>t </em>− <em>T</em>) <strong>(4 points)</strong></li>

 <li><strong>(4 points)</strong></li>

</ol>

<h1><strong>Exercise 2. </strong>State space representations</h1>

A company deployed 3 teams of drones in a region. Each team consists of a pair of drones. One drone in the team carries a transmitter and the other one carries a receiver. Transmitter <em>i </em>transmits at power level <em>p<sub>i </sub></em>(<em>p<sub>i </sub>&gt; </em>0). The path gain from transmitter <em>j </em>to receiver <em>i </em>is <em>G<sub>ij </sub></em>(<em>G<sub>ij </sub></em>&gt; 0 for <em>j </em>6= <em>i</em>, and <em>G<sub>ii </sub>&gt; </em>0). The signal power at receiver <em>i </em>is given by <em>s<sub>i </sub></em>= <em>G<sub>ii</sub>p<sub>i</sub></em>. The noise plus interference power (caused by other transmitters <em>j </em>6= <em>i</em>) at receiver <em>i </em>is given by

<em>q</em><em>i </em>= <em>σ</em>2 + X<em>G</em><em>ijp</em><em>j,</em>

<em>j</em>6=<em>i</em>

where <em>σ</em><sup>2 </sup><em>&gt; </em>0 is the self-noise power of the receivers.

Figure 1: The wireless network

The signal to interference plus noise ratio (SINR) at receiver <em>i </em>is defined as <em>S<sub>i </sub></em>= <em>s<sub>i</sub>/q<sub>i</sub></em>. For signal reception to occur, the SINR must exceed some threshold value <em>γ </em>(<em>i.e.</em>, <em>S<sub>i </sub></em>≥ <em>γ</em>). We assume <em>p</em>, <em>q </em>and <em>S </em>are discrete-time signals. For example, <em>p<sub>i</sub></em>(<em>k</em>) represents the transmit power of transmitter <em>i </em>at time <em>k </em>(<em>k </em>= 0<em>,</em>1<em>,</em>2<em>,…</em>). We want to have a certain SINR, e.g.

<em>S<sub>i</sub></em>(<em>k</em>) = <em>s<sub>i</sub></em>(<em>k</em>)<em>/q<sub>i</sub></em>(<em>k</em>) = <em>αγ,</em>

where <em>α &gt; </em>1 is an SINR safety margin. To achieve this goal, someone designed the following control rule <em>p<sub>i</sub></em>(<em>k </em>+ 1) = <em>p<sub>i</sub></em>(<em>k</em>)(<em>αγ/S<sub>i</sub></em>(<em>k</em>))<em>.</em>

<ol>

 <li>Show that the power control update algorithm can be expressed as a linear dynamical system with constant input, <em>e.</em>, in the form</li>

</ol>

<em>p</em>(<em>k </em>+ 1) = <em>Ap</em>(<em>k</em>) + <em>Bσ</em><sup>2</sup><em>,</em>

where <em>A </em>∈R<sup>3×3 </sup>and <em>B </em>∈R<sup>3×1 </sup>are constant and <em>p</em>(<em>k</em>) = [<em>p</em><sub>1</sub><em>,p</em><sub>2</sub><em>,p</em><sub>3</sub>]<em><sup>T</sup></em>. Describe <em>A </em>and <em>b</em>

explicitly in terms of <em>σ,γ,α </em>and the components of <em>G</em>.

<ol start="2">

 <li>Use Python to simulate the power control algorithm. Use the problem data</li>

</ol>

Experiment with two different initial conditions: <em>p</em><sub>1 </sub>= <em>p</em><sub>2 </sub>= <em>p</em><sub>3 </sub>= 0<em>.</em>1 and <em>p</em><sub>1 </sub>= 0<em>.</em>1<em>,p</em><sub>2 </sub>= 0<em>.</em>01<em>,p</em><sub>3 </sub>= 0<em>.</em>02. Plot <em>S<sub>i </sub></em>and <em>p </em>as a function of <em>t, </em>and compare it to the target value <em>αγ</em>. Repeat for <em>γ </em>= 5. Can the controller achieve the goal to make <em>S<sub>i</sub></em>(<em>t</em>) → <em>αγ</em>? Plot

all the <em>p<sub>i</sub></em>(<em>k</em>) as well.

<h1><strong>Exercise 3. </strong>Linearization</h1>

Perform linearization on the given differential equation

<em>y</em>¨+ (1 + <em>y</em>)<em>y</em>˙ − 2<em>y </em>+ 0<em>.</em>5<em>y</em><sup>3 </sup>= 0

<strong>Exercise 4. </strong><em>Equilibrium </em><em>(10 points)</em>

The simplified dynamics of the vertical ascent of a Space X rocket can be modeled as

where <em>D </em>is the distance from earth to the surface of the rocket, <em>m </em>is the actual mass of the rocket, <em>g </em>is the gravity constant, and <em>u </em>is the thrust. During a short period of time, we can assume <em>D</em>, <em>m</em>, <em>g</em>, <em>u </em>are all constant. <em>ln</em>(∗) is the natural logarithmic,

Find the equilibrium states () of the above dynamic system. Perform linearization on the system.

<h1><strong>Exercise 5. </strong>Linearization</h1>

Model the earth and a satellite as particles. The normalized equations of motion, in an earth-fixed inertial frame, simplified to 2 dimensions (from Lagrange’s equations of motion, the Lagrangian , where <em>r </em>is the radius of the trajectory of the satellite, <em>θ </em>is the angle, <em>k </em>is the Newtonian constant:

with <em>u</em>1, <em>u</em>2 are control input, representing the radial and tangential forces due to the thrusters. The reference orbit with <em>u</em>1 = <em>u</em>2 = 0 is circular with <em>r</em>(<em>t</em>) ≡ <em>p </em>and <em>θ</em>(<em>t</em>) = <em>ωt</em>, where <em>p </em>is a representing the constant cruise radius, <em>ω </em>is the constant angular velocity of the satellite.

<ol>

 <li>What’s the value of <em>k </em>expressed in terms of <em>p </em>and <em>w</em>, when the satellite is on the reference orbit? <strong>(10 points)</strong></li>

</ol>

Obtain the linearized equation about this orbit. (Hint: we linearize on a trajectory, not a equilibrium point, so ˙<em>x </em>6= 0) <strong>(15 points</strong>