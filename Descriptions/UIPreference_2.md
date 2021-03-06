
# UI 환경설정 (Camera, Canvas) 

유니티 엔진에서 UI를 제작하려면 어떻게 해야하는지 주요 컴포넌트의 설정에 대해 알아보자.

## Camera

씬뷰의 특정 영역을 캡쳐하여 화면을 플레이어에게 보여주는 장치이다. 하나의 씬에 카메라는 여러개가 있을 수 있으며 마스킹을 통해 일부만 보여지게 할 수 있다.

### 투영(Projection)

카메라가 피사체를 캡쳐하여 실제 화면에 보여지게 하는 것을 투영이라고 한다. 이 과정에서는 복잡한 과정을 거치지만 생략한다. 

유니티에서는 2가지의 투영 기법을 선택할 수 있다.

* Perspective(원근 투영) : 카메라가 현재 씬에 구성된 오브젝트들의 원근감을 그대로 살려서 화면에 보여준다. 즉, 카메라에 가까이 있는 오브젝트는 멀리있는 오브젝트보다 크게 보여진다. 원근 투영의 경우 카메라의 영역은 `절두체(Frustum)` 라고 하는 사각뿔에서 윗 부분이 평행하게 잘린 형태다.

| ![](./Images/Camera_1.PNG) |
|:--:|
| [절두체](http://telnet.or.kr/directx/graphics/programmingguide/fixedfunction/viewportsclipping/viewingfrustum.htm) |

* Orthographic(직교 투영) : 카메라가 원근감 없이 그대로 화면을 보여준다. 원근감이 없기 때문에 당연하게도 거리에 상관없이 오브젝트의 크기는 동일하다. 카메라의 영역은 직사각형 이다.

## Canvas

* 캔버스란 UI를 어떻게 그려지게 할지 보여지게 하는 게임 개체이다.
* 캔버스를 생성하는 방법은 Hierarchy 창 하단의 빈공간에서 마우스 오른쪽 버튼 - UI - Canvas 이다.
* 만약 UI 요소를 추가하는 과정에서 Canvas를 먼저 생성하지 않았을때는 자동으로 추가가 된다.

![](./Images/UnityCanvas_3.jpg)
* 캔버스의 영역은 씬뷰에서 직사각형으로 표시된다.
![](./Images/UnityCanvas_1.jpg)

* UI 요소를 추가할때 그려지는 순서는 첫 번째 자식이 먼저 표현되고 두 번째 자식이 다음으로 표시된다. 요소 순서를 변경하고 싶다면 요소를 드래그하면 된다. 아래의 예시 자료를 통해 알기 쉽게 설명하자면, Image(1) - Image(2) 순서로 UI 요소를 표현했지만 둘의 순서를 변경하고 싶다면 Image(2)를 위로 드래그하면 된다.
![](./Images/UnityCanvas_2.jpg)

### 렌더 모드(Render Mode)

캔버스에는 화면에 렌더링 할 때 사용할 수 있는 렌더링 모드 설정이 있다.

* Screen Space - Overlay 이 모드는 렌더링 된 화면 위에 UI 요소를 배치하는 것이다. 화면 크기, 해상도가 조절될 때 자동으로 캔버스가 크기를 변경한다.
* Screen Space - Camera 이 모드는 Camere 앞에 주어진 거리에 배치된다. UI 요소는 카메라 설정에 따라서 모양에 영향을 준다. 화면 크기, 해상도, 카메라 절두체가 변경되면 캔버스도 자동으로 크기가 변한다.
* World Space 이 모드는 자동으로 크기 조절이 아닌 수동으로 설정하고 싶을 경우에 쓰인다. UI 요소는 3D 배치에 따라서 Scend의 다른 개체 앞, 뒤에 랜더링 된다. 

-----------

# 피드백

## 개인적인 의견

* 피드백 단락에 있던 이름을 삭제했습니다. 공개된 저장소라 인터넷에 실명이 노출되기 때문입니다. 사실 전 상관없긴 합니다.
* 문서를 작성할땐 유니티에 대해 아무것도 모르는 사람이 봐도 어느정도 이해가 가는 수준에서 작성되었으면 좋겠습니다. 물론 UI 디자이너가 UI 환경설정에 대한 주요 컴포넌트를 조작할 일이 크게 없긴 하지만 '이 컴포넌트는 뭘 하는거다~' 정도는 알아야 한다고 생각합니다.
* Line 4 : 유니티 프로그램이라는 말 보단 '유니티 엔진에서~' 혹은 '유니티 에서' 가 좀 더 의미전달이 명확한 것 같습니다. 또한 '환경설정을 알아보자' 보단 Camera와 Canvas 컴포넌트에 대한 설명이 들어가니 '주요 컴포넌트의 설정에 대해 알아보자' 정도가 좋은듯 합니다.

## 이건 고쳐야해!

* UI 환경설정 과정이 없습니다. 씬에 어떤 오브젝트가 어떻게 배치되는지 어떤 컴포넌트가 어떻게 활용되는지에 대한 이미지도 있으면 좋을것 같습니다.
* 최상단 주제에서 Camera와 Canvas에 대해 써놓았지만 문서의 전체 단락엔 Canvas에 대한 설명밖에 없습니다.
* Camera는 간단한 설명만 있으면 될 것 같습니다.
* Canvas의 설명에 대해 글 만으로는 이해가 힘든 것 같습니다. 역시 추가적인 이미지가 있으면 좋을 것 같습니다.
* 렌더모드에 대한 설명에 '화면 공간, 세계 공간' 이라는 용어가 나오는데 혹시 이해를 하고 계신지 궁금합니다. 하지만 꼭 이해를 할 필요는 없습니다. 그렇다면 그냥 '화면에' 정도로 축약하는게 다른 사람이 보거나 이후에 님께서 보더라도 문제가 없지 않을까 싶습니다.

----------

# 피드백

* UI 환경설정 과정이 없습니다. 씬에 어떤 오브젝트가 어떻게 배치되는지 어떤 컴포넌트가 어떻게 활용되는지에 대한 이미지도 있으면 좋을것 같습니다. -> 이 부분에 대한 설명이 잘 이해가 가지 않습니다. UI 요소들이 어떻게 배치되고 어떤 컴포넌트(?)는 버튼과 같은 것들을 말하는지 좀 더 자세하게 설명 부탁드립니다.

--------

# 피드백

* 위에 하이어라키와 씬뷰의 이미지를 올린것처럼 처음 캔버스 설정부터 UI 요소들 (ex : 이미지, 텍스트) 같은 컴포넌트 들을 배치하는 과정에 대한 이미지를 의미한 것이었습니다. 지금 생각해보니 그 정도까진 필요없을것 같기도 합니다. 요번 챕터는 여기서 마무리 하겠습니다. 다음 챕터에 대한 문서 작성을 준비하시면 될 것 같습니다. 문서는 제가 미리 만들어 놓겠습니다.

