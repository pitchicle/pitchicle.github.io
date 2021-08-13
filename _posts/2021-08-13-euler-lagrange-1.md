---
layout: post
title: "오일러-라그랑주 방정식 (1)"
author: jungwoo.yu
comments: true
date: 2021-08-13 10:50
use_math: true
tags: [mathematics]
---

(이 글은 고민우, 유정우가 진행하는 시리즈 글입니다.)

먼저 오일러의 변분법에서의 오일러 방정식을 살펴봅시다. 오일러 라그랑주 방정식은 오일러 방정식의 일부 특수한 함수의 적용사례라고 생각하시면 편할 것 같습니다.

어떤 범함수 $J$가 존재한다고 합시다. 먼저 범함수는 어떤 함수를 입력받으면 어떤 스칼라값을 내놓는 함수를 말합니다. 저희는 그 범함수 $J$를 다음과 같이 정의해줍시다. (여기서 $y^\prime$은 $x$에 대한 $y$의 순간변화율을 의미합니다.)


$$
J = \int_{x_1}^{x^2}f(x,y,y^\prime)dx
$$
즉, $x$와 $y$와 $y'$을 변수로 가지는 어떤 함수 $f$에 대한 범함수 $J$를 정의해 준 것이죠. 그리고 저희의 최종 목적은 $J$의 극값을 가지는 $y$를 찾는 것이고 그렇게 된다면 이때의 $y$는 $y(\alpha,x)=y(0,x)+\alpha\eta(x))$가 될 것입니다. 


