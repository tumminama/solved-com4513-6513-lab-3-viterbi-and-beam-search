Download Link: https://assignmentchef.com/product/solved-com4513-6513-lab-3-viterbi-and-beam-search
<br>
The goal of this lab session is to accelerate the structured perceptron using two methods, Viterbi and Beam search. You should use the same data as in Lab 3.

<ul>

 <li> Implement the Viterbi algorithm to accelerate the argmax operation during both training and testing. Recall that the Viterbi is an exact search algorithm, i.e. it should return exactly the same result as the naive implementation, only faster. To ensure this happens, pay attention to random seeds, use of (ordered) dictionaries, etc. Here is an adaptation of Viterbi for the structured perceptron: : word sequence <strong>x </strong>= [<em>x</em><sub>1</sub><em>,…,x<sub>N</sub></em>], weights <strong>w </strong>set matrix <em>V <sup>|Y|×N </sup></em>= 0 set backpointer</li>

</ul>

<em>B</em><em>|Y|×N </em>= 0

<em>V </em>[<em>y,n</em>] = max<em>V </em>[<em>y<sup>0</sup>,n − </em>1] + <strong>w </strong><em>· φ</em>(<em>y,y<sup>0</sup>,</em><strong>x</strong>)

<em>y<sup>0</sup>∈Y</em>

<em>B</em>[<em>y,n</em>] = <em>argmax<sub>y</sub></em><em>0<sub>∈Y</sub>V </em>[<em><sup>y0</sup>,n − </em>1] + <strong>w </strong><em>· φ</em>(<em><sup>y,y0</sup>,</em><strong>x</strong>)

<ul>

 <li> What speed up do you get with Viterbi compared to the standard structured perceptron?</li>

 <li> Implement beam search to accelerate the argmax. Recall that it is an inexact search method so the results might differ. But given a large enough beam size it should achieve the same results as viterbi and the structured perceptron from Lab 3.</li>

 <li> Does beam search affect your accuracy? What is the effect of beam size on speed and accuracy compared to the standard structured perceptron and Viterbi? <strong>Tip 1: </strong>Try three different beam sizes and report the results. <strong>Tip 2: </strong>Use a table to summarise the results (accuracy and training time) for the standard perceptron (from the lab 3), Viterbi and Beam search.</li>

</ul>