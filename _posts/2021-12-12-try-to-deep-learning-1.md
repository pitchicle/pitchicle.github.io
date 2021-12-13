---
layout: post
title : '딥러닝을 쉽게 쓰려고 노력까진 했습니다 - Chapter 1. python의 기초'
author : dohyeon.lim
comments: true
date: 2021-12-12 00:01
use_math : true
tags: [computer-science]
---

# 딥러닝을 쉽게 쓰려고 노력까진 했습니다 - Chapter 1. python의 기초

이 시리즈는 ‘밑바닥부터 시작하는 딥러닝’이라는 책을 토대로 작성하였으며, 말 그대로 간단한 딥러닝을 이용한 손글씨 분석 알고리즘을 python을 통해 구현해보는 내용을 다룰 예정입니다.







 이번 시리즈에서는 python의 기초에 대해 다룰 예정입니다. 만약 python의 기초 문법과 numpy, pyplot을 사용할 줄 아신다면 이번 시리즈는 건너뛰어도 됩니다.



## 1-1. 산술연산

덧셈과 곱셈 등의 산술 연산은 다음과 같이 할 수 있습니다.

*는 곱셈, /는 나눗셈, \*\*는 거듭제곱을 의미합니다(3**2==32). python3의 경우 정수를 나눈 결과는 실수(부동소수점)가 됩니다(15/3==5.0).

