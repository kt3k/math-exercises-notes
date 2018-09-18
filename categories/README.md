# categories

- This notes are based on http://www.math.uchicago.edu/~mitya/topics-in-algebra/categories.pdf

> Every non-obvious statement in each of the examples appearing below should be treated
as an exercise

Nice way to present exercises :+1:

## Exercises

### 1.3

- Let 𝒞 be an category and X an object in 𝒞.
- Let f and g be identities of X.
- Because f is an identify, f ⚬ g = g. --- (1)
- Because = is symmetric and (1), g = f ⚬ g. --- (2)
- Because g is an identify, f ⚬ g = f. --- (3)
- Because (2), (3), and = is transitive, g = f. QED

### 1.4

#### (1)

- Let X, Y, Z, W be objects in Sets.
- Let f: X -> Y, g: Y -> Z, h: Z -> W be morphisms.
- For any x in X, ((h ⚬ g) ⚬ f)(x) = (h ⚬ g)(f(x)) = h(g(f(x))) = h((g ⚬ f)(x)) = (h ⚬ (g ⚬ f))(x), which means (h ⚬ g) ⚬ f = h ⚬ (g ⚬ f).
- Therefore the composition satisfies the axiom of Categories, and therefore Sets is a category.

#### (2)

- The same argument holds.

#### (3)

- Let X, Y, Z be objects in Groups.
- Let f: X -> Y, g: Y -> Z be morphisms.
- Let x, y elements of X.
- (g ⚬ f)(x * y) = g(f(x * y)) - (1) because of the composition definition.
- g(f(x * y)) = g(f(x) * f(y)) - (2) because f is a homomorphism.
- g(f(x) * f(y)) = g(f(x)) * g(f(y)) - (3) because g is a homomorphism.
- g(f(x)) * g(f(y)) = (g ⚬ f)(x) * (g ⚬ f)(y) - (4) because of the composition definition.
- Because of (1), (2), (3), and (4), (g ⚬ f)(x * y) = (g ⚬ f)(x) * (g ⚬ f)(y).
- Therefore g ⚬ f is a homomorphism, which means the composition definition is closed among homomophisms, and therefore Groups is a category.
