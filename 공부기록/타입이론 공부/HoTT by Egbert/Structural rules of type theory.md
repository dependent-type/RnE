Dependent type theory의 구조를 완성시키 위해 마지막으로 가정해야 하는 것들.

(i) 만약 우리가 context $\Gamma$에서 유형 $A$를 가지고 있다면,  문맥 $\Gamma, \Delta$에서의 어떤 판정도 새로운 변수 $x$에 대해 문맥 $\Gamma, x: A, \Delta$에서도 만들 수 있습니다. 약화 규칙은 문맥에 유형 $A$를 추가함으로써 유형과 용어의 잘 구성되었음과 판단적 동등성을 보존함을 주장합니다.

$$
\frac{\Gamma \vdash A \text { type } \quad \Gamma, \Delta \vdash \mathcal{J}}{\Gamma, x: A, \Delta \vdash \mathcal{J}} W_A
$$

컨텍스트를 유형 $A$의 새로운 변수로 확장하는 이 과정을 "약화(weakening)($A$에 의해)"라고 합니다. 유형 $A$ 위의 유형 패밀리 $W_A(B)$는 또한 상수 패밀리(constant family) $B$ 또는 단순 패밀리(trivial family) $B$로도 불립니다.