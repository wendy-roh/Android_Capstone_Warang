# 캡스톤 설계_영상인식기반 유아학습 시스템 
## Abstract 
유아용 학습 시스템은 이미 저장되어 있는 단어만 학습하는 기존 어플리케이션과 달리 사용자가 직접 카메라를 이용하여 주변의 보이는 무한한 사물을 스스로 찍으며 학습할 수 있게 한다. 이를 구현하기 위해 주변에서 쉽게 볼 수 있는 여러 사물을 딥러닝을 이용하여 학습시켜 실시간으로 감지할 수 있게 한다. 또한 AR 기술을 이용하여 사용자와 상호 작용할 수 있는 컴퓨터 그래픽 환경을 제공해주어 시각적인 학습 효과를 준다. 학습한 단어들은 두 가지의 게임에 적용하여 복습에 대한 흥미를 이끌어 낸다. 이러한 놀이를 접목한 교육은 아이들이 공부에 흥미를 가질 수 있게 하여 자기 주도적인 학습 효과를 높일 것으로 기대한다. <br>
Keywords : Infant, learning system, object detection, AR

## 1. 서론
 현재 코로나로 인해 아이들이 유치원, 학교 등을 가지 못하게 되면서 집에서 공부하는 홈스쿨링이 주목받고 있다. 비대면 교육이 요구되는 상황에서 학교교육을 대신해서 교육을 수행할 교육방법으로 홈스쿨링을 생각하지 않을 수 없다. 즉, 홈스쿨링은 부모에 의해서 가정에서 이루어지는 교육방식으로서 코로나 시대 또는 코로나 이후의 시대에 필요한 교육형태라고 할 수 있다. 또한 오늘날은 5G(5thGeneration)시대를 맞이하여 과거와 비교할 수 없을 정도로 빨라진 데이터 통신으로 인하여 가정에서도 더 많은 다양한 교육프로그램과 콘텐츠를 제공받을 수 있게 되었다. 따라서 가정에서의 홈스쿨링에 의해서도 아동에게 필요한 교육을 효율적이고 다양하게 제공할 수 있는 교육환경이 마련되었다고 볼 수 있다. 주된 사용자의 연령층이 어린 만큼 딱딱한 학습보다는 놀이를 통해 자연스럽게 학습이 가능한 콘텐츠에 초점을 맞추어 다양한 수단이 등장하고 있다. 유아들에게는 시각, 청각, 애니메이션 자극이 민감하게 다가오기 때문에 이를 활용하면 아이들이 공부에 흥미를 가지고 나아가 학습 능력 향상에 긍정적인 영향을 준다. <br>
 시중에 있는 제품들은 모두 낱말 카드 기반의 학습을 인해 하나의 이미지로만 학습되어 단일화된 학습만 가능하나는 한계가 있다. 이 제품들과 차별성을 두기 위해 이러한 단점을 극복하려 다양화된 학습에 초점을 맞추어 주변에서 보기 쉬운 사물들은 딥러닝으로 객체 감지 학습을 시켜 사용자가 카메라 촬영을 통해 실시간으로 감지할 수 있게 한다. 또한 컴퓨터 기술의 발달로 AR과 같은 기술은 단방향 시각 자극만이 아닌 상호작용 형 그래픽 환경을 제공해 주어 학습 몰입도를 증가시킨다. 이를 이용하여 아이들의 시각적인 학습을 위해 지구, 헬리콥터 등 쉽게 보기 힘든 사물과 동물을 AR카드로 제작하고 AR에 애니메이션 효과를 적용시켜 실감나게 공부할 수 있게 한다. <br> 학습한 단어들은 카드게임과 보물찾기 게임에 적용하여 복습 또한 재미있게 할 수 있게 한다. 이러한 놀이를 접목한 교육은 아이들이 공부에 흥미를 가질 수 있게 하여 자기 주도적인 학습 효과를 높일 수 있다.
