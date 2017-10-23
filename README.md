## Inception network with prettytensor(Cifar10)
**이 튜토리얼은 텐서플로우의 모듈 중에 하나인 prettytensor를 이용하여, Google inception network를 cifar10 데이터셋에 맞게 약간 변형한 코드를 
작성하는데 목표를 두고 있습니다.**

**작성자는 Hvass-Lab 및 김성훈 교수님의 "모두를 위한 딥러닝" 강의를 듣고나서 이 튜토리얼을 작성하였습니다. 따라서, 코드의 일부가 겹칠 수 있고, 
위의 두 강의를 듣고 오신 분이라면 쉽게 Inception network를 빌드할 수 있을 것입니다.**

**아래의 inception network관련 사진들의 출처는 다음과 같습니다**

<https://arxiv.org/abs/1409.4842>

**궁금한 사항이나 게시물에 문제가 있을시 <first287@naver.com>으로 연락을 주시면 감사하겠습니다.**

_ _ _
### 1. 작성자 컴퓨터 사양 및 프로그램 버전
**- Cpu : intel i7 -3770**

**- Ram : 16G**

**- GPU : GTX 1080TI(Memory: 11G)**

**- OS: window 10(64bit)**

**- Tensorflow-gpu version:  1.3.0rc2**

**- Tensorflow-gpu version:  1.3.0rc2**

**- Ipython version: 6.2.0**

_ _ _
### 2. 모델에 대한 간단한 설명
**Inception network는 아래 사진에서 볼 있는 Previous layer가 4개의 분기로 나누어진 후, 나중에 다시 합쳐지게 되는 inception module을 기본으로 합니다.**
![모듈](https://github.com/MINGUKKANG/Inception_net_prettytensor/blob/master/images/inception_module.PNG)

_ _ _
**Inception network를 소개한 논문 Go deeper with convolutions에서는 input_size로 (None,224,224,3)크기의 이미지를 사용했지만, cifar10의 경우 (None,32,32,3)크기의 이미지를 사용하므로 network를 약간 수정하였습니다. 수정한 network의 구조는 아래와 같습니다.**
![테이블](https://github.com/MINGUKKANG/Inception_net_prettytensor/blob/master/images/model_table.PNG)

_ _ _
### 3. 모델의 Accuracy 및 Cost 변화 추의(Tensorboard 활용)
![이미지1](https://github.com/MINGUKKANG/Inception_net_prettytensor/blob/master/images/Accuracy_train.PNG)
![이미지2](https://github.com/MINGUKKANG/Inception_net_prettytensor/blob/master/images/cost.PNG)

_ _ _
### 4. Confusion matrix
![Confusion](https://github.com/MINGUKKANG/Inception_net_prettytensor/blob/master/images/confusion%20matrix.PNG)
_ _ _
### 5. 논문 Go deeper with convolutions에서 사용한 모델의 모습

**출처는 다음과 같습니다.  <https://arxiv.org/abs/1409.4842>**

![모델](https://github.com/MINGUKKANG/Inception_net_prettytensor/blob/master/images/inception_network.jpg)
