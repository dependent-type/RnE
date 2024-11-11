$B(x)$ 가 context $\Gamma, x:A$ 하에서의 type일 때, 즉
$$
\Gamma, x: A \vdash B(x) \text { type }
$$
일 때, $B$ 를 **family** of types over $A$ 라 하며, $B(x)$를 context $\Gamma$ 하에서 $x:A$ 에 의해 **indexed**된 타입이라고 한다. 이때 $B$를 $x:A$ 에 따라 변화하는 $B(x)$ 로 생각한다.

>[!example] 
> 이후에 언급될 [[Identity type|identity type]]이 그 대표적인 예시이다. 
> $$\frac{\Gamma \vdash a: A}{\Gamma, x: A \vdash a=x \text { type. }}$$ 
> 이 규칙은 context $\Gamma$ 에서 type $A$ 의 원소 $a: A$가 주어졌을 때, context $\Gamma, x: A$ 에서 유형 $a=x$를 형성할 수 있다고 주장한다. 이 때 형성된 유형 $a=x$ 가 type family over $A$ in context $\Gamma$ 의 예시이다.

