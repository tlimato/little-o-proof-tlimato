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
If a function f(n) grows much slower than g(n) (i.e., f(n)∈o(g(n))), it also means that f(n)grows no faster than g(n) (i.e., f(n)∈O(g(n))). 
This is because f(n)∈o(g(n)) implies that for any positive constant cc, starting from some point n0, f(n) will always be less than c⋅g(n). 
Now, consider the definition of O(g(n)): it states that there exist constants c′ and n0′ such that f(n) is bounded above by c′⋅g(n) for all n≥n0′. 
By choosing a c′ greater than any cc we choose for o(g(n)), and keeping n0′=n0, we ensure that f(n) is still bounded by c′⋅g(n) for all n≥n0.
So, if f(n)∈o(g(n)), it also implies f(n)∈O(g(n)).

