---
Last modified: 2024-05-05
Category: Type Theory
Contributor:
  - "[[이현진]]"
---
# Multiset of subterms, Sub

$\verb|Sub|$ is a multiset of all subterms, which could be constructed from the set of all variables $V=\left\{x,y,z,...\right\}$, as follows:

>[!info] Deductive definition
>(1) (Basis) $\verb|Sub|(x)=\{x\}$, for each $x \in V$.
>
>(2) (Application) $\verb|Sub|((M N))=\verb|Sub|(M) \cup \verb|Sub|(N) \cup\{(M N)\}$.
>
>(3) (Abstraction) $\verb|Sub|((\lambda x . M))=\verb|Sub|(M) \cup\{(\lambda x . M)\}$.

# Tree representation

The subterms of a $\lambda$-term $M$ correspond to the subtrees in the tree representation of $M$.

$\verb|Sub|(y(\lambda x. (x \, z)))$ is just a subtree of following tree:
![[스크린샷 2024-01-05 오후 5.53.53.png|400]]

# Proper subterm

>[!info] Definition 
> $L$ is a proper subterm of $M$ if $L$ is a subterm of $M$, but $L \not \equiv M$.