## 2. 본론
### 1. 사용기술
> 딥러닝
 * 개념 
   * 딥러닝은 사물이나 데이터를 군집화하거나 분류하는 데 사용하는 기술이다. 컴퓨터는 사진만으로 개와 고양이를 구분하지 못하지만, 사람은 쉽게 가능하다. 사람처럼 쉽게 구분할 수 있도록 하는 방법이 기계학습(Machine Learning)이며 많은 데이터를 컴퓨터에 입력하고 비슷한 것끼리 분류하도록 하는 기술이다. <br>
  딥러닝의 핵심은 분류를 통한 예측으로, 수많은 데이터 속에서 패턴을 발견해 사물을 구분하고 컴퓨터에 먼저 정보를 가르치는 방법인 지도학습과 배움의 과정이 없고 컴퓨터가 스스로 학습하는 비지도 학습으로 나뉜다.
 * Tensorfllow Lite
   * Tensorflow는 구글에서 개발한 파이썬 환경에서 딥러닝과 같은 인공지능 기법을 쉽게 구현할 수 있도록 도와주는 오픈소스 라이브러리이다. Tensorflow Lite는 Tensorflow의 경량화 버전으로, 휴대기기, 내장형 기기 및 IoT 기기 등 모바일 환경에서 구동하도록 해준다. 때문에 Tensorflow PC에서 모델을 학습시킨 후에 Tensorflow Lite에 적용한다.
 * 기술 적용
   * Tensorflow Lite 기술은 주변의 객체를 실시간으로 인식하기 위해서 사용한다. COCO dataset에서 다운받은 ssd_mobilenet_v2_quantized 모델을 기반으로 객체를 라벨링하여 학습시킨다. 학습시킨 데이터를 모바일에서 사용하기 위해 tflite파일로 변환하여 어플에 적용한다. <br>
주변 사물의 사진을 찍어서 객체 이름의 한글과 영어를 보여주는 학습을 위해 사용된다. 인식된 객체의 이름은 문자로만 보여주지 않고 음성으로 들려주는 기술을 더해서 학습이 가능하다. <br>
사용자가 주변 사물을 찍은 사진으로 학습을 한 후에  복습 또한 게임을 통해 할 수 있게 한다. 핸드폰으로 찍은 사진은 기기의 내부저장소에 저장하여 게임을 실행할 때 사용하는데, 내부저장소는 다른 앱에서 내부저장소의 위치에 액세스하는 것을 방지하기 때문에 사용자별로 학습 사진을 저장할 수 있어서 사용한다.<br>
내부저장소에 저장된 사진을 이용해 객체의 사진과 객체의 이름을 연결하는 카드게임과 객체의 이름을 랜덤으로 띄워주면 알맞은 주변의 사물을 찾는 보물게임이 있다. 
> AR
 * 개념 
   * AR은 Augmented Reality의 약자로 실제세계와 현실세계에 기반한 가상의 세계를 동시에 혼합하여 보여주는 기술이다. 즉, 실시간으로 사용자와 상호작용하는 동안 3차원의 움직이는 화면과 다양한 영상, 음향효과를 제공하여 현실과 유사한 또 다른 현실을 창조함으로써 감각을 확장시키고 더 높은 몰입감과 현실감을 제공한다.
 * Unity와 Vuforia 
   *  Unity는 3D 및 2D 비디오 게임의 개발 환경을 제공하는 게임엔진이면서 3D 애니메이션, 건축 시각화, 가상현실 등 반응형 콘텐츠 제작을 위한 통합 저작 도구이다. <br>
Vuforia는 증강현실 어플리케이션을 생성할 수 있는 모바일 장치 용 증강현실 소프트웨어 개발 키트이다.
 * 기술적용 
   * 마커 인식을 하기 위해서 낱말카드를 제작한다. 마커는 동물, 탈것, 계절나무, 행성의 카테고리로 구성했고, 카드의 색깔을 다르게 하여 구분한다. 카드의 앞면에는 사물의 사진과 단어를 넣고, 뒷면에는 제작한 마커를 넣는다. 마커는 인식률을 높이기 위해 직선을 이용한 특정패턴과 단어의 초성을 넣어 제작한다. <br> 제작한 마커를 Unity에 불러오기 위해서 Vuforia에 package를 다운로드 받고 적용시킨다. 이후 Vuforia에 License Manager에서 키를 등록하고, Target Manager에서 제작한 마커를 등록한다. 등록한 마커를 다운로드받아 Unity에 등록하면 마커가 준비된다. Unity에 AR Camera를 추가하여 앞에서 생성했던 key를 넣어주고, Image Target을 추가하여 등록했던 마커를 넣어준다. 마커위에 3D 객체를 띄우기 위해 Asset Store에서 무료 asset을 다운받아 Unity에 추가한 후, 에셋을 Image Target위로 불러오면 마커를 인식하여 3D객체를 볼 수 있게 된다. <br> 화면을 터치했을 때 애니메이션을 동작하도록 하기 위해서는 Unity에 Animator를 생성하여 실행시킬 애니메이션을 추가하고 애니메이션끼리 transition을 추가하여 서로 연결을 시킨다. 그리고 Animator에 파라미터를 추가하여 터치했을 때 실행될 애니메이션에 파라미터를 true로 하고, 터치하지 않았을 때 실행될 기본 애니메이션에 파라미터를 false로 하고 script를 작성한다.
   * 제작한 마커의 모습은 다음과 같다. <img src="https://user-images.githubusercontent.com/62936197/152630567-5c071ff9-6a1f-43d7-bb7c-baa96f876f45.png" width="250" height="80"> 
