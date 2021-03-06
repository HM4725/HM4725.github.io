﻿---
layout: post
title: 1장. Artificial Intelligence
category: Machine Learning
tags: [Artificial Intelligence]
---

# 1. Definition
> 인간의 지능을 갖고 있는 기능을 갖춘 컴퓨터 시스템이며, 인간의 지능을 기계 등에 인공적으로 시연(구현)한 것이다.

위키피디아 [1]에는 인공지능이 위와 같이 정의되어 있다. 컴퓨터가 인간의 지능을 흉내낼 수 있으면, 인공지능이라고 부르는 것 같다.

> I propose to consider the question, "Can machines think?" This should begin with definitions of the meaning of the terms "machine" and "think."

앨런 튜링의 COMPUTING MACHINERY AND INTELLIGENCE [2]의 첫부분에 위와 같은 문구가 나온다. 튜링은 인공지능을 "기계"와 "생각" 두 가지 관점으로 생각을 하였고, 위 인용부분 이후엔 이에 대한 자신의 생각을 서술한다.

위 두가지 인용구를 정리해보면, 컴퓨터가 사람처럼 생각을 할 수 있을 때 이 컴퓨터를 인공지능이라고 부를 수 있을 것으로 보인다.

---

# 2. AI types
사람처럼 생각하는 컴퓨터를 인공지능이라고 한다는데, 그 정의가 너무 광범위하고 모호하게 보인다. 인공지능을 여러 기준에 따라 나누어 다시 살펴보자.
## 2.1. Criterion 1: Cognitive Capacities
AI를 인지 능력이라는 기준으로 분류한다면, 약인공지능과 강인공지능으로 나눌 수 있다 [3].

### 2.1.1. 약인공지능 (Weak AI)
약인공지능은 한가지 생각만 할 수 있는 인공지능을 의미한다. 예를 들어서 설명하면 이해하기 편하다.
요즘 유튜브를 보다 보면, *"BTS bring me here"* 과 같은 재미있는 댓글들을 볼 수 있다. 이런 댓글들은 유튜브 **다음 동영상** 이나 **맞춤 동영상** 에 자주 뜨는 영상에 많이 달린다. 사람들은 이를 유튜브 알고리즘이라고 부른다. 사실 이 알고리즘도 인공지능에 기반을 두고 있다. 이 인공지능은 **사용자 맞춤형 영상 추천** 이라는 한가지 역할을 기가막히게 잘한다. 사람만이 할 수 있다고 믿었던 *"이 영상 한번 봐봐!"* 를 컴퓨터가 하고 있는 것이다.
하지만 유튜브 영상 추천 알고리즘은 영상을 만들거나, 소리를 듣고 자막을 달아주지 못한다. **영상 추천** 한가지 기능만 기가막히게 잘하는 것이다. 이와 같이 한가지 문제를 기가막히게 잘 풀어내는 인공지능을 약인공지능이라고 한다.

### 2.1.2. 강인공지능 (Strong AI)
반대로 강인공지능는 진짜 사람처럼 여러가지 역할을 할 수 있는 인공지능을 뜻한다. 현재 필자는 커피를 마시며, 노트북 화면을 보고, 키보드를 치며, 이 글을 쓰고 있다. 한번에 여러가지 일을 하고 있는 것이다. 만약 인공지능이 진짜 사람처럼 범용적으로 생각하고 여러 기능을 할 수 있다면, 강인공지능이라고 부를 수 있을 것이다.

## 2.2. Criterion 2: Control
제어라는 관점에서 보면, Rule-based Systems와 Learning Systems로 나눌 수 있다 [4]. 인공지능의 역사를 살펴보면, 많은 과학자들이 Rule-based Systems와 Learning Systems로 갈라져 싸워왔다.
### 2.2.1. Rule-based Systems
if-then-else문으로 이루어진 인공지능이다. 모든 규칙을 프로그래밍화한다. 즉, 프로그래머가 제어할 수 있는 인공지능을 의미한다. 선천적으로 똑똑한 사람과 비슷한 인공지능이라고 생각하면 편하다.

