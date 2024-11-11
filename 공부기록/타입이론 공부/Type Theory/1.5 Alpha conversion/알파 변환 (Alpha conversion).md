---
Last modified: 2024-05-05
Category: Type Theory
Contributor:
  - "[[이현진]]"
---
$\lambda x.x^{2}$ 이나 $\lambda u.u^{2}$ 이나 나타내는 바는 같다. 즉 binding variable($\lambda$ 뒤에 붙는 변수와 그에 대해 종속되는 변수) 의 '이름'은 중요한 것이 아니다. 그렇다면 변수의 이름을 바꾸는 것 또한 가능할 것이다.

>[!info] 정의 1. Renaming $M^{x \rightarrow y} ;=_\alpha$
> $M^{x \rightarrow y}$ 는 $M$ 의 모든 $x$ 중 자유 변수인 것들을 $y$ 로 치환한 결과이다. 이를 'renaming' 이라고 하며 다음과 같은 $=_\alpha$ 기호로 표현된다.$$\lambda x . M=_{\alpha} \lambda y . M^{x \rightarrow y}$$이는 $y$ 가 $M$ 내에 없는 변수인 경우에만 가능하다. 즉, (1) $y \notin F V(M)$ 이면서[^1] (2) binding variable도 아니어야[^2] 한다.
> 
>[^1]: 만약 자유변수인 $y$ 가 $M$ 내에 존재했다면, $\alpha$-변환 뒤에는 종속변수가 되어 lambda term의 의미가 바뀌게 된다.
>[^2]: 만약 $y$가 이미 binding variable로 존재하는 상태였다면, 그 $y$ 가 기존의 $x$를 binding 하게 된다.

이는 $\lambda$-term 전체에 대해서만 적용 가능한 정의이다. 이를 더 범용적으로 사용하기 위하여 다음 정의를 도입한다.

>[!info] 정의 2. $\alpha$-conversion ($\alpha$-equivalence)
(1) (Renaming) $\lambda x \cdot M={ }_\alpha \lambda y . M^{x \rightarrow y}$ when $y \notin F V(M)$ and y is not a binding variable in $M$,
(2) (Compatibility) If $M={ }_\alpha N$, then $M L={ }_\alpha N L, L M={ }_\alpha L N$ and, for arbitrary $z, \lambda z . M={ }_\alpha \lambda z . N$,
(3a) (Reflexivity) $M={ }_\alpha M$,
(3b) (Symmetry) If $M={ }_\alpha N$ then $N={ }_\alpha M$,
(3c) (Transitivity) If both $L={ }_\alpha M$ and $M={ }_\alpha N$, then $L={ }_\alpha N$.

$M=_{\alpha}N$ 이면 $M$ 과 $N$ 은 **$\alpha$-convertible** 혹은 **$\alpha$-equivalent** 라고 한다.