> TTS(Text To Speech) 및 STT(Speech To Text)
 * 개념 
   * TTS란 글자, 문장, 숫자, 기호 등을 사람이 일반적으로 발성하는 청각 정보로 변환하는 것이며, 문장을 입력하면 인공지능이 사람의 음성으로 변환해 주는 음성합성기술이다. STT는 TTS와 반대로 음성을 글자, 문장, 숫자, 기호 등으로 변환하는 것을 말한다. STT 모델은 사람이 말하는 음성 언어를 컴퓨터가 해석하고 그 내용을 문자 데이터로 전환하는 방식이기 때문에 음성인식이라고도 한다.
 * 기술 적용
   * TTS와 STT를 이용하기 위해 Android Studio에서 내장 API로 제공하는 Google의 TTS와 STT 기술을 사용하는데, 별도의 설치 없이 권한 부여 후 사용한다. 이러한 TTS와 STT기술을 1.1에서의 Tensorflow Lite와 연동하여 사용자의 학습을 돕는다. 이는 Tensorflow Lite를 통해 인식한 사물의 한글 및 영어단어에 대해서 사용자가 직접 말하고 듣기가 가능하여 주변사물을 통한 친숙한 학습이 가능하기 때문에 사용자의 Reading과 Speaking 능력을 증진시키는 데 도움이 된다.
### 2. 시스템 구현 화면
> 메인화면
 * ‘학습하기’, ‘게임하기’, ‘연습장 ’버튼을 눌러 각 컨텐츠를 실행 할 수 있다. <br>
   <img src="https://user-images.githubusercontent.com/62936197/152630996-af73b842-98ba-4ab3-8811-f18505605dbe.png" width="250" height="180"> <br>
> 학습모드
 * 주변 사물로 공부하기
   * 주변에서 공부하기 버튼을 누르면 그림11와 같이 초기 화면이 나온다. 카메라로 사물을 찍으면 그림12과 같이 촬영한 이미지가 뜨고 내부저장소에 저장되며 사물 이름의 한글과 영어를 띄어준다. 그림11와 그림12은 듣기모드에서의 화면이다. 그림12과 같이 TTS를 이용한 듣기 모드에서는 촬영한 사물에 대해 영어 단어 듣기를 클릭하면 영어단어를, 한글 단어 듣기 버튼을 클릭하면 한글단어를 들을 수 있다. 이 때, 말하기 모드로 전환 버튼을 누르면 말하기 모드(STT)로 전환이 된다. 아래의 사진은 말하기 모드로 전환된 화면이다. <br> <img src="https://user-images.githubusercontent.com/62936197/152631024-753ac50c-1ae9-4861-a489-c2d09246ae97.png" width="250" height="180"> <br>
   * STT를 이용한 말하기 모드로 전환 시 학습의 효율성을 위해 사물 이름을 보여주지 않고 사용자가 인식한 사물의 사진을 보고 한글 및 영어 이름을 맞추면 정답 유무와 사물 이름을 띄워주어 발음을 확인할 수 있게 한다. 사용자의 발음을 text로 변환한 후 사용자에게 보여주며, 이 text값과 인식된 사물의 이름이 동일하다면 정답처리를 해준다. <br> <img src="https://user-images.githubusercontent.com/62936197/152631027-f88af175-686b-4830-88da-f8986c080c1e.png" width="250" height="180"> <br>
 * 낱말카드 AR로 공부하기
   * 낱말카드 AR로 공부하기 버튼을 누르면 Unity가 실행이 된다. 카드뒷면에 있는 마커를 인식하면 해당 객체가 3D의 형태로 화면에 띄어지고 객체를 터치하면 애니메이션이 실행된다. <br> <img src="https://user-images.githubusercontent.com/62936197/152631087-0d4d9d16-f6ac-4b1d-9366-150e3531a499.png" width="150" height="250"> <br> 