![1-1](https://user-images.githubusercontent.com/76457671/145794067-f9e4d5ce-ecd4-407a-abf0-37a47de1467c.png)



## 1-2. 자료형

프로그래밍 언어에는 자료형이 있습니다. c언어를 배우셨다면 알고 계실 수도 있지만, 자료형이란 데이터의 성질을 나타내는 것으로, 정수, 실수, 문자열과 같은 형태가 있습니다. python의 경우 type() 함수를 이용해 특정 데이터의 자료형을 알아볼 수 있습니다.

![1-2](https://user-images.githubusercontent.com/76457671/145794173-820b4a59-a068-44e5-bbe7-b80252c1cb18.png)

즉, 10은 int(정수), 3.14는 float(실수), "muyaho"는 str(문자열)임을 알 수 있습니다. 또한 자료형과 class라는 말을 같은 의미로 사용하는 경우가 있는데, <class 'int'>는 "10은 int라는 클래스(자료형)다"로 해석하시면 됩니다.



## 1-3. 변수

python에서 변수는 다음의 규칙내에서 정의할 수 있습니다.

- 영문 문자와 숫자를 사용할 수 있습니다.

- 대소문자를 구분합니다.

- 문자부터 시작해야 하며 숫자부터 시작하면 안 됩니다.

- _(밑줄 문자)로 시작할 수 있습니다.

- 특수 문자(+, -, *, /, $, @, &, % 등)는 사용할 수 없습니다.

- 파이썬의 키워드(if, for, while, and, or 등)는 사용할 수 없습니다.

![1-3](https://user-images.githubusercontent.com/76457671/145794251-a0e1bc3e-eea3-4e0c-8ac8-06ca8391b1a6.png)

python의 경우 동적 언어로 분류되는 프로그래밍 언어입니다. 동적이란 변수의 자료형을 상황에 맞게 자동으로 결정한다는 뜻입니다. c언어의 경우 int x = 10과 같이 자료형을 지정해줘야 하지만, python의 경위 위의 예시처럼 x를 int(정수)라 사용자가 명시하지 않았는데도 10이라는 정수로 초기화할 때, x의 형태가 int임을 python이 스스로 판단한 것입니다. 또한 여기서 봐야할 점이 정수와 실수를 곱한 결과가 실수형으로 나왔다는 것입니다(자동 형변환). 마지막으로 #은 주석의 시작을 알리는 문자로, # 이후에 적혀있는 문자는 모두 무시해버립니다.



## 1-4. 리스트

여러 데이터를 리스트를 이용해 정리할 수 있습니다. python에서의 리스트란, c언어의 배열의 개념이라 생각하시면 이해하기 편할겁니다.

![1-4-1](https://user-images.githubusercontent.com/76457671/145794322-d29f700a-69e5-4ec8-81f1-f8fe18fa8272.png)

원소에 접근할 때에는 a[0]과 같은 방식처럼 합니다. [] 안의 수를 인덱스(색인)라 하며 인덱스는 0부터 시작합니다. 또한 python의 리스트에는 슬라이싱이라는 기법이 있습니다. 슬라이싱을 이용하면 범위를 지정해 원하는 부분 리스트를 얻을 수 있습니다.

![1-4-2](https://user-images.githubusercontent.com/76457671/145794377-dec06ac4-2933-407d-8031-4cfe1d8321f2.png)



## 1-5. 딕셔너리

리스트는 인덱스의 번호로 0, 1, 2, ... 순으로 값을 저장한다면, 딕셔너리는 key와 값을 한 쌍으로 저장합니다. 즉, 영한 사전처럼 단어와 그 의미를 짝지어 저장합니다.

![1-5](https://user-images.githubusercontent.com/76457671/145794433-3dd86257-bddf-4f0f-841e-2c5a3eec50b7.png)



## 1-6. bool

python에는 bool이라는 '자료형'이 있습니다. 이 자료형은 c언어에서와 마찬가지로 True (참)와 False (거짓)라는 두 값 중 하나를 취합니다. 또 bool에는 and, or, not 연산자를 사용할 수 있습니다(자료형에 따라 사용할 수 있는 연산자가 정해져 있습니다).

![1-6](https://user-images.githubusercontent.com/76457671/145794492-9227b90f-8a8f-4f56-8db0-d8e5a554d29c.png)



## 1-7. if 문

c언어에서도 많이 사용하던 if 조건문입니다.

![1-7](https://user-images.githubusercontent.com/76457671/145794541-ae9a7a3f-f19e-4eb2-8126-c1520ecb4e52.png)

python에서는 공백 문자(" ")가 중요한 의미를 지닙니다. 이번 if 문에서도 if school: 다음 줄은 앞에 tap 문자가 있습니다. 이 들여쓰기는 지난 조건(if school)이 충족될 때 실행되는 코드를 표현합니다. 또한 c언어에서처럼 if문의 조건이 충족이 안될 때 다른 조건의 if문을 사용하기 위해선 'else if'가 아닌 'elif' 뒤에 조건을 입력하는 방식으로 사용합니다.



## 1-8. for 문

이 또한 c언어에서도 많이 사용하던 for 반복문입니다.

![1-8](https://user-images.githubusercontent.com/76457671/145794636-1c4d6244-e3f1-4230-a355-317baa92b2c6.png)

여기서는 [1, 2, 3]이라는 리스트 안의 원소를 하나씩 출력하는 예를 보여줬습니다. for _ in _ : 구문을 사용하면 리스트 등의 데이터 집합의 각 원소에 차례로 접근할 수 있습니다.



## 1-9. 함수

특정 기능을 수행하는 일련의 명령을 묶어 하나의 함수로 정의할 수 있습니다.

![1-9-1](https://user-images.githubusercontent.com/76457671/145794683-9053ce75-15e2-416d-b74d-e4d856b1fea6.png)

함수는 인수를 취할 수 있고, + 연산자를 사용해 문자열을 이어 붙일 수 있습니다.

![1-9-2](https://user-images.githubusercontent.com/76457671/145794770-9f0e8adf-1d9f-4bed-8e9f-a3c4f0f835dd.png)



## 1-10. 넘파이(numpy)

딥러닝을 구현하다 보면 배열이나 행렬 계산이 많이 등장합니다. 넘파이의 배열 클래스인 numpy.array에는 편리한 메서드가 많이 존재해, 딥러닝을 구현할 때 이 메서드들을 이용합니다.

![1-10-0](https://user-images.githubusercontent.com/76457671/145794865-bdf1c329-65a0-4c4d-812a-e936a668b842.png)
먼저 위와 같이 넘파이 라이브러리를 가져옵니다. python에서는 라이브러리를 읽기 위해 import 문을 이용합니다. 여기에서는 import numpy as np라 했는데, 직역하면 "numpy를 np라는 이름으로 가져온다"가 됩니다. 이렇게 해두면 앞으로 넘파이를 호출할 때 np를 통해 참조할 수 있습니다.



### 1-10-1. 넘파이 배열 생성

넘파이 배열을 만들 때는 np.array() 를 이용합니다. np.array()는 python의 리스트를 인수로 받아 넘파이 라이브러리가 제공하는 특수한 형태의 배열을 반환합니다.

![1-10-1](https://user-images.githubusercontent.com/76457671/145794929-ded0934a-b7c9-4fd1-9edf-23149196bcd1.png)


### 1-10-2. 넘파이의 산술 연산

![1-10-2-1](https://user-images.githubusercontent.com/76457671/145794985-3c9c2130-ee12-4509-99f8-85979ceb820a.png)

여기서 중요한 점은 x와 y의 원소의 개수가 같다는 것입니다. 만약 원소의 개수가 다르다면 오류가 발생하니 원소의 개수 맞추기는 매우 중요합니다. 넘파이 배열은 원소별 계산뿐 아니라 넘파이 배열과 수치 하나 (스칼라값)의 조합으로 된 산술연산도 수행할 수 있습니다. 이 경우 스칼라값과의 계산이 넘파이 배열의 원소별로 한 번씩 수행됩니다. 이 기능을 **브로드캐스트**라고 합니다(브로드캐스트에 관한 자세한 내용은 1-10-4에서 다룹니다).

![1-10-2-2](https://user-images.githubusercontent.com/76457671/145795040-02a7dd9e-ac06-4b8b-b0a5-f81c1c8f7304.png)



### 1-10-3. 넘파이의 N차원 배열

넘파이는 1차원 배열뿐 아니라 다차원 배열도 작성할 수 있습니다. 예를 들어 2차원 배열(행렬)은 다음처럼 작성합니다.

![1-10-3-1](https://user-images.githubusercontent.com/76457671/145795139-826a557d-06a9-429a-87a2-3d779cd9330f.png)

위의 예시는 2x2 크기의 A라는 행렬을 작성했습니다. 행렬의 형상(크기)은 shape으로, 행렬의 담긴 원소의 자료형은 dtype으로 알 수 있습니다. 이어서 행렬의 산술 연산을 봅시다.

![1-10-3-2](https://user-images.githubusercontent.com/76457671/145795177-7fd32645-a47a-4067-95ab-d0e1cce2bc0d.png)

 형상이 같은 행렬끼리면 행렬의 산술 연산도 대응하는 원소별로 계산됩니다. 행렬또한 배열과 마찬가지로 스칼라값의 산술 연산 시 브로드캐스트 기능이 작동합니다.

![1-10-3-3](https://user-images.githubusercontent.com/76457671/145795238-f5488c04-422a-4e22-86f1-2a4c3f18f054.png)



### 1-10-4. 브로드캐스트

앞에서 계속해서 언급했던 브로드캐스트에 대해 설명해보겠습니다. 행렬이나 배열과 스칼라값을 곱할 시 스칼라값이 배연이나 행렬로 확대된 후 연산이 이뤄집니다. 이 기능을 브로드캐스트라고 합니다.

![1-10-4-1](https://user-images.githubusercontent.com/76457671/145795633-21ba4e0d-4b1a-4f68-be19-7c40a26a6674.png)

![1-10-4-2](https://user-images.githubusercontent.com/76457671/145795636-94eda8e3-235b-40d5-835b-a92fa33c3be4.png)

위와 같은 경우 1차원 배열을 2차원 배열로 늘려 연산을 진행시킵니다.

![1-10-4-3](https://user-images.githubusercontent.com/76457671/145795652-07b72ba9-5cac-4bb3-9258-b0d9af75485d.png)



### 1-10-5. 원소 접근

각 원소에 접근하기 위해선 다음과 같이합니다.

![1-10-5-1](https://user-images.githubusercontent.com/76457671/145795797-0dec3a62-06cc-4cee-9d2b-0eadea0eb0f1.png)

이 방법 외에도, 인덱스를 배열로 지정해 한 번에 여러 원소에 접근할 수도 있습니다.

![1-10-5-2](https://user-images.githubusercontent.com/76457671/145795833-397516cf-a758-4bff-8f3b-605255740482.png)

이 기법을 응용해 특정 조건을 만족하는 원소만을 얻을 수 있습니다.

![1-10-5-3](https://user-images.githubusercontent.com/76457671/145795875-88c9c622-6262-4c02-93b9-84d6d5db7765.png)



## 1-11. matplotlib

딥러닝에서는 그래프 그리기와 데이터의 시각화도 중요합니다. matplotlib은 그래프를 그려주는 라이브러리입니다. matplotlib을 사용하면 그래프 그리기와 데이터 시각화가 쉬워집니다. 이번 절에서는 그래프를 그리고 이미지를 화면에 표시하는 방법을 설명합니다.



### 1-11-1. 단순한 그래프 그리기

그래프를 그리려면 matplotlib의 pyplot 모듈을 이용합니다.

![1-11-1](https://user-images.githubusercontent.com/76457671/145796110-29df3c9a-61af-4e2e-ab8a-5f8fd6142e0a.png)

이 코드에서는 넘파이의 arange 메서드로 [0, 0.1, 0.2, ..., 5.8, 5.9]라는 데이터를 생성해 x에 할당하고, x의 각 원소에 np.sin()을 적용하여 y에 할당합니다. x와 y를 인수로 plt.plot 메서드를 호출해 그래프를 그리고, plt.show()를 호출해 그래프를 화면에 출력합니다.



### 1-11-2. pyplot의 기능

여기에 cos 함수를 추가해 보겠습니다. 또, 제목과 각 축의 이름(레이블) 표시 등, pyplot의 다른 기능도 사용해보겠습니다.

![1-11-2](https://user-images.githubusercontent.com/76457671/145796121-b75a173c-e785-4c21-aecb-8c3eeffc307a.png)



### 1-11-3. 이미지 표시하기

pyplot에는 이미지를 표시해주는 메서드인 imshow()도 준비되어 있습니다. 이미지를 읽어들일 때는 matplotlib.image 모듈의 imread() 메서드를 이용합니다.

![1-11-3](https://user-images.githubusercontent.com/76457671/145796130-5f6a2e75-0571-4b76-9273-6d8b909ec8b4.png)

선인장의 사진 파일은 프롤로그에서 말했던 https://github.com/WegraLee/deep-learning-from-scratch에서 다운받으실 수 있고, 저의 경우 선인장의 사진 파일이 '/Users/imdohyeon/Downloads/deep-learning-from-scratch-master/dataset/cactus.png'에 존재하고 있었기에 img = imread() 괄호 내부에 그 경로를 적어준 것입니다. 저 괄호 안에 여러분이 저장하신 사진 파일이 들어있는 경로를 적어주시면 됩니다.



이것으로 딥러닝을 배우기 위한 python의 기초를 알아봤습니다. 다음 시리즈에서는 퍼셉트론에 대해 알아보도록 하겠습니다. 