영상의학 분야의 예를 들어보자.
영상의학과 의사는 다리가 아픈 환자의 엑스레이 사진이나 초음파 영상을 본다. 지방질과 근육 사이에 근막이 존재한다. 하지만 환자의 사진엔 근막이 있어야할 곳이 끊어져있고, 하얀 근육 부분이 지방질의 영역을 침범하고 있다. 이를 if-then-else문으로 프로그래밍하면 다음과 같다.
```
if [다리가 아픔]: then
  if [근막이 끊어져있다]: then
    if [끊어진 근막 사이로 둥글게 근육이 튀어나와있다]: then
      ["근막통증증후군"으로 판정]
    else:
      ...
  else:
    ...
else:
  ...
```
이처럼 모든 경우를 프로그래밍하는 인공지능 시스템을 Rule-based Systems이라고 한다.
+ **장점**
1. 프로그래머가 제어하기 쉽다.

+ **단점**
1. 경우의 수가 늘어나면, 프로그래머가 제어하기 어려워진다.
2. 규칙을 규정하기 어려운 경우, 만들 수 없다.

### 2.2.2. Learning Systems
그 유명한 Machine Learning이 이에 속한다. 컴퓨터가 데이터를 통해 학습을 하고, 이후 학습된 컴퓨터는 사람처럼 생각을 하는 것이다. 후천적으로 똑똑해지는 사람과 비슷한 인공지능이라고 생각하면 편하다.

Rule-based Systems처럼 영상의학 분야의 예를 이용하여 Learning-based로 프로그래밍하면 다음과 같다.
```
dataset := [many xray images]
model := [learning model]
model.train(dataset)

patient := [xray.png]
result := model.diagnose(patient)
```
이에 관한 자세한 내용은 2장. Machine Learning에서 살펴보기로 하자.

+ **장점**
1. 규칙을 규정하기 어렵더라도, 만들 수 있다.
2. 기계 스스로 판단할 수 있다.

+ **단점**
1. 제어하기 어렵다. (Black box)
2. 수학적 지식이 필요하다.

---

# 3. Problems
인공지능은 여타 분야와 마찬가지로 여러 문제를 직면하고 있다.
## 3.1. 인공지능 개념 자체의 모호함
1950년대 여러 과학자들은 기계가 스스로 생각을 할 수 있을 때, 이를 인공지능이라고 하자고 했다. 사실 이는 컴퓨터 과학적 접근이라기 보다는 심리학적 접근이였다. 인공적인 두뇌의 가능성을 논의함에 따라 인공지능이 학문 분야로 들어선 것이다. 그래서인지 과거의 인공지능 개념은 현대의 컴퓨터 과학과는 잘 맞지 않는다.

현대의 인공지능은 **생각** 보다는 **문제 해결** 에 더 가깝다. 유튜브 알고리즘도 사람처럼 생각한다기보다는 영상 추천이라는 기능을 잘 해낸다. 영상 추천이라는 문제를 해결하는 것이다.

그런데 프로그래밍을 해본 사람이라면, 이상한 점을 느낄 것이다. OS는 "하드웨어를 제어"라는 문제를 해결하는 프로그램이고, DBMS는 "데이터를 관리"라는 문제를 해결하는 프로그램이다. 이 둘은 매우 복잡하지만, 인공지능과는 거리가 멀어보인다. 백번 양보해서 두 프로그램을 Rule-based System의 인공지능이라고 해보자. 그렇다면 사실상 모든 컴퓨터는 인공지능이 된다. 실제로 Rule-based System은 인공지능이 아니라는 의견도 많이 있다.

## 3.2. 인공지능의 구현 방향
사람이 하는 일을 Rule-based로만 흉내내는 것은 불가능하다. 사람의 모든 행동을 규칙만으로 설명할 수 있다면, 내 다음 행동도 규칙에 의거하여 예측이 가능해질 것이다. 하지만 사람의 미래를 예측하기는 어렵다. 그래서 요즘 Machine Learning이 뜨는 것이다. 기존의 Rule-based로 해결하지 못한 문제들을 해결할 수 있게 되었기 때문이다.

