Homework process and study group
================================

I worked with Kevyn Cheng (SID: 25720910), Austin Leung (SID: 25225613)
and Chen Ruichao (SID: 25006046). Like lastweek, we got together in my
living room to work individually and discuss difficult problems/check
answers when we had them.

Powers of a Nilpotent Matrix (OPTIONAL)
=======================================

SKIP

Elementary Matrices
===================

(a) Row operations on a 4x5 Augmented Matrix:

    -   Switching Rows 2 and 4:\
        $\begin{pmatrix}
              0 & 1 & 0 & 0 \\
              1 & 0 & 0 & 0 \\
              0 & 0 & 1 & 0 \\
              0 & 0 & 0 & 1
            \end{pmatrix}$

    -   Multiplying row 3 by -4:\
        $\begin{pmatrix}
              1 & 0 & 0 & 0 \\
              0 & 1 & 0 & 0 \\
              0 & 0 & -4 & 0 \\
              0 & 0 & 0 & 1
            \end{pmatrix}$

    -   Adding 2× row 2 to row 4 and subtracting row 2 from row 1:\
        $\begin{pmatrix}
              1 & -1 & 0 & 0 \\
              0 & 1 & 0 & 0 \\
              0 & 0 & 1 & 0 \\
              0 & 2 & 0 & 1
            \end{pmatrix}$

(b) Row Reducing Elementary Matrix:\
    Row reducing A:\
    $\begin{pmatrix}
          1 & -2 & 0 & -5 \\
          0 & 1 & 0 & 3 \\
          -2 & -2 & 1 & -6 \\
          0 & 1 & 0 & 2
        \end{pmatrix}\xrightarrow{r3+2r1} 
        \begin{pmatrix}
          1 & -2 & 0 & -5 \\
          0 & 1 & 0 & 3 \\
          0 & -7 & 1 & -16 \\
          0 & 1 & 0 & 2
        \end{pmatrix}\xrightarrow{r3+7r4}
        \begin{pmatrix}
          1 & -2 & 0 & -5 \\
          0 & 1 & 0 & 3 \\
          0 & 0 & 1 & -2 \\
          0 & 1 & 0 & 2
        \end{pmatrix}\xrightarrow{r4-r2}$

    $\begin{pmatrix}
          1 & -2 & 0 & -5 \\
          0 & 1 & 0 & 3 \\
          0 & 0 & 1 & -2 \\
          0 & 0 & 0 & -1
        \end{pmatrix}\xrightarrow{-r4}
        \begin{pmatrix}
          1 & -2 & 0 & -5 \\
          0 & 1 & 0 & 3 \\
          0 & 0 & 1 & -2 \\
          0 & 0 & 0 & 1
        \end{pmatrix}\xrightarrow{r3+2r4}
        \begin{pmatrix}
          1 & -2 & 0 & -5 \\
          0 & 1 & 0 & 3 \\
          0 & 0 & 1 & 0 \\
          0 & 0 & 0 & 1
        \end{pmatrix}\xrightarrow{r2-3r4}$

    $\begin{pmatrix}
          1 & -2 & 0 & -5 \\
          0 & 1 & 0 & 0 \\
          0 & 0 & 1 & 0 \\
          0 & 0 & 0 & 1
        \end{pmatrix}\xrightarrow{r1+5r4}
        \begin{pmatrix}
          1 & -2 & 0 & 0 \\
          0 & 1 & 0 & 0 \\
          0 & 0 & 1 & 0 \\
          0 & 0 & 0 & 1
        \end{pmatrix}\xrightarrow{r1+2r2}
        \begin{pmatrix}
          1 & 0 & 0 & 0 \\
          0 & 1 & 0 & 0 \\
          0 & 0 & 1 & 0 \\
          0 & 0 & 0 & 1
        \end{pmatrix}$\
    Repeating the same row operations simultaneously on the 4x4 Identity
    Matrix yields the following transformation matrix. Left multiplying
    A by this new matrix E:\
    $\begin{pmatrix}
          1 & 1 & 0 & 1 \\
          0 & -2 & 0 & 3 \\
          2 & 2 & 1 & 5 \\
          0 & 1 & 0 & -1
        \end{pmatrix}
        \begin{pmatrix}
          1 & -2 & 0 & -5 & :16 \\
          0 & 1 & 0 & 3 & :-7\\
          -2 & -2 & 1 & -6 & :9\\
          0 & 1 & 0 & 2 & :-5
        \end{pmatrix}$ = $ \begin{pmatrix}
          1 & 0 & 0 & 0 & :4 \\
          0 & 1 & 0 & 0 & :-1\\
          0 & 0 & 1 & 0 & :2\\
          0 & 0 & 0 & 1 & :-2
        \end{pmatrix}$

