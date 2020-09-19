In this directory, I'm going to take notes on reading "Introduction of Commutative Algebra" by M. F. Atiyah and I. G. Macdonald.


The book is available at, for example:
- US: https://www.amazon.com/dp/0201407515
- Japan: https://www.amazon.co.jp/dp/0201407515


# Introduction

According to the author, commutative algebra was derived from the two sources: algebraic geometry and algebraic number theory.

The central idea of commutative algebra is prime ideal according to the auther. Prime ideals are the generalization of prime numbers in arithmetic. The author says "near a point" in geometrical sense and "localizing" a ring at a prime ideal are similar. I have no idea about this at all, but the author seems trying to say that prime ideals in algebra and points in geometry are similar. What an incredible analogy 🤯

The author credited J. P. Serre and J. Tate as the pioneers of the domain.

# Chapter 1. Rings and Ideals

## Rings and ring homomorphisms

The author presents the definition of `ring`. Suppose A is a set with 2 binary operators (`+` and `*`). A is a ring when:

1. A is an abelian group with the respect to addition.
2. ∀x,y,z∈A((xy)z=x(yz)) i.e. multiplication is associative
3. ∀x,y,z∈A(x(y+z)=xy+xz) i.e. multiplication is distributive over addition
4. ∀x,y∈A(xy=yz) i.e. multiplication is commutative
5. ∃1∈A∀x∈A(x1=1x=x) i.e. There is an identity element.

From 5, the identity element is unique because if i are j are identity elements, then i=ij=j.

When 1 = 0, then x = 1x = 0x = (y - y)x = yx - yx = 0, i.e. the all elements in the ring is 0. In that case, that ring is called zero ring.

Note: (A, +, `*`) is an commutative ring with an identity when A is an abelian group with respect to addition, A is a commutative monoid with respect to multipication, and multiplication is distributive over addition.

Let A and B be rings and f be a map of A -> B, then f is a ring homomorphism if:

1. ∀x,y∈A(f(x+y)=f(x)+f(y))
2. ∀x,y∈A(f(xy)=f(x)f(y))
3. f(1)=1

In other words, f respects addition and multiplication of A and B.

A subset S of a ring A is subring when addition and multiplication of elements of S is closed in S and it has 1.

If f: A -> B, g: B -> C are ring homomorphisms, then g⚬f is a ring homomorphism.

## Ideals. Quotient Rings

An ideal 𝔞 of a ring A is an additive subgroup of A and A𝔞⊆𝔞 i.e. ∀x∈A,y∈𝔞(xy∈𝔞).

Prosition 1.1. There is a one-to-one order-preserving correspondence between the ideal 𝔟 of A which contains 𝔞, and the ideal 𝔟' of A/𝔞, given by 𝔟 = φ^-1(𝔟').
