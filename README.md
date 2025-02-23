# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$


Solving:

$T(n) = T(n/13) + 5$

 $= (T((n/13)/13) + 5) + 5$
    
 $= T(n/13^2 ) + 10$
    
 $= T(n/13^3 ) + 15$
    
 ...
 
 $= T(n/13^i) + 5i$

for $i = \log{_13}{n}$

 $= T(1) + 5\log{_13}{n} = 1 + 5\log{_13}{n} ∈ Θ(5\log{n})$

$T(n) ∈ Θ(5\log{n})$

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

Solving:

$T(n) = 13T(n/13) + 5$

 $= 13(13T((n/13)/13) + 5) + 5$
    
 $= 13^ 2T(n/13^2 ) + 10$
    
 $= 13^3 T(n/13^3 ) + 15$
    
 ...
 
 $= 13^i T(n/13^i) + 5i$

for $i = log_13 n$

 $= nT(1) + 5log_13 n = n + 5log_13 n ∈ Θ(n)$

$T(n) ∈ Θ(n)$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

Solving:

$T(n) = 13T(n/13) + 2n$

 $= 13(13T((n/13)/13) + 2n) + 2n$
    
 $= 13^ 2T(n/13^2 ) + 4n$
    
 $= 13^3 T(n/13^3 ) + 6n$
    
 ...
 
 $= 13^i T(n/13^i) + 2in$

for $i = log_13 n$

 $= nT(1) + 2nlog_13 n = n + 2nlog_13 n ∈ Θ(2nlog n)$

$T(n) ∈ Θ(2nlog n)$


### Sources:

I used the example provided in the mergesort slides as well as referencing my own work for the Divide and Conquer Sum assignment.

“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.” - Natalie Sleight
