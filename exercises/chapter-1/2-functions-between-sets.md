2.1. How many different bijections are there between a set S with n elements
and itself? [§II.2.1]  

equal to number of permutations of S. n!


--------------------------------------------------------------------------------
2.2. Prove statement (2) in Proposition 2.1. You may assume that given a family
of disjoint nonempty subsets of a set, there is a way to choose one element in
each member of the family [§2.5, V.3.3]  

> Proposition 2.1. Assume A != ∅, and let f : A → B be a function. Then  
> (1) f has a left-inverse if and only if it is injective.  
> (2) f has a right-inverse if and only if it is surjective.

(==>) 
  if f has a right inverse g, then ∀ b ∈ B we have f g b = b, so b is in
  the image of f. therefore f is surjective.

(<==)
  if f is surjective, then ∀ b ∈ B, the inverse f* b is nonempty.
  so to construct the right inverse g : B -> A, we can let g(b) be defined
  as the chosen element of f*(b) by the axiom of choice. 
  then, ∀ b ∈ B, f g b = b
    


--------------------------------------------------------------------------------
2.3. Prove that the inverse of a bijection is a bijection and that the
composition of two bijections is a bijection.  



2.4. Prove that ‘isomorphism’ is an equivalence relation (on any set of sets). [§4.1]  2.5. Formulate a notion of epimorphism, in the style of the notion of monomorphism seen in §2.6, and prove a result analogous to Proposition 2.3, for epimorphisms and surjections. [§2.6, §4.2]  2.6. With notation as in Example 2.4, explain how any function f : A → B determines a section of πA.  2.7. Let f : A → B be any function. Prove that the graph Γf of f is isomorphic to A.  2.8. Describe as explicitly as you can all terms in the canonical decomposition (cf. §2.8) of the function R → C defined by r → e2πir. (This exercise matches one assigned previously. Which one?)  2.9. Show that if A′ ∼= A′′ and B′ ∼= B′′, and further A′ ∩B′ = ∅ and A′′ ∩B′′ = ∅,  then A′ ∪ B′ ∼= A′′ ∪ B′′. Conclude that the operation A B (as described in §1.4) is well-defined up to isomorphism (cf. §2.9). [§2.9, 5.7]  2.10. Show that if A and B are finite sets, then |BA| = |B||A|. [§2.1, 2.11, §II.4.1]  12The reader should also be aware that there are important variations on the operations we have seen so far—particularly important are the fibered flavors of products and disjoint unions. 13This (reasonable) statement is the axiom of choice; cf. §V.3. 18 I. Preliminaries: Set theory and categories  2.11. In view of Exercise 2.10, it is not unreasonable to use 2A to denote the set of functions from an arbitrary set A to a set with 2 elements (say {0, 1}). Prove that there is a bijection between 2A and the power set of A (cf. §1.2). [§1.2, III.2.3]
