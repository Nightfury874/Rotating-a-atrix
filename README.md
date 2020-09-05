# Rotating-a-matrix
Write a program to rotate a matrix in 90 degree angle.
DSA Lab Assignment for 05/09/2020</br>
<br> We were supposed to allocate the array or matrix using malloc functions.</br>
<br> We must ensure that your solution defends any test-cases. For instance, 1x1
matrix.</br>
<br>Input should be given by random function and the code snippet of a single
dimensional array is given below-</br>
#include&lt;stdlib.h&gt;
#include&lt;time.h&gt;
srand(time(0));
for(i=0;i&lt;n;i++)
a[i]=(rand()%(upper_limit-lower_limit +1))+lower_limit;
