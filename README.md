# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

For picking the first element for a randomized array, the odds of choosing a good pivot (an element that would be in the middle half when sorted) are $1/2$ because it will must be part of the middle $n/2$ elements. If we were to pick the median of the first,middle, and last elements, we know it would atleast have one element on either side of it in the sorted array. Thus the probability of the median element being a good pivot is 

$$
\begin{align}
P(\text{good pivot| median of three random elements}) &= 1 - P(\text{not a good pivot| median of three random elements})\\ 
&= 1 - \frac{(n - 3)}{2 \dot n}
\end{align}
$$
This is greater than
$$
\begin{align}
P(\text{good pivot| first element in the array}) &= 1 - P(\text{not a good pivot| first element in the array})\\ 
&= 1 - \frac{(n)}{2 \dot n}\\
&= \frac{1}{2}
\end{align}
$$

Hence for any $n > 3$, picking the median value of the first, middle, and last elements of an array increases your odds of picking a good pivot compared to arbitrarily picking the first element of the array.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.
