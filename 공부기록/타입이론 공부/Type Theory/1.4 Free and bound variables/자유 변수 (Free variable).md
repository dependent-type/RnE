---
Last modified: 2024-05-05
Contributor:
  - "[[이현진]]"
Category: Type Theory
---
# Set of all free variables, $FV$

For arbitrary variable $x\in V$,

>[!info] Definition 
> (1) (Variable) $F V(x)=\{x\}$
> 
(2) (Application) $F V(M N)=F V(M) \cup F V(N)$
>
(3) (Abstraction) $F V(\lambda x . M)=F V(M) \backslash\{x\}$

>[!example]- 
>$\begin{aligned} &-F V(\lambda x . x y)= F V(x y) \backslash\{x\} \\ &=(F V(x) \cup F V(y)) \backslash\{x\} \\ &=(\{x\} \cup\{y\}) \backslash\{x\} \\ &=\{x, y\} \backslash\{x\} \\ &=\{y\} . \\\\ &-F V(x(\lambda x . x y))=\{x, y\} .\end{aligned}$

>[!warning] 
>Free variable이더라도 $\lambda$-term의 어딘가에서는 bound일 수 있다.

# Tree representation

![[스크린샷 2024-01-05 오후 5.53.53.png|400]]

특정 위치의 변수가 자유변수인지는 tree representation을 통해 쉽게 알 수 있다. 해당 변수의 노드에서 위를 향해 끝까지 경로를 그리면 (자명하게도 그 경로는 하나일 것이다.) 해당 경로에 $\lambda x$ 와 같은 abstraction 노드가 존재하는지 확인하면 된다.

[[닫힌 람다 항 (Closed lambda-term)]]
