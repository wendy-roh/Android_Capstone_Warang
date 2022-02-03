# 캡스톤 설계_영상인식기반 유아학습 시스템 
## Abstract 
유아용 학습 시스템은 이미 저장되어 있는 단어만 학습하는 기존 어플리케이션과 달리 사용자가 직접 카메라를 이용하여 주변의 보이는 무한한 사물을 스스로 찍으며 학습할 수 있게 한다. 이를 구현하기 위해 주변에서 쉽게 볼 수 있는 여러 사물을 딥러닝을 이용하여 학습시켜 실시간으로 감지할 수 있게 한다. 또한 AR 기술을 이용하여 사용자와 상호 작용할 수 있는 컴퓨터 그래픽 환경을 제공해주어 시각적인 학습 효과를 준다. 학습한 단어들은 두 가지의 게임에 적용하여 복습에 대한 흥미를 이끌어 낸다. 이러한 놀이를 접목한 교육은 아이들이 공부에 흥미를 가질 수 있게 하여 자기 주도적인 학습 효과를 높일 것으로 기대한다. <br>
Keywords : Infant, learning system, object detection, AR

## 1. 서론
 현재 코로나로 인해 아이들이 유치원, 학교 등을 가지 못하게 되면서 집에서 공부하는 홈스쿨링이 주목받고 있다. 비대면 교육이 요구되는 상황에서 학교교육을 대신해서 교육을 수행할 교육방법으로 홈스쿨링을 생각하지 않을 수 없다. 즉, 홈스쿨링은 부모에 의해서 가정에서 이루어지는 교육방식으로서 코로나 시대 또는 코로나 이후의 시대에 필요한 교육형태라고 할 수 있다. 또한 오늘날은 5G(5thGeneration)시대를 맞이하여 과거와 비교할 수 없을 정도로 빨라진 데이터 통신으로 인하여 가정에서도 더 많은 다양한 교육프로그램과 콘텐츠를 제공받을 수 있게 되었다. 따라서 가정에서의 홈스쿨링에 의해서도 아동에게 필요한 교육을 효율적이고 다양하게 제공할 수 있는 교육환경이 마련되었다고 볼 수 있다. 주된 사용자의 연령층이 어린 만큼 딱딱한 학습보다는 놀이를 통해 자연스럽게 학습이 가능한 콘텐츠에 초점을 맞추어 다양한 수단이 등장하고 있다. 유아들에게는 시각, 청각, 애니메이션 자극이 민감하게 다가오기 때문에 이를 활용하면 아이들이 공부에 흥미를 가지고 나아가 학습 능력 향상에 긍정적인 영향을 준다. <br>
 시중에 있는 제품들은 모두 낱말 카드 기반의 학습을 인해 하나의 이미지로만 학습되어 단일화된 학습만 가능하나는 한계가 있다. 이 제품들과 차별성을 두기 위해 이러한 단점을 극복하려 다양화된 학습에 초점을 맞추어 주변에서 보기 쉬운 사물들은 딥러닝으로 객체 감지 학습을 시켜 사용자가 카메라 촬영을 통해 실시간으로 감지할 수 있게 한다. 또한 컴퓨터 기술의 발달로 AR과 같은 기술은 단방향 시각 자극만이 아닌 상호작용 형 그래픽 환경을 제공해 주어 학습 몰입도를 증가시킨다. 이를 이용하여 아이들의 시각적인 학습을 위해 지구, 헬리콥터 등 쉽게 보기 힘든 사물과 동물을 AR카드로 제작하고 AR에 애니메이션 효과를 적용시켜 실감나게 공부할 수 있게 한다. 학습한 단어들은 카드게임과 보물찾기 게임에 적용하여 복습 또한 재미있게 할 수 있게 한다. 이러한 놀이를 접목한 교육은 아이들이 공부에 흥미를 가질 수 있게 하여 자기 주도적인 학습 효과를 높일 수 있다.
## 2. 사용기술
> 딥러닝
 * 개념 
   * 딥러닝은 사물이나 데이터를 군집화하거나 분류하는 데 사용하는 기술이다. 컴퓨터는 사진만으로 개와 고양이를 구분하지 못하지만, 사람은 쉽게 가능하다. 사람처럼 쉽게 구분할 수 있도록 하는 방법이 기계학습(Machine Learning)이며 많은 데이터를 컴퓨터에 입력하고 비슷한 것끼리 분류하도록 하는 기술이다.
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
   * 마커 인식을 하기 위해서 낱말카드를 제작한다. 마커는 동물, 탈것, 계절나무, 행성의 카테고리로 구성했고, 카드의 색깔을 다르게 하여 구분한다. 카드의 앞면에는 사물의 사진과 단어를 넣고, 뒷면에는 제작한 마커를 넣는다. 마커는 인식률을 높이기 위해 직선을 이용한 특정패턴과 단어의 초성을 넣어 제작한다. 제작한 마커를 Unity에 불러오기 위해서 Vuforia에 package를 다운로드 받고 적용시킨다. 그리고 Vuforia에 License Manager에서 키를 등록하고, Target Manager에서 제작한 마커를 등록한다. 등록한 마커를 다운로드받아 Unity에 등록하면 마커가 준비된다. Unity에 AR Camera를 추가하여 앞에서 생성했던 key를 넣어주고, Image Target을 추가하여 등록했던 마커를 넣어준다. 마커위에 3D 객체를 띄우기 위해 Asset Store에서 무료 asset을 다운받아 Unity에 추가한 후, 에셋을 Image Target위로 불러오면 마커를 인식하여 3D객체를 볼 수 있게 된다.
