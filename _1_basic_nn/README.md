# 1. Basic NeuralNets

* [DeepLearning.AI TensorFlow Developer Professional Certificate](https://www.coursera.org/professional-certificates/tensorflow-in-practice)
  * Course 1 [Introduction to TensorFlow for Artificial Intelligence, Machine Learning, and Deep Learning](https://www.coursera.org/learn/introduction-tensorflow?specialization=tensorflow-in-practice)
    * Week 1 A New Programming Paradigm
    * Week 2 Introduction to Computer Vision

---



## Coursera 강의 내용 요약

### Week 1 새로운 프로그래밍 패러다임

```python
import tensorflow as tf
from tensorflow import keras
import numpy as np
```

#### 해당 주차 개념

* **기계학습**이란 무엇인가? 개념 설명
* **Neuron**(Perceptron)과 Neural Network 신경망
  * **Dense** Layer (=Fully-Connected Layer)가 대략 3층 이상 쌓이면 "Deep" Neural Network
* ★ dense layer[[다큐먼트](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Dense)]\( - units, input shape\), 모델 compile[[다큐먼트](https://www.tensorflow.org/api_docs/python/tf/keras/Model#compile)]하기(- loss function, optimizer)

#### 해당 주차 실습 내용 요약

* 간단한 수리 문제 기계학습으로 풀어보기
  : 독립변수 x와 종속변수 y 준비
  → **Sequential** 순차적 신경망에 **Dense Layer** 추가
  → **Loss Function** 손실 함수(**"mean_squared_error"**)와 **Optimizer** 최적화 함수(**"sgd"**) 결정 
  → 구축한 신경망에 데이터 입력 후 모델 **Fit** 피팅 
  → (평가지표 통한 **Convergence** 학습 수렴 확인 생략)
  → Unseen data 학습에 사용되지 않은 데이터를 통해 모델 성능 확인

#### Coursera 강의 강사 공식 자료

* Course 1 - Part 2 - Lesson 2: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%202%20-%20Lesson%202%20-%20Notebook.ipynb)



### Week 2 컴퓨터 비젼 개론

```python
import tensorflow as tf
from tensorflow import keras
import numpy as np
import matplotlib.pyplot as plt
```

#### 해당 주차 개념

* 이미지 데이터를 여러 Class로 분류하는 **Multi-class Classification** 문제에 DNN 사용
* ★ activation function, epoch과 Keras API의 Callback[[다큐먼트](https://www.tensorflow.org/api_docs/python/tf/keras/callbacks/Callback)] 기능

#### 해당 주차 실습 내용 요약

* [Fasion MNIST](https://github.com/zalandoresearch/fashion-mnist) 데이터셋 (28x28, 1 channel(grayscale), train 60,000 / test 10,000) 사용
* 기계학습의 전반적인 과정
  : Keras API의 예제 데이터셋 **Load 불러오기** → (Train-Test Split 과정에서 자동 **Labeling**)
  → 전처리 (이미지 데이터의 **Nomalization 정규화** (0~255 값들을 255로 나눠주기)) 
  → **Sequential** 순차적 신경망에 **Dense Layer** 쌓기 
  → **Loss Function** 손실 함수(**"sparse_categorical_crossentropy"**)와 **Optimizer** 최적화 함수(```tf.optimizers.Adam()```) 결정 
  → 구축한 신경망에 데이터 입력 후 모델 **Fit** 피팅
  → Evaluation **Metrics 평가 지표**(Accuracy 정확도)를 통해 **Convergence 학습 수렴** 확인

#### Coursera 강의 강사 공식 자료

* Course 1 - Part 4 - Lesson 2: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%204%20-%20Lesson%202%20-%20Notebook.ipynb)
* Course 1 - Part 4 - Lesson 4: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%204%20-%20Lesson%204%20-%20Notebook.ipynb)

