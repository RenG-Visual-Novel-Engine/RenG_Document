## Member
- - -
> **MainImageName** - `string` (R)
- 호버링되지 않을 떄의 이미지입니다.

> **HoverImageName** - `string` (NR)
- 호버링 될 때의 이미지입니다.

> **T** - `obj.Transform` (R) [[Transform]]
- 버튼이 위치할 트랜스폼이 요구됩니다.

> **Anime** - `[]*obj.Anime` (NR) [[Animation]]
- 버튼이 실행할 애니메이션이 요구됩니다.
- 여러 개의 애니메이션은 동시에 실행됩니다.

> **Action** - `func()` (R)
- 버튼을 클릭했을 때의 실행 동작이 요구됩니다.

## Process
- - -
 1. [[Transform#SpecialTransform]]이 업데이트 됩니다.
 2. MainImageName을 이용해 정의된 이미지 텍스쳐를 가져옵니다.
 3. 해당 스크린 렌더 버퍼에 업데이트 됩니다.
 4. 애니메이션이 존재하는지 판단하고 애니메이션을 추가합니다.
 5. 호버링 이미지가 존재하는지 확인하고, 이벤트를 추가합니다.