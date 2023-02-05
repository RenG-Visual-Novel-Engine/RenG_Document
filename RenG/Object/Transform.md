## Member
- - -
> **Pos** - `obj.Vector2` (R)
- 기준점의 스크린 X, Y 픽셀 단위 좌표가 요구됩니다.

> **Size** - `obj.Vector2` (R)
- 텍스쳐 사이즈의 픽셀 단위 크기가 요구됩니다.

> **Rotate** - `int` (R)
- 텍스쳐의 도 단위 회전 각도가 요구됩니다.

> **Type** - `obj.SpecialTransform` (NR) [[Transform#SpecialTransform]]
- 특수 트랜스폼이 요구됩니다. 

## SpecialTransform
- - -
- 특수한 의도를 가진 트랜스폼들입니다.

> **Center** - `struct {}`
- 윈도우 정중앙에 정렬되며, 사이즈는 미리 기존 트랜스폼에서 정의되지 않는 이상 텍스쳐 원본 사이즈를 그대로 가지게 됩니다.

> **XCenter** - `struct { Ypos int; }` 
- 윈도우 X축을 중앙으로 고정하고 Y축 좌표(상하)를 조절할 수 있습니다.

> **YCenter** - `struct { Xpos int; }` 
- 윈도우 X축을 중앙으로 고정하고 Y축 좌표(상하)를 조절할 수 있습니다.

>   **AxisCenter** - `struct { Azis obj.Vector2; }`
- X, Y 축을 임의로 고정시키고 그 축의 교점을 중심으로 중앙 배열됩니다.

## Others
- - -
- 기존 Transform에서 작성한 Pos 값들은 SpecialTransform을 사용하면 무시됩니다.
- 혹시나 Size를 정의하지 않으면, 텍스쳐의 원본 사이즈가 그대로 사용됩니다.
- 초기화되지 않은 멤버 변수들은 Golang 기본 규칙에 따라 int 형들은 모두 0으로 설정됩니다.