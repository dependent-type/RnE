---
Last modified: 2024-05-05
Category: Type Theory
Contributor:
  - "[[이현진]]"
---
# The set $\mathbb{T}$ of all simple types

$\mathbb{T}$ is a set of all **simple types**, which could be build from the infinite set of **type variables**: $\mathbb{V}=\{\alpha, \beta, \gamma, \ldots\}$, as follows:

>[!info] Definition
> (1) (Type variable) If $\alpha \in \mathbb{V}$, then $\alpha \in \mathbb{T}$,
> (2) (Arrow type) If $\sigma, \tau \in \mathbb{T}$, then $(\sigma \rightarrow \tau) \in \mathbb{T}$.

>[!tip] Abstract syntax
$\mathbb{T}=\mathbb{V} \mid \mathbb{T} \rightarrow \mathbb{T}$.

>[!example]- 
Examples of simple types: $\gamma,(\beta \rightarrow \gamma),((\gamma \rightarrow \alpha) \rightarrow(\alpha \rightarrow(\beta \rightarrow \gamma)))$.

>[!note] Notation 
>(1) The Greek letters $\alpha, \beta, \ldots$ and variants thereof are used for type variables belonging to $\mathbb{V}$.
>(2) We use $\sigma, \tau, \ldots$ (occasionally $A, B, \ldots$ ) to denote arbitrary simple types.
>(3) Outermost parentheses may be omitted.
>(4) The parentheses in arrow types are **right-associative**.

>[!warning] Note
> Note the right-associativity of the arrow, in contrast with the left-associativity of application. So $\alpha_1 \rightarrow \alpha_2 \rightarrow \alpha_3 \rightarrow \alpha_4$ is shorthand for the simple type $\left(\alpha_1 \rightarrow\left(\alpha_2 \rightarrow\left(\alpha_3 \rightarrow \alpha_4\right)\right)\right)$, whereas $x_1 x_2 x_3 x_4$ abbreviates $\left(\left(\left(x_1 x_2\right) x_3\right) x_4\right)$.

>[!warning] Remark
>Apart from the type variables $\alpha, \beta, \ldots$, we also still have (ordinary) variables $x, y, \ldots$. When we speak simply about variables, from now on we only mean the latter species.

# Intended meaning of the types

- type variables are **abstract representations** of basic types such as $\verb|Nat|$ for natural numbers, $\verb|List|$ for lists, etcetera.
- arrow types represent **function types**, such as nat $\rightarrow$ real (the set of all functions from naturals to reals) or (nat $\rightarrow$ integer) $\rightarrow$ (integer $\rightarrow$ nat) (the set of all functions with input a function from naturals to integers and output a function from integers to naturals).

>[!warning] Remark
>We distinguish between the sets $\mathbb{N}$ or $\mathbb{L}$ and the types nat or list, because sets like $\mathbb{N}$ belong to mathematics and types like nat to computer science. Otherwise said: $\mathbb{N}$ is a collection of things in the 'real world' of mathematical entities, whereas nat is some coding of these entities in the 'virtual world' of computer programming. This distinction between sets and types will repeatedly play a role in the rest of this book.

# Typing statements

For term $M$ and type $\sigma$, we could express things like 'term $M$ has type $\sigma$' as follows:
$$
M:\sigma
$$
this is so-called **statements**(or typing statements)

>[!info] Assume
> (1) We have an infinitude of variables available for each type $\sigma$.
> 
> (2) Each variable $x$ has a unique type:
> 	if $x: \sigma$ and $x: \tau$, then $\sigma \equiv \tau$.

>[!example] 
> variable $x$ has type $\sigma$: $x:\sigma$

[[Construction principles with types]]