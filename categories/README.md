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

#### (1) Sets is a category

- Let X, Y, Z, W be objects in Sets.
- Let f: X -> Y, g: Y -> Z, h: Z -> W be morphisms.
- For any x in X, ((h ⚬ g) ⚬ f)(x) = (h ⚬ g)(f(x)) = h(g(f(x))) = h((g ⚬ f)(x)) = (h ⚬ (g ⚬ f))(x), which means (h ⚬ g) ⚬ f = h ⚬ (g ⚬ f).
- Therefore the composition satisfies the axiom of Categories, and therefore Sets is a category.

#### (2) sets is a category

- The same argument holds.

#### (3) Groups is a category

- Let X, Y, Z be objects in Groups.
- Let f: X -> Y, g: Y -> Z be morphisms.
- Let x, y be elements of X.
- (g ⚬ f)(x * y) = g(f(x * y)) - (1) because of the composition definition.
- g(f(x * y)) = g(f(x) * f(y)) - (2) because f is a homomorphism.
- g(f(x) * f(y)) = g(f(x)) * g(f(y)) - (3) because g is a homomorphism.
- g(f(x)) * g(f(y)) = (g ⚬ f)(x) * (g ⚬ f)(y) - (4) because of the composition definition.
- Because of (1), (2), (3), and (4), (g ⚬ f)(x * y) = (g ⚬ f)(x) * (g ⚬ f)(y).
- Therefore g ⚬ f is a homomorphism, which means the composition definition is closed among homomophisms, and therefore Groups is a category.
- (For the composition axiom, the same arguments as Sets holds.)

#### (4) groups is a category

- The same arguments as (3) hold.

#### (5) Ab is a category

- The same arguments as (3) hold.

#### (6) ab is a category

- The same as (3).

#### (7) `Vect_k` is a category

- Let X, Y, Z be vector spaces over k.
- Let f: X -> Y, g: Y -> Z be linear maps.
- Let x ∈ X.
- Let a ∈ k.
- (g ⚬ f)(ax) = g(f(ax)) --- by definition of g ⚬ f
- = g(af(x)) --- because f is a linear map.
- = ag(f(x)) --- because g is a linear map.
- = a(g ⚬ f)(x) --- by definition of g ⚬ f
- g ⚬ f is a linear map from X to Z.
- The composition is closed among linear maps, which means `Vect_k` forms a category. QED.

#### (8) `vect_k` is a category

- The same as (7).

#### (9) Top is a category

- Let X, Y, Z be topological spaces.
- Let f: X -> Y, g: Y -> Z be continuous maps.
- Let U ⊂ Z be an open set.
- (g ⚬ f)^-1(U) = f^-1(g^-1(U)) --- by definition of the inverse map.
- g^-1(U) is an open set in Y because g is a continuous map.
- Therefore f^-1(g^-1(U)) is an open set in X because f in a continuous map.
- This means g ⚬ f is a continuous map and the composition is closed among continous maps.
- This measn Top forms a category. QED.

### 1.5

#### 1st question

- Let X be a topological space.
- Let U, V, W in Op(X) such that U ⊆ V and V ⊆ W.
- Let a: U -> V, b: V -> W, c: U -> W.
- b ⚬ a equals inevitably c because there is no other choice.

#### 2nd question

- Let U, V, W, X in Op(X) such that U ⊆ V ⊆ W ⊆ X.
- Let f: U -> V, g: V -> W, h: W -> X, k: U -> X.
- (h ⚬ g) ⚬ f = k = h ⚬ (g ⚬ f) because there is no other choice.

### 1.6

#### The inverse is unique

- Let 𝒞 be a category, f: X -> Y be a morphism, g, h is inverse of f.
- g = g ⚬ id_Y = g ⚬ (f ⚬ h) = (g ⚬ f) ⚬ h = id_X ⚬ h = h. QED.