하지만 다수의 인공지능 회사들은 Machine Learning을 맹신하고 있다. 즉, 모든 것을 Machine Learning으로 해결하려는 기업들이 굉장히 많이 있다. 현재 네이버 클로바의 경우, Learning System을 이용한다. 네이버는 수학적으로 제어를 하기보단, 자본력을 바탕으로 수많은 실험을 하는 것으로 알고 있다. 프로그래머가 제어하기보단 학습된 기계가 문제를 해결해주기를 바라는 심정으로 실험을 하는 것이다. 이는 마치 중세 유럽의 연금술을 보는 듯하다. Black box의 내부를 철저하게 분석하고 그 원리를 알아내려고 하지 않는다. *"그냥 해보니까 우연히 되네"* 하는 심보이다. 필자는 이런 실태가 굉장히 안타깝다.

그래서 올바르게 인공지능을 구현하는 방향을 두 가지 예시를 통해 제안한다. 그 예는 AlphaGo와 Inverse Autoregressive Flow이다.

먼저 Google DeepMind의 AlphaGo [5]는 먼저 Rule-based로 프로그래밍하려고 했다. 그런데 바둑의 경우 돌을 놓는 경우의 수 (250^150)가 너무 크기 때문에 Rule-based로만 프로그래밍을 할 수 없었다. 그래서 그 유명한 **시간복잡도** 를 낮추기 위해 확률분포를 모델링하는 Machine Learing을 도입한 것이다.

필자가 좋아하는 인공지능의 대가 [King ma](https://scholar.google.nl/citations?user=yyIoQu4AAAAJ&hl=en) 선생님의 Improved Variational Inference with Inverse Autoregressive Flow [6]를 살펴보면, 자코비안 행렬의 역행렬을 구하는 부분이 나온다. 역행렬 계산의 시간복잡도는 O(N^3)이다. King ma 선생님은 이 부분을 특정 조건 하의 Machine Learning을 통해 O(N)까지 낮추었다.

정리하자면, 처음부터 아무 이유없이 Learning System을 채택하기보다는 먼저 Rule-based로 접근을 해보고, Rule-based보다 Machine Learning의 시간복잡도가 더 낮을 때 Mechine Learning을 선택해야 한다.

## 3.3. 강인공지능
사람의 신경계도 완벽하게 파악하지는 못한 지금, 강인공지능을 구현하는 것은 넌센스이다. 과연 사람같은 강인공지능을 만들어 낼 수 있을지도 의문이다. 나중에 기술력이 굉장히 발전해서 강인공지능을 만들 수 있게 되더라도, 큰 문제가 발생한다. 만약 인공지능이 자아를 갖고 자유의지를 행할 수 있게 된다면, 이 인공지능을 사람처럼 인정해주어야하냐 하는 문제가 발생한다. 또한 엘론 머스크가 경고한 것처럼 초지능을 갖는 인공지능이 독재자처럼 행동할 수도 있다.

다행 중 다행인 것은 아직까진 강인공지능이 구현되기는 멀어 보인다는 것이다. Siri, 빅스비, OkGoogle은 소리를 인식하고 이를 처리하고 다시 말을 해준다. 어떻게 보면, 강인공지능처럼 보인다. 하지만 아직까지는 소리를 인식하는 약인공지능, 이를 처리하는 약인공지능, 말을 하는 약인공지능의 조합일 뿐이다.

---

# 4. References
> [1][https://ko.wikipedia.org/wiki/%EC%9D%B8%EA%B3%B5%EC%A7%80%EB%8A%A5](https://ko.wikipedia.org/wiki/%EC%9D%B8%EA%B3%B5%EC%A7%80%EB%8A%A5)
[2][https://www.csee.umbc.edu/courses/471/papers/turing.pdf](https://www.csee.umbc.edu/courses/471/papers/turing.pdf)
[3][http://cogprints.org/7150/1/10.1.1.83.5248.pdf](http://cogprints.org/7150/1/10.1.1.83.5248.pdf)
[4][https://www.tricentis.com/artificial-intelligence-software-testing/ai-approaches-rule-based-testing-vs-learning/](https://www.tricentis.com/artificial-intelligence-software-testing/ai-approaches-rule-based-testing-vs-learning/)
[5][http://airesearch.com/wp-content/uploads/2016/01/deepmind-mastering-go.pdf](http://airesearch.com/wp-content/uploads/2016/01/deepmind-mastering-go.pdf)
[6][https://arxiv.org/abs/1606.04934](https://arxiv.org/abs/1606.04934)
