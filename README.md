Download Link: https://assignmentchef.com/product/solved-cs2211a-lab-no-5
<br>
<strong>Introduction to C </strong>

The objective of this lab is:

<ul>

 <li>To practice the C compilation process</li>

 <li>To practice C formatted input/output, as well as C expressions and selection statements If you would like to leave, and at least 30 minutes have passed, raise your hand and wait for the TA.</li>

</ul>

Show the TA what you did. If, and only if, you did a reasonable effort during the lab, he/she will give you the lab mark.

<h2>====================================================================================</h2>

<ol>

 <li>Type in (using an editor) and then compile (using <strong>gcc</strong>) the following c program. If you do not have any compilation errors, the compiler will generate an executable program called a.out. To execute this program, simply type a.out and hit enter.</li>

</ol>

#include &lt;stdio.h&gt; int main(void)

{ printf((“Hello world
”);

}

<ol start="2">

 <li>If you want to name the generated executable file with something other than out, you should use <strong>gcc</strong> with <strong>-o</strong> option, e.g., gcc –o hello hello.c (in this case, you should type hello to execute the program)</li>

 <li>By default, <strong>gcc</strong> compiles programs using <strong>C89</strong>. To compile using <strong>C99</strong>, you should use “<strong>gcc -std=c99</strong>”.</li>

</ol>

Recompile hello.c program using <strong>C99</strong> instead of <strong>C89</strong>. Do you get a warning message from the compiler?  If so, what needs to be done to make it go away?

<ol start="4">

 <li>It is a good practice to use “<strong>gcc -Wall</strong>” to check all warnings in your program.</li>

</ol>

Try again to compile the <em>original</em> hello.c program with “<strong>gcc -Wall</strong>” using <strong>C89</strong> and <strong>C99</strong>.

<ol start="5">

 <li>You can force <strong>gcc</strong> to stop after the preprocessing stage by using <strong>-E</strong></li>

</ol>

Type in the following simple.c program. Execute the following two commands:  gcc –E simple.c  gcc –E –std=c99 simple.c

What is the difference between the two outputs?

#define MIN 0 #define MAX 100 int main(void) { int i, j, m, n;   i = MAX;

/* First command line

*/   j = MIN;

// Second command line   m = i + j;   n = MAX + MIN;   return 0;

}




<ol start="6">

 <li>Write a program that declares several int and float variables (without initializing them) and then prints their values. Is there any pattern in the values?</li>

 <li>What will happen when you attempt to print an arithmetic expression using the <em>wrong</em> conversion specifier, i.e., printing int expression using %f or float expression using %d?</li>

 <li>Mentally evaluate the following printf function calls and write your answer on a piece of paper. Write a program that prints the values of the output.  Verify your answers with the program answers

  <ul>

   <li>printf(“*%20.10d*
*%-20.10d*
*%.10d*
*%-20d*
”,</li>

  </ul></li>

</ol>

123456,123456,-123456,-123456);




<ul>

 <li>printf(“%.4f
”, 83.162);</li>

</ul>




<ul>

 <li>printf(“%12.5e
”, 30.253);</li>

</ul>




<ul>

 <li>printf(“%-6.2g
”, .0000009979);</li>

</ul>

<ol start="9">

 <li>Mentally evaluate the following expressions and write the answer on a piece of paper.</li>

</ol>

Write a program that prints the value of these expressions.  Verify your answers with the program answers.

<ul>

 <li>13 % 4, -13 % 4, 13 % -4, and -13 % -4</li>

 <li>13 / 4, -13 / 4, 13 / -4, and -13 / -4</li>

</ul>

<ol start="10">

 <li>Show the output produced by the following program fragment. int i = 1, j = 2; int k = 3, m = 4; i %= j++ % (k += –m);</li>

</ol>

printf(“%d %d %d %d
”, i++, ++j, k–, –m);

<ol start="11">

 <li>Show the output produced by the following program fragment. int i = 1, j = 2; int k = 3, m = 4; i *= j / – (k -= ++m);</li>

</ol>

printf(“%d %d %d %d
”, i++, ++j, k–, –m);

<ol start="12">

 <li>De Morgan’s laws state that the expression !(condition1 &amp;&amp; condition2) is logically equivalent to  the expression (!condition1 || !condition2).</li>

</ol>

In addition,

the expression !(condition1 || condition2) is logically equivalent to  the expression (!condition1 &amp;&amp; !condition2).

Use De Morgan’s laws to write equivalent expressions for each of the following, and then write a program to show that both the original expression and the new expression in each case are equivalent.

(a)  !(x &lt;  5) &amp;&amp; !(y &gt;= 7) (b)  !(a == b) || !(g != 5)

<ul>

 <li>!((x &lt;= 8) &amp;&amp; (y &gt;  4))</li>

 <li>!((i &gt; 4) ||  (j &lt;= 6))</li>

</ul>

<ol start="13">

 <li>Write a program to implement the following flowchart <em>segment</em>. The program should get the value of pH from the user. Test your program to make sure that it produces correct answers.</li>

 <li>Rewrite the following program fragment by replacing the switch statement with</li>

</ol>

(a) Nested  if .. else  statement (b) A series of if statements without else

Be careful to deal with the default case properly.




#include &lt;stdio.h&gt;




int main(void)

{ int i;

for(i=1; i&lt;=8; i++)

{    switch(i)     {       case 1:       case 2:  printf(“%d ==&gt; a
”, i);                break;

case 3: case 4:       case 5:  printf(“%d ==&gt; b
”, i);                break;




case 6:  printf(“%d ==&gt; c
”, i);                break;




default: printf(“%d ==&gt; d
”, i);

}   }   return 0;

}