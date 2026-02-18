1.1. Locate a discussion of Russell’s paradox, and understand it.  

russell's paradox: 'set of all sets that don't contain themselves' is an
an paradox that revealed an issue in naive set theory -- that being
unrestricted impredicativity (what is now called a 'size issue').

the solution to this problem has essentially been to impose a DAG onto
the definition of sets, they can only contain things strictly below themselves.
proper classes, grothendieck universes and type universes are all manifestations
of this solution.

--------------------------------------------------------------------------------
1.2. Prove that if ∼ is an equivalence relation on a set S, then the
corresponding family P∼ defined in §1.5 is indeed a partition of S: that is,
its elements are nonempty, disjoint, and their union is S. [§1.5]  


equivalence relations ~ have to satisfy
- refl : a ~ a
- symm : a ~ b <=> b ~ a
- tran : a ~ b, b ~ c => a ~ c

partions P~ of a set have to satisfy
- nonempty : ∀a ∈ S, [a]~ != ø
- disjoint : [a]~ ∩ [b]~ => [a]~ = [b]~
- union is S : ∪{a∈S}[a]~ = S

proof that equivalence relations forma partition of S

- nonempty is satisfied via refl. every member [a]~ of the family P~ must
  contain a itself

- disjoint is satisfied via all three properties: 
    suppose c ∈ [a]∼ ∩ [b]∼. then c ∼ a and c ∼ b. 
    take any x ∈ [a]∼, so x ∼ a.
    by symmetry, a ∼ c. 
    by transitivity, x ∼ c. 
    by transitivity again, x ∼ b. 
    so x ∈ [b]∼. 
    this shows [a]∼ ⊆ [b]∼. 
    the reverse inclusion is symmetric (same argument swapping a and b), giving
    [a]∼ = [b]∼.

- union is satisfied via refl. since every element a ∈ S is always a member of
  some equivalence class, the union of all of the members [a]~ ∈ P~ must amount
  to S in its entirity

--------------------------------------------------------------------------------
1.3. Given a partition P on a set S, show how to define a relation ∼ on S such
that P is the corresponding partition. [§1.5]  

we define ~ to be membership within a block

- refl: since every a ∈ S is a member of some block B ∈ S, so a and a is always
  in the same block. a ~ a by definition.

- symm: all members of the same block satisfy ~ by definition, so forall b ∈ B
  and a ∈ B, a ~ b and b ~ a.

- tran: 
    if b is in the same block as a, then a and b ∈ B1
    if c is in the same block as b, then b and c ∈ B2
    since blocks are disjoint, we know that if b is a member of two blocks
    simultaneously, then they must be equal : B1 = B2.
    therefore a must be in the same block as c. a ~ c


--------------------------------------------------------------------------------
1.4. How many different equivalence relations may be defined on the set {1, 2,
3}?  

using [1.3], we know this is the same as the number of partions of {1,2,3}, which
is the same as the number of disjoint combinations of the set.

{1}, {2}, {3}
{1,2}, {3}
{1}, {2,3}
{1,3}. {2}
{1,2,3}

5 in total


--------------------------------------------------------------------------------
1.5. Give an example of a relation that is reflexive and symmetric but not
transitive. What happens if you attempt to use this relation to define a
partition on the set? (Hint: Thinking about the second question will help you
answer the first one.)  

if we don't have transitive, then we can have the scenario in which:
  a ~ b => a, b ∈ B1
  b ~ c => b, c ∈ B2
  but not a ~ c, so a and c are not members of some block.
  in this case, we have that B1 is not equal to B2.
  yet they share b as an element, 
  therefore they are not disjoint.
  

--------------------------------------------------------------------------------
1.6. Define a relation ∼ on the set R of real numbers by setting a ∼ b ⇐⇒ b−a ∈
Z. Prove that this is an equivalence relation, and find a ‘compelling’
description for R/∼. Do the same for the relation ≈ on the plane R × R defined
by declaring (a1, a2) ≈ (b1, b2) ⇐⇒ b1 − a1 ∈ Z and b2 − a2 ∈ Z. [§II.8.1,
II.8.10]

- refl: ∀ a ∈ R, a - a = 0, which is in Z
- symm: 
    ∀ a ∈ R, ∀ b ∈ R, a - b = - (b - a)
    let a - b = c
    if c ∈ Z, then -c must also be in Z
    therefore a - b ∈ Z <=> b - a ∈ Z
- trans: 
    a, b, c ∈ R
    a - b ∈ Z
    b - c ∈ Z
    let a - b = n
    let b - c = m
    a - c = (a - b) + (b - c)
          = n + m
    the sum of two integers is an integer
    therefore a - c ∈ Z

semantic description: this is an equivalence relation that quotients out all reals
which are integer steps away from one another. said alternatively, it collapses the
reals into blocks whose members are all some integer away from one another.
in the fractional representation, real numbers in the block look like
N.M, where N may differ, but M is the same.
this turns the real number line into the interval [0,1), or the circle S1. notably
it is not the interval [0,1), because the two ends are equivalent under ~.


for the second part, the proof is the exact same but just component wise.

semantically, this means turning R2 into [0,1) glued with [0,1), which is the
torus T2.



