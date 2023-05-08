Download Link: https://assignmentchef.com/product/solved-tdt4171-assignment-2-probabilistic-reasoning-over-time
<br>
<h1>Hidden Markov Model</h1>

Some tourists are curious if there are fish in a nearby lake. They are unable to observe whether this is true or not by staring into the lake. However, they can observe whether or not there are birds nearby that affect the presence of fish. Based on their instincts, the tourists propose the following domain theory:

<ol>

 <li>The prior probability of fish nearby (that is, without any observation) is 0<em>.</em></li>

 <li>The probability of fish nearby on day <em>t </em>is 0<em>.</em>8 given there are fish nearby on day <em>t </em>− 1, and 0<em>.</em>3 if not.</li>

 <li>The probability of birds nearby on day <em>t </em>if there are fish nearby on the same day is 0<em>.</em>75, and</li>

</ol>

0<em>.</em>2 if not.

The following evidence is given

<table width="443">

 <tbody>

  <tr>

   <td width="244">•   <strong>e</strong><sub>1 </sub>= {birds nearby}•   <strong>e</strong><sub>2 </sub>= {birds nearby}•   <strong>e</strong><sub>3 </sub>= {no birds nearby}</td>

   <td width="199">•   <strong>e</strong><sub>4 </sub>= {birds nearby}•   <strong>e</strong><sub>5 </sub>= {no birds nearby}•   <strong>e</strong><sub>6 </sub>= {birds nearby}</td>

  </tr>

 </tbody>

</table>

We will denote the state variable for fish nearby on day <em>t </em>by <em>X<sub>t</sub></em>.

<h2>Instructions</h2>

Use programming to solve all exercises in this section involving computation. The results need to be extracted from the program and well documented in a human-readable format that is easy to understand in a PDF file. Additionally, write a few sentences to give the results some context. The results can, for example, be plotted using Matplotlib [1] to give a more straightforward overview.

The code must be runnable without any modifications after delivery. Moreover, the code must be readable and contain comments explaining it. We recommend that Python with the package NumPy [2] be used for the programming exercises. It is not allowed to use libraries, such as Scikit-learn [3] to solve the tasks.

<h2>Problems</h2>

<ul>

 <li>Formulate the information given above as a hidden Markov model, and provide the complete probability tables for the model.</li>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:<em>t</em></sub>)<em>, </em>for <em>t </em>= 1<em>,…,</em>6<em>.                                                     </em>(1)

What kind of operation is this (filtering, prediction, smoothing, likelihood of the evidence, or most likely sequence)? Describe in words what kind of information this operation provides us.

<ul>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:6</sub>)<em>, </em>for <em>t </em>= 7<em>,…,</em>30<em>.                                                    </em>(2)

What kind of operation is this (filtering, prediction, smoothing, likelihood of the evidence, or most likely sequence)? Describe in words what kind of information this operation provides us. What happens to the distribution in Equation (2) as <em>t </em>increases?

<ul>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:6</sub>)<em>, </em>for <em>t </em>= 0<em>,…,</em>5<em>.                                                     </em>(3)

What kind of operation is this (filtering, prediction, smoothing, likelihood of the evidence, or most likely sequence)? Describe in words what kind of information this operation provides us.

<ul>

 <li>Compute</li>

</ul>

argmax <strong>P</strong>(<em>x</em><sub>1</sub><em>,…,x<sub>t</sub></em><sub>−1</sub><em>,X<sub>t</sub></em>|<strong>e</strong><sub>1:<em>t</em></sub>)<em>, </em>for <em>t </em>= 1<em>,…,</em>6<em>.                                       </em>(4)

<em>x</em><sub>1</sub><em>,…,x<sub>t</sub></em>−<sub>1</sub>

What kind of operation is this (filtering, prediction, smoothing, likelihood of the evidence, or most likely sequence)? Describe in words what kind of information this operation provides us.

<h1>2        Dynamic Bayesian Network</h1>

Some tourists visiting a cabin are interested in finding out if there are animals nearby. They can observe outside of their window every day whether there are animal tracks and whether the food they placed outside is gone. Furthermore, they believe that the animal tracks and the food placed outside are conditionally independent given animals nearby (<em>AnimalTracks<sub>t </sub></em>⊥⊥ <em>FoodGone<sub>t </sub></em>| <em>AnimalsNearby<sub>t</sub></em>). Based on gut feelings, the tourists provide the following domain theory:

<ol>

 <li>The prior probability of animals nearby (that is, without any observation) is 0<em>.</em></li>

 <li>The probability of animals nearby on day <em>t </em>is 0<em>.</em>8 given that there were animals nearby on day <em>t </em>− 1, and 0<em>.</em>3 if not.</li>

 <li>The probability of animal tracks on day <em>t </em>if there are animals nearby on the same day is 0<em>.</em>7, and 0<em>.</em>2 if not.</li>

 <li>The probability of the food gone on day <em>t </em>if there are animals nearby on the same day is 0<em>.</em>3, and 0<em>.</em>1 if not.</li>

</ol>

The following evidence is given

<table width="535">

 <tbody>

  <tr>

   <td width="252">•   <strong>e</strong><sub>1 </sub>= {animal tracks<em>,</em>food gone}•   <strong>e</strong><sub>2 </sub>= {no animal tracks<em>,</em>food gone}</td>

   <td width="283">•   <strong>e</strong><sub>3 </sub>= {no animal tracks<em>,</em>food not gone}•   <strong>e</strong><sub>4 </sub>= {animal tracks<em>,</em>food not gone}</td>

  </tr>

 </tbody>

</table>

We will denote the state variable for animals nearby on day <em>t </em>by <em>X<sub>t</sub></em>.

<h2>Instructions</h2>

Solve by hand all exercises in this section involving computation, not by programming. The results must be accompanied by steps to solve them and justifications, not only the final results.

<h2>Problems</h2>

<ul>

 <li>Formulate the information given above as a dynamic Bayesian network and provide the complete probability tables for the model.</li>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:<em>t</em></sub>)<em>, </em>for <em>t </em>= 1<em>,</em>2<em>,</em>3<em>,</em>4<em>.                                                    </em>(5)

<ul>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:4</sub>)<em>, </em>for <em>t </em>= 5<em>,</em>6<em>,</em>7<em>,</em>8<em>.                                                   </em>(6)

<ul>

 <li>By forecasting further and further into the future, you should see that the probability converges towards a fixed point. Verify that</li>

</ul>

lim <strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:4</sub>) = h0<em>.</em>6<em>,</em>0<em>.</em>4i<em>.                                                   </em>(7)

<em>t</em>→∞

<ul>

 <li>Compute</li>

</ul>

<strong>P</strong>(<em>X<sub>t</sub></em>|<strong>e</strong><sub>1:4</sub>)<em>, </em>for <em>t </em>= 0<em>,</em>1<em>,</em>2<em>,</em>3<em>.                                                   </em>(8)