---
Last modified: 2024-01-05
Category: Type Theory
Contributor:
  - "[[이현진]]"
---
# Application

For the type of the application $M N$, we clearly have to know the types of $M$ and $N$. Based on the intention of $MN$, $M$ must be applied to 'input term' $N$. Therefore, type of $M$ and $N$ must be as follows:
$$
M:\sigma \rightarrow \tau, N:\sigma, MN:\tau
$$

# Abstraction

Similarly, since $\lambda x.M$ is the function that has a input value $x$ and output $M$. Therefore, we could let the types of $x$ and $M$ such as $x:\sigma$, $M:\tau$, type of $\lambda x.M$ must be function type as follows:
$$
\lambda x.M : \sigma \rightarrow \tau
$$