$$
y(\alpha,x) = y(0,x)+\alpha\eta(x)
$$
![](https://user-images.githubusercontent.com/46587635/129293611-45b8907d-83d6-442d-a7b5-8f412a219282.png)

그러니까 $\eta(x)$는 $J$가 극값이 되는 경로인 $y(0,x)$에서 임의의 $x$지점에서 다른 $y(x)$와 $y(0,x)$가 얼마나 떨어져있는지를 나타내는 함수라고 생각할 수가 있고, $\alpha$는 임의의 작은 실수로 $y(x)$가 $y(0,x)$로 부터 조금 벗어나있음을 알려주게 됩니다. 

그렇게 되면 당연히 $\eta(x1)=0$, $eta(x2)=0$임을 알 수가 있습니다. 시작하는 곳과 도착하는 곳에서의 오차는 존재할 수 없기 때문이죠.

자 다시 한번 생각해봅시다. 저희의 최종 목표가 뭐였죠? $J$의 극값을 가지게 하는 $y$를 찾는 것입니다. 그러면 여기서 $\alpha=0$일때 $J$가 극값을 가진다는 것을 수학적으로 보이면 되겠죠? 이걸 수학적으로 표현해주면 다음과 같이 씁니다.


$$
[{\partial J \over \partial \alpha}]_{\alpha=0} = 0
$$


이제 $J$를 $\alpha$에 대해 편미분을 해줍시다. 이때 연쇄율을 이용하여 표현하면 다음과 같습니다. 


$$
{\partial J \over \partial \alpha} = \int_{x_1}^{x_2}\{ {\partial f \over \partial x}{\partial x \over \partial \alpha}+{\partial f \over \partial y}{\partial y \over \partial \alpha}+{\partial f \over \partial y^\prime}{\partial y^\prime \over \partial \alpha} \}dx
$$


이제 이 식의 중괄호 내부에 있는 것을 풀어줍니다. $x$와 $\alpha$는 독립변수이기 때문에 첫번째 항은 소거되고 두번째 항과 세번째 항을 풀 수 있겠죠? 다른 변수들에 대한 $f$의 변화율은 $f$가 어떤 함수인지 모르니 그대로 남겨둡니다. 


$$
{\partial y \over \partial \alpha} = \eta(x) \text{, }
{\partial y^\prime \over \partial \alpha} = \eta^\prime(x) \text{, }
{\partial x \over \partial \alpha} = 0
$$


이를 대입하여 정리하면


$$
{\partial J \over \partial \alpha} = \int_{x_1}^{x_2}\{ {\partial f \over \partial y}\eta(x) + {\partial f \over \partial y^\prime}\eta^\prime(x) \}dx
$$


이고 여기서 부분적분을 이용합시다. 첫번째 항을 그대로 남겨두고 두번째 항을 부분적분해줍니다. 


$$
{\partial J \over \partial \alpha} = \int_{x_1}^{x_2}\{ {\partial f \over \partial y}\eta(x) - {d\over dx}{\partial f \over \partial y^\prime}\eta(x) \}dx + [{\partial f \over \partial y^\prime}\eta(x)]_{x_1}^{x_2} \\
\eta(x_1)=\eta(x_2)=0
$$


그러면 이와같이 되고 위의 $\eta$조건을이용하여 정리해주면 


$$
{\partial J \over \partial \alpha} = \int_{x_1}^{x_2}({\partial f \over \partial y}-{d\over dx}{\partial f \over \partial y^\prime})\eta(x)dx
$$


가 되고 이것이 0이 되어야 합니다. 이 때 임의의 $\eta(x)$에 대해 성립하는 것이므로 대괄호로 묶인 항이 0이 되어야 합니다.

따라서 다음과 같은 오일러 방정식을 얻게 되는 것이죠.


$$
{\partial f \over \partial y}-{d\over dx}{\partial f \over \partial y^\prime} = 0
$$
이게 변분법의 기본정리에 의한 오일러방정식입니다. 위에서는 시각적으로 쉽게 하기위해 좌표에 $x$, $y$를 넣었지만 꼭 좌표에서만 해당하는 것이 아니고, 함수의 형태나조건만 맞는다면 다른 변수도 대입하여 활용할 수 있습니다.

그러면 이제 오일러-라그랑주 방정식은 무엇일까요? 그것은 바로 $f$에 라그랑지안인 $L$을 대입한 것입니다.

이와 위치에너지의 정의를 이용하여 $F=ma$를 유도해 보도록 하겠습니다.

먼저 위의 식들은 운동에너지와 위치에너지 공식입니다.


$$
T = {1\over2}mv^2 \\
{dV\over dx} = -F
$$


라그랑지안은 계의 동역학을 나타내는 함수입니다. 계의 운동에너지 $T$에서 위치에너지 $V$를 뺀 값을 라그랑지안이라고 정의합니다.  


$$
L = T-V
$$


라그랑주 역학에서는 계의 상태를 어떤 물체의 좌표와 속도를 이용하여 나타내기 때문에 라그랑지안은 좌표와 속도의 함수입니다. 즉 $L(t,x(t),x^\prime(t))$인 것이죠. ($x$는 좌표 위치, $x^\prime$은 속도입니다)그런데 이런 형태 어디서 많이 보지 않았나요? 바로 위에서 얘기한 f랑 똑같은 형태인 것이죠. 그럼 이제 위의 오일러 방정식에 $f=L$, $y=x$, $y'=x'$, $x=t$를 넣어서 정리해주면 


$$
\begin{matrix}
{\partial L \over \partial x} - {d\over dt}{\partial L \over \partial v} &=& { {\partial ({1\over2}mv^2-V)}\over \partial x}-{d\over dt}({ {\partial ({1\over2}mv^2-V)}\over \partial v}) \\
&=& F - {d\over dt}(mv) \\
&=& F-ma \\
&=& 0 \\
&\Leftrightarrow& F=ma
\end{matrix}
$$


$F=ma$가 유도되는 것입니다. (단, 이때 유도되는 공식은 보존력에 대해 성립하며, 원래 기존의 편미분에서는 $x$를 $x^\prime$으로 편미분할 때의 값은 자명하게 0이라고 할 수 없으나, 라그랑지안을 적용하는 오일러-라그랑주 방정식에서는 이것이 0입니다. 즉, 어떤 변수의 시간에 대한 도함수꼴의 변수여도 모양이 서로 다르면 다른 변수로 가정하여 문제를 해결하므로 주의하시기 바랍니다.)

다음 시간에는 오일러 방정식과 오일러-라그랑주 방정식의 응용사례와 라그랑주 역학의 자세한 이야기를 하겠습니다.



출처:

\- [위키피디아 라그랑지언](https://ko.wikipedia.org/wiki/%EB%9D%BC%EA%B7%B8%EB%9E%91%EC%A7%80%EC%96%B8)

\- [위키피디아 오일러-라그랑주 방정식](https://ko.wikipedia.org/wiki/오일러-라그랑주_방정식)

\- [위키피디아 변분법](https://ko.wikipedia.org/wiki/변분법)