Pump Properties Proofs
======================

(a) The first reversed transition matrix will not return any arbitrary
    state transformed by the given pump transition matrix:\
    $$\begin{pmatrix}
          0 & 0 & 0 \\
          b & a & 0 \\
          c & 0 & 0 
        \end{pmatrix}$$\
    back to it’s initial state. For example, the state vector
    $\begin{pmatrix}
          1  \\
          0  \\
          50 
        \end{pmatrix}$ transformed by the above simply yields
    $\begin{pmatrix}
          0  \\
          b  \\
          c 
        \end{pmatrix}$. When this intermediate is acted on by the
    reversed transition matrix:\
    $$\begin{pmatrix}
          0 & b & c \\
          0 & a & 0 \\
          0 & 0 & 0 
        \end{pmatrix}$$\
    yields the following state vector $\begin{pmatrix}
          \text{b}^2+\text{c}^2  \\
          ba  \\
          0 
        \end{pmatrix}$. that is unequivalent to our starting state.

(b) The second reversed transition matrix utilizes normalization of
    constants to try to account for water loss in the systemm, but it
    still is unable to return the transformed vector back to
    the original. The new reverse matrix:\
    $$\begin{pmatrix}
          0 & a' & c' \\
          0 & b' & 0 \\
          0 & 0 & 0 
        \end{pmatrix}
        a'+b' = 1; c' = 1$$\
    is even easier to disproove, because c’ = 1. So if the same
    transformed state $\begin{pmatrix}
          0  \\
          b  \\
          c 
        \end{pmatrix}$ , acted on by the new reverse transform matrix,
    becomes: $\begin{pmatrix}
          ba' +cc'  \\
          bb'  \\
          0 
        \end{pmatrix}$. This is unequivalent to our starting state.
    Comparing row 3 of the new and original state vectors, 0 $\neq$ 50.

(c) If each column sums to one, the the total amount of water in the
    system is unchanging, as all of the water from each of the pools is
    completely defined in the next time step. No water can be
    “unaccounted for.”

(d) The illustration below translates to the following transition
    matrix:\
    $$\begin{pmatrix}
          0 & 0 & 0 \\
          0.5 & 0.4 & 0.2 \\
          0 & 0.6 & 0.65 
        \end{pmatrix}$$\
    Because the amount of water leaving reservoirs 1 and 3 doesn’t sum
    to 1 (columns), there is technically leakage in the system. Water
    unaccounted for (without the self-loops) simply disappears in the
    next time step. And so 1 and 3 will soon go to zero.

(e) The product of matrix A and vector x is a linear combination of the
    rows of x, with the coefficients being the columns of (a
    particular row) of A. In a 3x3 example:\
    $$\begin{pmatrix}
          a_{11}x + a_{12}x + a_{13}x\\
          a_{21}x + a_{22}x + a_{23}x \\
          a_{31}x + a_{32}x + a_{33}x 
        \end{pmatrix}$$\
    But since the rows of A sum to one,\
    $$\begin{pmatrix}
          x(a_{11} + a_{12} + a_{13})\\
          x(a_{21} + a_{22} + a_{23}) \\
          x(a_{31} + a_{32} + a_{33}) 
        \end{pmatrix}$$\
    each row is just equal to x \* 1, so the result is the same
    uniform vector. This is easily expanded to an $n$x$n$ version of A.

Show it
=======

