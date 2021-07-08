# 주요 UI 컴포넌트 (RectTransform, Image, Text, Button)
UI 요소를 배치하기 위해서 주요 UI 컴포넌트에 대해서 알아보자.
## The Rect Tool
UI를 제작할때 가장 많이 사용되는 툴이다. Rect Tool은 2D 기능과 UI 모두에 사용이 되며, 3D 객체에도 사용이 가능하다.

![](./Images/Unity_Rect_Tool_Button.jpg)

* 첫 번째 기능은 UI 요소를 선택한 후 드래그하여 이동할 수 있다.
* 두 번째 기능은 UI 요소의 위치를 변경할 수 있다.
* 세 번째 기능은 UI 요소를 회전시킬 수 있다.
* 네 번째 기능은 UI 요소의 크기를 한 방향으로만 늘어나게 할 수 있다.
* 다섯번째 기능은 UI 요소의 크기를 자유롭게 변형시킬 수 있다.
## RectTransform

RectTransform 기능은 UI 요소의 위치, 회전, 크기 조절을 할 수 있고 너비와 높이 조정도 가능하다.

![](./images/UI_RectTransform.png)

* Pos는 아래 설명의 Anchor와 Pivot의 기준으로 설정된 실제 좌표이다. 이를 사용하여 UI 요소의 크기를 변경할 수 있다.
* Anchors는 UI 요소의 원점 위치를 정할 수 있다. 아래 이미지의 앵커 좌표를 원점으로 하여 UI 요소 위치 기준값을 결정할 수 있다. 
![](./images/Unity_Anchor_image.jpg)
* UI 요소의 원점을 두고 싶을 경우엔 캔버스의 왼쪽 하단(0,0) 오른쪽 상단(1,1)일 때 Anchor의 값을 (0.5, 0.5)로 지정하면 된다.

* 왼쪽 상단 모서리에 있는 Anchor Preset 버튼에 대해서 알아보자면, 이는 UI 요소를 부모 영역의 측면이나 중간에 고정을 시켜 부모 크기와 함께 늘릴 수 있다. 여기에서 수평 및 수직은 독립적이다.
* 부모 영역 안에 있는 자식 영역을 정확한 위치에 고정시키고 싶다면 Ctrl + alt + 앵커 좌 클릭을 하면 된다. 자식 영역을 옆으로 늘리고 싶을때는 stretch를 클릭하면 된다.
![](./images/Unity_Anchor_image_3.jpg)

* Pivot는 UI 요소 내부의 기준점을 정할 수 있다.
## Image
![](./images/UI_ImageInspector.jpg)

* 
## Text

## Button

# 피드백

Pivot에 대한 개념이 이해가 안 됩니다. image 설명부터는 내일 다 끝내겠습니다..!
