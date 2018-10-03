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
