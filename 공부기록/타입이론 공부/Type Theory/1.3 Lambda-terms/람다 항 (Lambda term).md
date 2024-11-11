---
Last modified: 2024-05-02
Category: Type Theory
Contributor:
  - "[[이현진]]"
---
이제부터는 본격적으로 람다 대수의 세계로 들어가 보도록 하겠다. 그 첫 걸음으로, 명확하게 언급하지 않았던 '표현'의 정의를 알아보자. 람다 대수에서는, 우리가 지금까지 다뤘던 표현을 '**$\lambda$-term**' 이라고 부른다.

모든 $\lambda$-term 의 집합을 일반적으로는 $\Lambda$ 로 표기하며, 모든 변수(variable)들의 집합 $V=\left\{x,y,z,...\right\}$로부터 귀납적으로 construct될 수 있다.

>[!info] $\Lambda$ 의 귀납적 정의
>(1) (Variable) If $u \in V$, then $u \in \Lambda$.
>
>(2) (Application) If $M$ and $N \in \Lambda$, then $(M N) \in \Lambda$.
>
>(3) (Abstraction) If $u \in V$ and $M \in \Lambda$, then $(\lambda u . M) \in \Lambda$.
>
>(1), (2), (3) are the only ways to construct elements of $\Lambda$. 

다음과 같은 abstract syntax로 간단하게 표현할 수도 있다.

>[!tip] Abstract syntax
> $\Lambda=V|(\Lambda \Lambda)|(\lambda V . \Lambda)$]]