-   Since the set of vectors is linearly dependent, there exists a set
    of constants $c_k$ for each vector that will make
    $${c_{1}\vec{v_1} + c_{2}\vec{v_2} + c_{3}\vec{v_3} +   \dots + c_{k}\vec{v_k}} = 0.$$
    Because multiplying each vector of the set by $A$ is a linear
    operation,
    $$c_{i}A\vec{v_i} = Ac_{i}\vec{v_i} \text{ and } A\vec{v_1} + A\vec{v_2} = A(\vec{v_1} + \vec{v_2})$$
    for any number of vectors. Thus, the set
    $$(A\vec{v_1}, A\vec{v_2}, A\vec{v_3},   \dots  A\vec{v_k})$$ can be
    multiplied by the same set of constants $c_k$, and the A factored:
    $$A(c_{1}\vec{v_1} + Ac_{2}\vec{v_2} + Ac_{3}\vec{v_3} +   \dots + Ac_{k}\vec{v_k}) \rightarrow A(c_{1}\vec{v_1} + c_{2}\vec{v_2} + c_{3}\vec{v_3} +   \dots + c_{k}\vec{v_k})$$
    which clearly shows the same condition as before. The set of v can
    still be shown to equal 0 with the same set of constants $c_k$,
    which means they are linearly dependent after the transformation.
    This is due to the linearity of transforming with a matrix A.

Figuring out the tips
=====================

(a) By inspection, we are able to see that the scheme with 6 tips
    ($\vec{T}$) around the table leaves some abiguity in the plates
    vector ($\vec{P}$) by the end of the problem. For example, if
    everyone tips a total of \$2, $$\begin{pmatrix}
          0.5 & 0.5 & 0 & 0 & 0 & 0 \\
          0 & 0.5 & 0.5 & 0 & 0 & 0 \\
          0 & 0 & 0.5 & 0.5 & 0 & 0 \\
          0 & 0 & 0 & 0.5 & 0.5 & 0 \\
          0 & 0 & 0 & 0 & 0.5 & 0.5 \\
          0.5 & 0 & 0 & 0 & 0 & 0.5
        \end{pmatrix}
        \begin{pmatrix}
          2 \\
          2 \\
          2 \\
          2 \\
          2 \\
          2 
        \end{pmatrix} = 
        \begin{pmatrix}
          2 \\
          2 \\
          2 \\
          2 \\
          2 \\
          2 
        \end{pmatrix}$$ We get the resulting plates vector ($\vec{P}$)
    with \$2 in each position However, if everyone tips alternating
    amounts of \$1.50 and \$2.50, we get the same amount in the plates:
    $$\begin{pmatrix}
          0.5 & 0.5 & 0 & 0 & 0 & 0 \\
          0 & 0.5 & 0.5 & 0 & 0 & 0 \\
          0 & 0 & 0.5 & 0.5 & 0 & 0 \\
          0 & 0 & 0 & 0.5 & 0.5 & 0 \\
          0 & 0 & 0 & 0 & 0.5 & 0.5 \\
          0.5 & 0 & 0 & 0 & 0 & 0.5
        \end{pmatrix}
        \begin{pmatrix}
          1.50 \\
          2.50 \\
          0.75 \\
          1.25 \\
          0.75 \\
          1.25
        \end{pmatrix} = 
        \begin{pmatrix}
          2 \\
          2 \\
          2 \\
          2 \\
          2 \\
          2 
        \end{pmatrix}$$

(b) If, however, the number of people at the table is odd, then the
    columns of the resulting matrix are no longer linearly dependent
    (scaled for simplicity): $$\begin{pmatrix}
          1 & 1 & 0 & 0 & 0 \\
          0 & 1 & 1 & 0 & 0 \\
          0 & 0 & 1 & 1 & 0 \\
          0 & 0 & 0 & 1 & 1 \\
          1 & 0 & 0 & 0 & 1 
        \end{pmatrix}\xrightarrow{Row Reduce}
        \begin{pmatrix}
          1 & 0 & 0 & 0 & 0 \\
          0 & 1 & 0 & 0 & 0 \\
          0 & 0 & 1 & 0 & 0 \\
          0 & 0 & 0 & 1 & 0 \\
          0 & 0 & 0 & 0 & 1 
        \end{pmatrix}$$which implies that there is only 1 ($\vec{T}$)
    for each ($\vec{P}$).

