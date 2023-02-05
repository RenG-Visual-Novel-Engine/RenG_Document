## Member
- - -
> **Name** - `string` (R)
- 정의된 이미지 이름이 요구됩니다.

> **T** - `obj.Transform` (R) [[Transform]]
- 이미지가 그려질 트랜스폼이 요구됩니다.

> **Anime** - `[]*obj.Anime` (NR) [[Animation]]
- 이미지가 실행할 애니메이션이 요구됩니다.
- 여러 개의 애니메이션은 동시에 실행됩니다.

## Process
- - -
 1. 가장 먼저 [[Transform#SpecialTransform]]이 업데이트 됩니다.
 2. Name을 이용해 정의된 이미지 텍스쳐를 가져옵니다.
 3. 해당 스크린에 렌더 버퍼에 업데이트 됩니다.
 4. 



