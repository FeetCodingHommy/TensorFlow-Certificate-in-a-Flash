# 2. Image Classification w/ ConvNets

* [DeepLearning.AI TensorFlow Developer Professional Certificate](https://www.coursera.org/professional-certificates/tensorflow-in-practice)
  * Course 1 [Introduction to TensorFlow for Artificial Intelligence, Machine Learning, and Deep Learning](https://www.coursera.org/learn/introduction-tensorflow?specialization=tensorflow-in-practice)
    * Week 03 Enhancing Vision with Convolutional Neural Networks
    * Week 04 Using Real-world Images
  * Course 2 [Convolutional Neural Networks in TensorFlow](https://www.coursera.org/learn/convolutional-neural-networks-tensorflow?specialization=tensorflow-in-practice)
    * Week 05 Exploring a Larger Dataset

---



## Coursera 강의 내용 요약

### Week 3 CNN으로 컴퓨터 비젼 개선

```python
import tensorflow as tf
from tensorflow import keras
import numpy as np
# ===== 아래는 시각화 및 예제 데이터 =====
import matplotlib.pyplot as plt
import cv2
from scipy import misc
```

#### 해당 주차 개념

* **Convolutional Neural Network**의 특징
* **Convolution** Layer와 **Pooling** Layer의 역할과 각 레이어들을 통과한 데이터 전후 특징
  * custom convolution filter로 알아보는 CNN에서 데이터의 인지(?) 과정[[강좌 보조 자료](https://lodev.org/cgtutor/filtering.html)]

★ convolution  layer[\(Conv2D\)[다큐먼트](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Conv2D)]\( - filters, kernel_size, activation, input_shape\), pooling layer[[다큐먼트](https://www.tensorflow.org/api_docs/python/tf/keras/layers/MaxPool2D)]하기(- pool_size)

#### 해당 주차 실습 내용 요약

* [Fasion MNIST](https://github.com/zalandoresearch/fashion-mnist) 데이터셋 (28x28, 1 channel(grayscale), train 60,000 / test 10,000) 사용

* 이미지 데이터를 CNN으로 분류하는 과정

  : Keras API의 예제 데이터셋 Load 불러오기 → (Train-Test Split 과정에서 자동 Labeling)

  → 전처리 (이미지 데이터의 Nomalization 정규화 (0~255 값들을 255로 나눠주기)) 

  → Sequential 순차적 신경망에 **Convolution**, **Pooling**, Dense Layer 쌓기 

  → **Loss Function** 손실 함수(**"sparse_categorical_crossentropy"**)와 **Optimizer** 최적화 함수(```tf.optimizers.Adam()```) 결정 

  → 구축한 신경망에 데이터 입력 후 모델 Fit 피팅

  → Evaluation **Metrics 평가 지표**(Accuracy 정확도)를 통해 Convergence 학습 수렴 확인

#### Coursera 강의 강사 공식 자료

* Course 1 - Part 6 - Lesson 2: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%206%20-%20Lesson%202%20-%20Notebook.ipynb)
* Course 1 - Part 6 - Lesson 3: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%206%20-%20Lesson%203%20-%20Notebook.ipynb)



### Week 4 현실의 데이터를 맞춰보자

#### 해당 주차 개념

* 

#### 해당 주차 실습 내용 요약

* 

#### Coursera 강의 강사 공식 자료

* Course 1 - Part 8 - Lesson 2: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%208%20-%20Lesson%202%20-%20Notebook.ipynb)
* Course 1 - Part 8 - Lesson 3: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%208%20-%20Lesson%203%20-%20Notebook.ipynb)
* Course 1 - Part 8 - Lesson 4: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%201%20-%20Part%208%20-%20Lesson%204%20-%20Notebook.ipynb)



### Week 5 더 거대한 데이터셋

#### 해당 주차 개념

* 

#### 해당 주차 실습 내용 요약

* 

#### Coursera 강의 강사 공식 자료

* Course 2 - Part 2 - Lesson 2: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lmoroney/dlaicourse/blob/master/Course%202%20-%20Part%202%20-%20Lesson%202%20-%20Notebook.ipynb)

