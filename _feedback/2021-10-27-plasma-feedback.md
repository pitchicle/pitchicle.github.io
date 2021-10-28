---
layout: post
title: '고체, 액체, 기체말고 또 있다고? - 플라즈마'
author: yongho.lee
comments: true
date: 2021-10-27 21:06
use_math: true
tags: [physics]
---



지구에 사는 우리들은 물질들에 둘러싸여 삶을 살아가고 있습니다. 그것은 대부분 고체, 액체, 기체의 상태를 이루고 있을 것입니다. 아래의 그림과 같이 고체는 분자끼리의 상호작용이 강하여 모양을 유지하고 일정한 부피를 가지고 있습니다. 액체는 고체보다는 분자 사이의 상호작용이 약해서 담는 부피에 따라 모양이 달라지지만 일정한 부피를 가지고 있습니다. 기체는 분자 사이의 힘이 너무 약해서 담는 부피에 따라 모양이 달라지고 부피 또한 달라집니다. 우리는 주변에서 고체, 액체, 기체를 자주 보고 살기 때문에 다른 물질의 상태는 잘 생각하지 않게 됩니다. 하지만 정말로 물질의 상태는 고체, 액체, 기체밖에 없을까요? 

### 제 4의 상태, 플라즈마

![플라즈마 볼](https://user-images.githubusercontent.com/77658570/139059864-e88b71be-8742-44ed-81f2-27cc3f112632.png)

과학에 관심 있는 학생 또는 독자라면 위의 그림과 같은 `플라즈마 볼`을 본 적이 있을겁니다. 손을 대면 그쪽으로 따라오는게 정말 신기하고 그냥 가만히 놔두어도 선들이 움직이는 것을 보면 과학의 신비함에 놀라곤 합니다. 각설하고, 여러분들은 이 신기한 교육 기구의 이름에 있는 `플라즈마`가 고체, 액체, 기체가 아닌 제 4의 상태라고 불리는 것을 아셨나요? 이 글에서는 플라즈마의 정의, 성질, 특징에 대해 알아보려고 합니다.

<div style="text-align:center">
    <img src="https://user-images.githubusercontent.com/77658570/139059992-2b063a8e-1c5d-43f3-8483-30f10464aced.png" style="zoom: 50%;" />
    <p>
        제 4의 상태, 플라즈마
    </p>
</div>

플라즈마를 간단하게 표현하자면 위의 그림과 같이 원자핵과 전자가 분리되어 있는 기체입니다. 하지만 우리가 사는 세상의 기체에도 분자 간 충돌로 인하여 잠시나마 원자핵과 전자가 분리되어 있는 기체가 있을 것입니다. 이런 것들을 플라즈마라고 부르지는 않는데요, 과학자들은 플라즈마의 정의를 좀 더 과학적으로 접근하여 다음과 같은 두 가지의 특성을 지니는 상태일 때 이 상태를 `플라즈마`라고 부르기로 했습니다.



> *A plasma is a* **quasi-neutral** *gas of charged and neutral particles which exhibits* **collective behavior**.



처음부터 어려운 단어를 마주했습니다. 차근차근 단어의 뜻과 이것이 왜 플라즈마의 정의인지 알아보겠습니다. 먼저 quasi–neutrality, 준 중성 상태는 무엇일까요? 그냥 중성도 아니고 준 중성 상태라니요? 여기서 말하는 중성은 (+), (-)가 없는 그 중성 맞습니다! 하지만 앞서 말했던 것처럼 플라즈마에서는 원자핵과 전자가 분리되어 있습니다.(정확하게는 전하를 가진 입자와 전하를 가지지 않은 입자 또한 있습니다.) 국소적으로 관찰했을 때 플라즈마는 +와 –를 가진 극을 띄는 상태입니다. 하지만 전체적으로 보았을 때는 원자핵과 전자의 전하량의 합이 0으로 수렴하고 이런 상태가 ‘마치 중성과 같다’라고 하여 우리는 이러한 상태를 ‘quasi-neutrality, 준 중성 상태’라고 말합니다.

collective behavior를 직역하면 집단적 움직임입니다. 플라즈마는 겉으로 보기에는 준 중성 상태를 만족하고 있지만 국소적으로 볼 때는 각각의 입자들이 전하를 가지고 있기 때문에 각각의 입자들이 자기장과 전기장과 상호작용하여 움직입니다. 이러한 움직임을 집단적 움직임이라고 표현합니다. 앞서 말씀드린 두 가지의 특징을 가지고 있을 때 이를 플라즈마라고 정의합니다.



---



### 플라즈마 정의에 대한 정량적 해석

사실 말씀드린 내용이 정성적인 내용이라 깊이있는 이해를 원하시는 독자님들께 설명이 충분하지 못할 것입니다. 우리는 Debye shielding (디바이 차폐)에 관한 사고실험을 통해 좀 더 정량적으로, 자세히 이해해보려고 합니다. 풀이 과정에서 맥스웰 방정식, Taylor Series, 2 order ODE의 풀이가 필요하기 때문에 필요한 분들만 읽으시면 될 것 같습니다.

<div style="text-align:center">
    <img src="https://user-images.githubusercontent.com/77658570/139060097-d8d084ee-cc77-423b-a81f-3d6595013969.png" style="zoom:80%;" />
    <p>
        디바이 차폐
    </p>
</div>

위의 그림은 균일한 플라즈마 내에 점전하가 들어있는 모습을 나타낸 것입니다. 먼저 디바이 차폐 사고실험 및 식 유도를 진행하기 전에 몇 가지의 가정을 하고 시작하겠습니다.



\- 1 dimension : 편리한 계산을 위해서 x축만 고려 (그레디언트를 미분으로 표현 가능).

\- hydrogen plasma : ion과 electron이 같은 개수.

\- Steady-State : 충분한 시간이 지난 후 Steady-State에 도달했을 때로 가정.

\- : 이온의 질량이 전자의 질량보다 훨씬 커서 이온은 움직이지 않음.



전기 퍼텐셜을 계산하기 위해 맥스웰 방정식 중 가우스 법칙을 푸아송 방정식으로 바꾸어 표현합니다.


$$
\nabla\cdot\vec{D} = \sigma \\
\nabla\cdot\vec{E} = {\sigma\over\epsilon_0} \\
\vec{E} = -\nabla\phi \\
-\epsilon_0\nabla^2\phi = \sigma
$$
이를 첫 번째 가정을 이용하여 아래와 같은 식으로 정리해줍니다.


$$
{d^2\phi\over dx^2} = -{1\over\epsilon_0}(en_i-en_e)
\text{ (}n_i\text{는 ion density, }n_e\text{는 electron density})
$$


이때 $\sigma$는 전하 밀도이므로 $e$만큼의 전하량을 가진 ion과 $-e$만큼의 전하량을 가진 전자의 전하 밀도를 더하여 나타냅니다. 무한대에 있는 입자들의 밀도를 이라고 할 때 네 번째 가정에 의하여


$$
n_i=n\text{, } n_c=n\exp\left({e\phi\over kT_c}\right) \text{ (Boltzmann Distribution function)}
$$


 으로 나타낼 수 있습니다. 이 두 개의 밀도를 위의 미분방정식에 넣어 풀이해야 하는데 식이 너무 복잡합니다. $\exp(x)$의 Taylor series를 통해 식을 간편하게 만들 것입니다. ($\exp(x)$는 $e^x$입니다.)


$$
e^x=1+x+{x^2\over2}+\cdots \text{ (}|x|<1\text{)}
$$


이를 위의 전자의 밀도에 적용하면 다음과 같이 쓸 수 있습니다. 


$$
n_c = n\exp\left({e\phi\over kT_c}\right)\approx n\left(1+{e\phi \over kT_c} + \cdots \right) (\because \left|{e\phi\over kT_c}\right|\ll1)
$$


두 번째 범위를 나타내는 부등식은 전기 퍼텐셜 에너지보다 운동에너지의 값이 더 큰 것을 의미합니다. 즉, 운동에너지가 전기 퍼텐셜 에너지보다 클 때 위와 같이 나타낼 수 있습니다. 이제 $n_i$, $n_e$를 위의 푸아송 방정식에 대입하여 풀어보겠습니다.


$$
{d^2\phi\over dx^2} = {e\over\epsilon_0}(n_c-n_i) = {e\over\epsilon_0}\left(n+{ne\phi\over kT_c} - n\right) = {ne^2\over\epsilon_0kT_c}\phi
$$


이후 디바이 길이를 정의하여 대입합니다. $\lambda_D = \sqrt{\epsilon_0kT_c\over ne^2}$이라고 하면


$$
{d^2\phi\over dx^2} = {1\over{\lambda_D}^2}\phi \\
\phi = C_1e^{-{|x|\over\lambda_D}}+C_2e^{|x|\over\lambda_D}
$$


여기에서 초기 조건 두 가지를 정의하여 식에 대입하면 다음과 같이 정리할 수 있습니다. 
$$
x=0, \phi=\phi_0 \\
x\rightarrow\infty, \phi=0 \\
\phi=\phi_0e^{-{|x|\over\lambda_D}}
$$


이를 좌표평면 위에 나타내면 다음과 같은 개형을 나타냅니다. 



<div style="text-align:center">
    <img src="https://user-images.githubusercontent.com/77658570/139060863-091cde19-4a6d-44b8-a93e-055dbcbee480.png" style="zoom:50%;" />
    <p>
        플라즈마 전위 분포
    </p>
</div>

여기에서 $x=0$에서의 전기 퍼텐셜의 $1\over e$배가 되는 지점을 $\lambda_D$, Debye length라고 합니다.



##### 참고 자료

[1] [서울대 나용수교수님] 플라즈마 기초 2강 Introduction 2 Definition of Plasma, "[https://www.youtube.com/watch?v=3QKeV9H4_cg](https://www.youtube.com/watch?v=3QKeV9H4_cg)", Youtube

[2] Boas 수리물리학 개정 3판





##### 이미지 출처

[Title] State of matter, "[https://en.wikipedia.org/wiki/State_of_matter](https://en.wikipedia.org/wiki/State_of_matter)", wikipedia

[a] Phase of matter, "[https://www.grc.nasa.gov/WWW/K-12/airplane/state.html](https://www.grc.nasa.gov/WWW/K-12/airplane/state.html)", NASA

[b] Plasma ball, "[https://www.menkind.co.uk/red5-5-plasma-ball](https://www.menkind.co.uk/red5-5-plasma-ball)", Menkind

[c] Plasma basics, "[http://gaotontech.com/plasma-basics/](http://gaotontech.com/plasma-basics/)", gaotontech

[d] 디바이 차폐(Debye Shielding), "[https://marriott.tistory.com/58](https://marriott.tistory.com/58)", 개날연 블로그
