# To Mock A Mockingbird

Reading Smullyan's book ["To Mock a Mockingbird"](https://en.wikipedia.org/wiki/To_Mock_a_Mockingbird).

I only do the problems after Chapter 9.

## Chapter 9

The birds are combinators, in other words, lambda expressions. The mockingbird is λx.xx. This helps a lot in thinking about various birds, puzzles, and problems.

### 1. The Significance of the Mockingbird

This problem is basically about finding a fixed-point combinator. If Y is a fixed-point combinator, then Y g = g (Y g). This means g is fond of Y g for any g. Keeping this in mind, this problem is still very tricky because we only have M, the mocking bird, and the composition condition. Look carefully on the famous Y combinator λg.(λx.g(xx))(λx.g(xx)). There are three parts where the same pattern XX appears. That is (IMO) the main trick of this problem. This lambda expression can be written in terms of combinations of the composition of M.

- Let g be any bird.
- There exists a bird, g ⚬ M, the composition of g and M because of the composition condition.
- Let T be a bird (g ⚬ M)(g ⚬ M).
- g is fond of T,
- because T = (g ⚬ M)(g ⚬ M) - by definition
- = g(M(g ⚬ M)) - by the composition rule
- = g((g ⚬ M)(g ⚬ M)) - by the mockingbird's nature
- = g T - by the definition of T

Therefore any bird is fond of at least one bird. QED.

### 2. Egocentric?

- (M ⚬ M)(M ⚬ M) is egocentric because (M ⚬ M)(M ⚬ M) = M((M ⚬ M)(M ⚬ M))
- = ((M ⚬ M)(M ⚬ M))((M ⚬ M)(M ⚬ M))
- This means (M ⚬ M)(M ⚬ M) is fond of itself i.e. is egocentric. QED.

The answer section show a more indirect solution using the result of the previous problem.

### 3. Agreeable Bird

- Let A be an agreeable bird.
- Let f be an any bird.
- Let C be f ⚬ A.
- Because A is an agreeable bird, Ax = Cx for some x.
- Cx = f(Ax) --- by definition of C
- ... = f(Cx) --- by definition of x
- This means f is fond of Cx for some x for any bird f. QED.

- M is agreeable because for any B, MB = BB.
- Therefore 1. is a special case of 3.

### 4. Agreeable Bird 2

- Let D an arbitrary bird.
- Let E be D ⚬ B.
- Because C is agreeable, Cx = (D ⚬ B)(x) for some x. --- (a.)
- (A ⚬ B)(x) = Cx --- by def of C. --- (b.)
- (D ⚬ B)(x) = D(Bx) --- by def of composition. --- (c.)
- Because of (a.), (b.), and (c.), A(B(x)) = D(B(x)).
- This means A and D agree on B(x) and D is an arbitrary bird.
- Therefore A is agreeable bird. QED.

### 5. An Excercise in Composition

- Let E be B ⚬ C.
- A ⚬ E exists because of the composition law.
- Let x be an any bird.
- (A ⚬ E)(x) = A(E(x)) --- by def of composition
- ... = A((B ⚬ C)(x)) --- by def of E
- ... = A(B(Cx)) --- by def of composition
- Therefore A ⚬ E is D. QED.
