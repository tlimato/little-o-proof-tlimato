[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/wM4-KOzy)
# Little-o

In addition to the big-O, big-$\Omega$, and big-$\Theta$ notation that
we covered at the beginning of this class, a few other notations are sometimes
used in asymptotic analysis.  For example, "little-$o$" notation.

Prove (i.e.\ give a formal mathematical proof) that $f(n)\in o(g(n))$ implies
that $f(n)\in O(g(n))$.

Hint: The proof will be *very* short and *very* easy. You can start by
identifying the differences between the definitions of O and o.

I have started with the formal definition of $o$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$f(n)\in o(g(n)) \iff \forall c>0, \exists n_0, \forall n\ge n_0: f(n) < c g(n)$

## NOT STRICTLY FORMAL PROOF:

First we need to clarify the implications of the definitions.
Given that $f(n) \in o(g(n))$, by definition, this means the following

- For any positive constant $c$, there exists some threshold $n_0$ beyond which $f(n)$ is always less than $c \cdot g(n)$.

Now, consider the definition of Big-O notation:
$$
f(n) \in O(g(n)) \iff \exists c' > 0, \exists n_0', \forall n \geq n_0': f(n) \leq c' \cdot g(n)
$$

To show that $f(n) \in o(g(n))$ implies $f(n) \in O(g(n))$, we start by choosing any constant $c' > c$. 
(Note: This choice is possible because $c$ is any positive constant, and we can always find a larger constant $c'$.)
We then set $n_0'$ equal to $n_0$. The value $n_0$ is the threshold beyond which the condition $f(n) < c \cdot g(n)$ holds true, as specified by the definition of little-o notation.

Then, for all $n \geq n_0'$, the following inequalities hold:

$$
f(n) < c \cdot g(n) \leq c' \cdot g(n)
$$

here we see that $f(n)$ is not only less than $c \cdot g(n)$ but also less than or equal to $c' \cdot g(n)$.
This satisfies the condition for Big-O notation, which requires that there exists some constant $c'$ and some threshold $n_0'$ such that $f(n) \leq c' \cdot g(n)$ for all $n \geq n_0'$. 
Therefore, we have shown that if $f(n)$ is in little-o of $g(n)$, it must also be in Big-O of $g(n)$.


References:
- https://en.wikipedia.org/wiki/Big_O_notation
- https://en.wikipedia.org/wiki/Little-o_notation

I use Github Copilot to assist in writing code, It's built into my vs code install I use for Professional work and It's helpful in accelerating projects and avoiding syntax issues. I will make this clarification on other assignments as well.