> 연습장
 * 학습을 통해 내부저장소에 저장된 사진과 사진의 이름을 좌, 우 버튼으로 조작하여 보여준다. 화면에 보이는 사진을 보면서 이름을 따라 쓸 수 있어 사물의 이름을 반복해서 익힐 수 있고 화면에 스스로 쓰기 때문에 쓰기 능력을 키울 수 있다. 연습장 화면은 펜, 지우개, 전체 지우개 버튼으로 구성되어 있어 편리하게 쓰고 지울 수 있다. <br> <img src="https://user-images.githubusercontent.com/62936197/152631089-3583a023-5c42-4606-bc1e-2be61a9ea9d1.png" width="250" height="180"> <br>
> 게임모드
 * 카드게임
   * 선택한 카드는 빨간색 배경으로 바뀌며 선택한 사진과 이름의 짝이 맞을 경우 빨간색 배경으로 남아있고 짝이 맞지 않을 경우 흰색 배경으로 돌아온다. 4개의 짝을 모두 맞추면 다이얼로그로 게임이 끝났음을 알려주고 ‘확인’ 버튼을 누르면 게임이 초기화되어 다시 진행할 수 있게 한다. <br> <img src="https://user-images.githubusercontent.com/62936197/152631090-cdfe0055-68c7-4375-b406-c2a844531d7d.png" width="250" height="180"> <br>
 * 보물찾기
   * 보물찾기 버튼을 누르면 학습모드의 주변사물로 학습하기에서 인식한 사물들에 대해서만 보물찾기 게임을 진행할 수 있다. 게임을 시작하게 되면 그림19와 같이 내부 저장소에 저장된 이름이 랜덤으로 뜨게 되는데, 이 이름에 맞는 사물을 비추게 되면 정답 여부를 애니메이션으로 보여주며, 만약 정답일 경우 다음 랜덤 text를 자동으로 불러온다. <br> <img src="https://user-images.githubusercontent.com/62936197/152631092-6f2be744-525d-4b3f-a2dc-1c648600e4e4.png" width="250" height="180"> <br>
## 3. 결 론
* 유아는 이 시스템으로 단어의 학습과 복습을 통해 단어를 통달할 수 있는 기대효과를 불러올 수 있다. 또한 유아는 카메라를 이용하여 스스로 학습하기 때문에 자기주도 학습능력이 길러지는 기대효과를 불러올 수 있다. 언어발달 교육은 말하기, 쓰기, 듣기의 역할이 균형을 맞출 때 길러지며 이 시스템은 세 가지의 균형을 맞췄다. <br>
창의성은 문제 해결을 위해 다양한 관점에서 가능한 많은 아이디어를 생성해 내는 특성이다. 창의성과 놀이 단어의 연결정도는 높게 나타났으며 일상생활에서의 놀이 지도를 통해 창의성을 신장시킬 수 있다. 따라서 이 시스템으로 익숙한 환경에서의 학습을 통해 주변 사물과 연상하여 효과적인 단어 공부가 가능하게 하며 실제 사물뿐만 아니라 인터넷에서 찾은 사진으로도 교육 효과를 낼 수 있다. <br> 기존 어플들은 마커가 이미 만들어진 상태로 유통되어 그 마커를 이용해서만 학습이 가능하다는 한계가 있다. 그러므로 마커가 자동으로 생성된다면 더 많은 교육 컨텐츠를 만들 수 있다는 확장성이 생긴다. 학습을 마친 사물의 이미지를 사물의 이름을 파일명으로 하여 폴더로 내보내면 파일명의 첫 글자와 여러 개의 이미지를 자동으로 랜덤 배치하여 마커를 생성해낸다. 후에 이 마커에 AR 객체만 연동시켜준다면 무한한 교육 컨텐츠를 이용할 수 있다. <br> <img src="https://user-images.githubusercontent.com/62936197/152631094-1b0186d5-7271-4574-9a13-8cc2b6d7949c.png" width="250" height="150"> <br>
