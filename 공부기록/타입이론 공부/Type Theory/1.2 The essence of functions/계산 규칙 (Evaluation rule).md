---
Last modified: 2024-05-05
Category: Type Theory
Contributor:
  - "[[이현진]]"
---

# $\beta$-축약

표현 $(\lambda x . M) N$에 대해서, 이는 다음과 같이 '축약'될 수 있다:
$$
M[x:=N]
$$
이 때, $(\lambda x . M) N$를 포함하는 기존 전체 식이 $M[x:=N]$를 포함하는 전체 식으로 **축약**되었다고 말한다. 축약된 표현과 그 이전의 표현은 다른 표현이다. '축약'이란 적용(application)으로 만들어진 새로운 표현을 실제로 계산(execute)하는 것이다.

>[!example]-
>- $\left(\lambda x . x^2+1\right)(3)$는 $\left(x^2+1\right)[x:=3]$로 축약되고, 그 값은 10이다.
>- $(\lambda y .5)(3)$는 $5[y:=3]$로 축약되고, 그 값은 5 이다.
>- $(\lambda x . x)(\lambda y . y)$는 $x[x:=\lambda y . y]$로 축약되고, 그 값은 $\lambda y . y$이다.

축약은 큰 표현의 일부분에서도 가능하다. 즉, 형태가 $(\lambda x . M) N$인 표현이 더 큰 표현의 하위 표현일 때, 이 하위 표현식은 위에서 설명한대로 $M[x:=N]$으로 다시 쓸 수 있다. (단, 표현식의 나머지 부분은 변경되지 않아야한다.)