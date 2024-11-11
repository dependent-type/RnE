context 는 다음과 같은 순차적인 변수 선언들의 모음이다.
$$
x_1: A_1, x_2: A_2\left(x_1\right), \ldots, x_n: A_n\left(x_1, \ldots, x_{n-1}\right)
$$
위와 같은 형식의 context 가 변수 $x_1, \ldots, x_n$ 을 declare한다고 한다.
단, 같은 변수가 두 번 선언될 수는 없다.

뒤에 위치한 변수 선언을 함에 있어 앞에 위치한 변수선언이 전제로서 사용될 수도 있다. 즉,
$$
x_1: A_1, x_2: A_2, \ldots, x_{k-1}: A_{k-1} \vdash A_k \text { type }
$$

context의 길이가 0인 경우, 이를 empty context라고 한다. 이러한 context는 well-formedness 조건을 '공허하게' 만족한다. 즉 empty context는 well-formed이다. empty context는 closed type으로도 불리며, 해당 context에서 well-formed 인 term을 closed term이라고도 한다.
