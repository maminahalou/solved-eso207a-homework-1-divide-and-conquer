Download Link: https://assignmentchef.com/product/solved-eso207a-homework-1-divide-and-conquer
<br>
<table width="573">

 <tbody>

  <tr>

   <td width="249">             <strong>ESO207A:                    Data</strong></td>

   <td width="91"><strong>Structures</strong></td>

   <td width="233">        <strong>and                   Algorithms</strong></td>

  </tr>

  <tr>

   <td width="249">Homework <em>1: Divide and Conquer</em></td>

   <td width="91"> </td>

   <td width="233"> </td>

  </tr>

 </tbody>

</table>

<strong>Instructions.</strong>

<ol>

 <li>Solutions have to be submitted on Gradescope. For this, each problem should start on a newsheet. If this is not followed then it may not be possible to grade your answers.</li>

 <li>For each problem, write your name, Roll No., problem number, the date and the names ofany students with whom you collaborated. Remember that you must write the answer and the algorithm in your own words.</li>

 <li>For questions in which algorithms are asked for, your answer should provide the following: (a) A clear description of the algorithm in English and/or pseudo-code, where, helpful, (b) A proof/argument of the correctness of the algorithm, and, (c) an analysis of the running time of the algorithm.</li>

</ol>

<em>Full marks will be given only to correct solutions which are described clearly</em>. Convoluted and unclear descriptions will receive <em>low marks</em>.

<h1>Problem 1. Order Notation and Recurrence Equations                                                                                          (30)</h1>

<ul>

 <li>State whether each of the following statement is true or false, with a brief reason. (i) <em>n</em><sup>2 </sup>= <em>O</em>(2<em><sup>n</sup></em>), (ii) <em>n</em><sup>3 </sup>= <em>O</em>(<em>n</em><sup>4 </sup>log<em>n</em>), (iii) <em>n</em><sup>2 </sup>= Ω(<em>n</em><sup>3</sup>), (iv) 3<em><sup>n </sup></em>= Θ(<em>n</em>!) (v) 2<em><sup>n </sup></em>= Θ(2<em><sup>n</sup></em><sup>+<em>c</em></sup>), for any constant <em>c</em>. (10)</li>

 <li>Solve the following recurrence equations. Assume that <em>T</em>(1) = Θ(1) and <em>T</em>(2) = Θ(1) for all the functions below. Use the recursion tree method (unrolling the recurrence eqn as done in class). Do not use the master formula. Make and state appropriate simplifying assumptions if needed. (4 × 5 = 20).

  <ol>

   <li><em>T</em>(<em>n</em>) = <em>T</em>(<em>n/</em>2) + <em>n</em>.</li>

   <li><em>T</em>(<em>n</em>) = 4<em>T</em>(<em>n/</em>3) + <em>n</em><sup>2</sup>.</li>

   <li><em>T</em>(<em>n</em>) = 3<em>T</em>(<em>n/</em>3) + <em>n</em>.</li>

   <li><em>T</em>(<em>n</em>) = 2<em>T</em>(<em>n/</em>2) + <em>n</em>log<em>n</em>.</li>

  </ol></li>

</ul>

<h1>Problem 2. Non-dominated points                                                                                                                                           (35)</h1>

A two-dimensional point (<em>x,y</em>) is said to dominate another two-dimensional point (<em>u,v</em>) if <em>x </em>≥ <em>u </em>and <em>y </em>≥ <em>v</em>. Non-dominated points are also called maximal points. Given a set <em>P </em>of points, a point <em>p </em>= (<em>x,y</em>) is said to be a non-dominated point of <em>P </em>if no other point <em>q </em>in <em>P </em>dominates <em>p</em>. See Figure 1 for examples. Given a set of <em>n </em>points <em>P </em>placed in arbitrary order in an array, give a time efficient algorithm find non dom(<em>P,n</em>) to find the set of all non-dominated points in <em>P</em>. <em>Notes</em>:

<ol>

 <li>For simplicity, assume that no two points have the same <em>x</em>-coordinate or the same <em>y</em>-coordinate.</li>

 <li>A <em>point p </em>is represented as a structure with two attributes <em>x </em>and <em>p.y</em>. The set of points <em>P</em>, is represented as an array <em>P</em>[1<em>,…,n</em>] of <em>point</em>s in arbitrary order.</li>

 <li>You can find the index of the median of the points in <em>P</em>[<em>k,…,l</em>] by the <em>x </em>coordinate by using an informal statement like “let <em>i </em>= median(<em>P,k,l</em>) by <em>x</em>-coordinate” Similarly, a statement like “let <em>i </em>=median(<em>P,k,l</em>) by <em>y </em>coordinate” can be used to find the index of the median of the points in <em>P</em>[<em>k,…,l</em>] by the <em>y </em> These functions run in time <em>O</em>(<em>l </em>− <em>k </em>+ 1). The median of <em>n </em>points is returned as the b(<em>n </em>+ 1)<em>/</em>2c th ranked point (by <em>x</em>-coordinate or <em>y</em>-coordinate as the case may be).</li>

 <li>Full marks will be provided for a correct solution that takes <em>O</em>(<em>n</em>log<em>n</em>) time.</li>

 <li>A correct solution of <em>O</em>(<em>n</em><sup>2</sup>) time will earn only 15 points in total.</li>

</ol>

Figure 1: Dominated and non-dominated points in a point-set

<h1>Problem 3.                                                                                                                                                                                                     (35)</h1>

An important court trial is going on that has <em>N </em>witnesses. However, not all witnesses are honest; a witness is either <em>true </em>or <em>false</em>. A <em>true </em>witness always speaks the truth, whereas a <em>false </em>witness may lie and cannot be relied upon. To test the witnesses’ credibility, the judge speaks to them in pairs (e.g., <em>W</em>1 and <em>W</em>2). Both are asked the same questions about the case and the answers given by each one is presented to the other. Each of them (e.g., <em>Wi</em>) is now asked whether the other person (i.e. <em>W</em>2) is telling the truth or not (and vice-versa). The possibilities are as follows:

<table width="462">

 <tbody>

  <tr>

   <td width="94">W1 says</td>

   <td width="98">W2 says</td>

   <td width="271">Conclusion</td>

  </tr>

  <tr>

   <td width="94">W2 is true</td>

   <td width="98">W1 is true</td>

   <td width="271">Both are true, or both are false witnesses</td>

  </tr>

  <tr>

   <td width="94">W2 is true</td>

   <td width="98">W1 is false</td>

   <td width="271">At least one is a false witness</td>

  </tr>

  <tr>

   <td width="94">W2 is false</td>

   <td width="98">W1 is true</td>

   <td width="271">At least one is a false witness</td>

  </tr>

  <tr>

   <td width="94">W2 is false</td>

   <td width="98">W1 is a false</td>

   <td width="271">At least one is a false witness</td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Show that if there are more than <em>N/</em>2 false witnesses, the judge cannot necessarily pick out the true witnesses, irrespective of the pairwise test strategy used. Assume that the false witnesses can conspire to fool the judge.</li>

 <li>Assuming that more than <em>N/</em>2 witnesses are true, the judge now wants to identify one true witness. Show that b<em>N/</em>2c pairwise tests are sufficient to reduce this problem to that of approximately half its size.</li>

 <li>Show that the true witnesses can be identified with Θ(<em>N</em>) pairwise tests, assuming that more than <em>N/</em>2 witnesses are true. Argue and solve the recurrence that describes the number of tests.</li>

</ol>