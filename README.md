# Ubuntu18.04_PyTorch
PyTorch는 파이썬(Python)을 위한 오픈소스 머신 러닝 라이브러리이다.

Tensorflow의 사용자들이 주로 사용하며 GPU를 사용할 수 있기 때문에 속도가 상당히 빠르다.

PyTorch는 설치가 다른 프로그램들에 비해 설치가 간단하며 학습속도와 추론속도가 빠르고 다루기가 쉽다.

그리고 다른 파이썬 라이브러리들과의 높은 호환성을 보여주며 직관적이고 간결한 코드로 구성이 되어있다.

# 참조

- 최신 PyTorch 버전에는 CUDA와 cuDNN이 포함되어 배포가 됩니다.

- 그러므로 CUDA와 cuDNN의 다른버전을 이용하시려면 꼭 참고해주세요.

# 설치방법
[Ubuntu 18.04 Tensorflow](https://github.com/DeepAbyss-s/Ubuntu18.04_Tensorflow)를 먼저 설치를 하셨다면 anaconda가 설치가 되어 있으시니 1번의 과정은 진행을 하지 않으셔도 됩니다.
1. [Anaconda 공식홈페이지 링크](https://www.anaconda.com/products/individual#download-section)로 이동하여 가장 아래부분으로 가시면 설치를 하실 수 있는 파일이 있습니다.

64-Bit (x86) Installer 라는 이름의 파일을 받아주시면 됩니다.

단, 설치를 하기 전에 꼭 파이썬 3.7.0버전이 설치가 되어있는지를 확인 해주셔야됩니다.

파일을 받으신 폴더로 이동하여 터미널 창을 실행 시킨 후 아래의 코드로 설치를 진행을 하시면 됩니다.
> sudo sh ./Anaconda3-2019.03-Linux-x86_64.sh

2. anaconda의 설치를 완료하시면 이제 환경을 구성해야 됩니다.

터미널 창을 실행 시킨 후 아래의 코드를 입력해주셔야 됩니다.

>source ~/.bashrc

실행하였을때에 (base) 라는 코드가 앞에 보이면 그대로 진행하시면 됩니다. 

위 코드는 아나콘다의 실행환경을 구성하는 명령어입니다.

>vi ~/.bashrc

아나콘다를 사용할 수 있는 환경을 위 명령어를 통해 들어가줍니다.

만약 편집기가 실행이 되지 않으신다면 아래 코드로 편집기를 실행해줍니다.

>sudo apt install vim

편집기로 들어가셔서 가장 아래 코드부분 밑에 
>export PATH="/home/username/anaconda3/bin:$PATH"

위 내용을 입력하신후에 "ESC"키를 눌러 아래에 " : " 표시가 보일때 wq를 눌러 저장해줍니다.

>conda create -n pytorch python=3.7

위 파이썬 버전은 본인이 쓰시는 버전을 사용하시면 됩니다.

pytorch를 anaconda에서 실행을 시켜줍니다. 명령어가 쭉 나오면서 설치를 진행합니다.

>conda activate pytorch

>pip install torch torchvision

만약 위 두가지를 설치하는 도중에 오류가 발생하면 파이썬이나 우분투OS파일에 문제가 있음으로, OS를 재설치하거나 처음부터 다시 설정을 하는 것을 권장드립니다.

위 두가지 세팅이 정상적으로 구성이 되었으면 테스트를 해보아야 됩니다.

3. 터미널 창을 실행 시킨 후 아래의 코드를 입력해주셔야 됩니다.

> python

파이썬이 실행이 된다면 파이썬 3.7.0버전은 정상적으로 설치가 된 것입니다.

이제 파이썬 버전과 설치된 쿠다의 버전을 확인할 차례입니다.

PyTorch를 불러옵니다.

> import torch

설치된 PyTorch의 버전을 확인하려면 아래의 코드를 실행시켜주시면 됩니다.

> torch.__version__

'1.x.x' (x는 버전) 라고 뜰 것입니다. 

_저희는 1.4.0 버전을 설치 하였기 때문에 1.4.0버전이라고 뜹니다._

설치된 Cuda의 버전을 확인하려면 아래의 코드를 실행시켜주시면 됩니다.

> torch.version.cuda

'10.x.x' (x는 버전)

_저희는 10.1.0 버전을 이미 설치를 하였기 때문에 설치가 된 버전이 뜰 것입니다._ 

이렇게 진행이 되었다면 PyTorch의 설치는 끝입니다.

Python에서 나오시려면 ctrl 키와 Z 키를 동시에 누르면 종류가 됩니다.



For Install PyTorch