(c) To generalize, in this problem, the matrix can be row reduced to
    Reduce Row Echelon Form if n is odd. If it is even, the columns
    become linearly dependent, and there exist an infinity of solutions.

Image Stitching
===============

(a) Two equations: $$\begin{aligned}
    q_x = R_{11}p_x + R_{12}p_y + T_x\\
    q_y = R_{21}p_x + R_{22}p_y + T_y
    \end{aligned}$$ The points $p$ and $q$ are known, while the 4
    rotation elements $R_{ij}$ and the 2 translation elements $T_j$
    are unknown. The 6 total unknowns will require 6 distinct equations,
    which means 3 commond points are needed (each point yields
    2 equations).

(b) System of linear equations: $$\begin{aligned}
    \begin{cases}
        q_{1x} = R_{11}*p_{1x} + R_{12}*p_{1y} + T_x\\
        q_{1y} = R_{21}*p_{1x} + R_{22}*p_{1y} + T_y\\
        q_{2x} = R_{11}*p_{2x} + R_{12}*p_{2y} + T_x\\
        q_{2y} = R_{21}*p_{2x} + R_{22}*p_{2y} + T_y\\
        q_{3x} = R_{11}*p_{3x} + R_{12}*p_{3y} + T_x\\
        q_{3y} = R_{21}*p_{3x} + R_{22}*p_{3y} + T_y
    \end{cases}
    \end{aligned}$$

(c) iPython Notebook also submitted.

(d) If the points are co-linear and related by the equation
    $(p_2 - p_1) = k(p_3 - p_1)$, then it can be rearranged to show:
    $p_3 = \frac{p_{2} - p_{1}}{k} + p_1$ which means that the last two
    equations above are redundant, because they can be represented in
    terms of the other points $p_1$ and $p_2$. The system
    is underdetermined. I don’t see how this makes “geometric sense,”
    but the math is fairly sound.

Your Own Problem
================

-   Suppose a certain ’open till late’ boardgame cafe is having a free
    games night. Ryan, the temp, is the sole staff member working on
    this very crowded and popular evening. Despite the constant hustle
    and bustle, he has time to notice patterns in the way people select
    which games to use, and when they leave. Ryan wants to calculate
    when everyone will leave the store so that he can go home to his
    loving wife, Kelly. Ryan is tired. At 10pm he closes the games
    cabinet and issues a ’last call’; customers can no longer get new
    games, but they can trade between the ones already out, or leave
    the store.

-   Ryan notices that at 10pm, there are 10 people playing Risk. They
    leave at a rate of 0.4 people per person playing per hour (ppppph).
    They transfer to Dixit at a rate of 0.3ppppph and transfer to
    Dominion at a rate of 0.3ppppph.

-   Ryan notices that at 10pm, there are 5 people playing Dixit. They
    leave at a rate of 0.5ppppph and transfer to Dominion at a rate of
    0.5ppppph

-   Ryan notices that at 10pm, there are 6 people playing Dominion. They
    leave at a rate of 0.2ppppph. Everybody loves Dominion.

-   At what time will Ryan get to leave? Asssume that all people must be
    in whole numbers (truncate decimals)

-   This is solved by setting up an intial state vector representing the
    people playing each game at 10pm, and multiplying it by the
    transition matrix until each value is less than 1. The first
    multiplication looks like so: $$\begin{pmatrix}
          0 & 0 & 0  \\
          0.3 & 0 & 0 \\
          0.3 & 0.5 & 0.8 
        \end{pmatrix}
        \begin{pmatrix}
          10 \\
          5 \\
          6
        \end{pmatrix}$$ It takes 6 hours (cycles) to get to 0 people in
    the store, so Ryan gets to leave at 4am. Who even likes Dominion,
    anyway?


