### Overview

---

- **화면에 나타나는 인터페이스 요소를 설명하거나 짧은 메시지를 제공**한다.
- 유저는 레이블을 **편집할 수 없다.**
- 유저는 레이블의 **내용을 복사할 수는 있다.**
- 고정 텍스트([static text](https://www.sothink.com/tutorials/static-text-and-dynamic-text.htm))를 얼마든지 표시할 수 있지만, 짧게 유지하는 것이 좋다.
    - static text: 입력을 하거나 편집이 불가능한 텍스트
    - (cf) dynamic text: 유저가 내용을 입력하거나 편집이 가능한 텍스트

<p align="center">
<img src="https://user-images.githubusercontent.com/50728605/169069599-46deff48-260d-4d2b-a1fc-d696078eabcc.png" width="350" alignment"center">
</p>


### Guideline

---

- **레이블은 읽기 쉬워야 한다(legible).**
    - 레이블은 기본 또는 스타일이 지정된 텍스트가 포함될 수 있다.
    - 레이블의 스타일을 수정하거나 사용자 정의 글꼴을 사용하면 가독성을 해치지 않도록 해야한다.
    - 유저가 기기에서 글크기를 변경할 때도 여전히 가독성이 좋도록 다이나믹 타입([Dynamic Type](https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/typography/#dynamic-type-sizes))을 채택하는 것이 좋다.
    - Dynamic Type: 유저가 원하는 글크기를 사용할 수 있도록 유저에게 유연성(flexibility)를 제공
    - 레이블을 [접근성](https://developer.apple.com/design/human-interface-guidelines/accessibility/overview/introduction/) 옵션을 활성화한 상태(eg. 볼드체)로 테스트를 해봐야 한다.        
<p align="center">
<img src="https://user-images.githubusercontent.com/50728605/169069659-5fe3d78f-0caf-4d61-9214-db4ca4147ecb.png" width="500" alignment"center">
</p>

- 텍스트에 대해 알고싶다면, [String Programming Guide](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/Strings/introStrings.html) 확인
- 텍스트의 스타일을 만들고 싶다면, [Attributed String Programming Guide](https://developer.apple.com/library/content/documentation/Cocoa/Conceptual/AttributedStrings/AttributedStrings.html) 확인
- 레이블 개발자 가이드를 보기 위해서는 [UILabel](https://developer.apple.com/documentation/uikit/uilabel) 확인

### Example

---

- 아래는 onthelook 라는 패션앱니다.
- “카테고리"에서 각 그림 아이콘마다 설명(eg 아우터, 상의, 하의 etc)이 되는 레이블이 있다.

<p align="center">
<img src="https://user-images.githubusercontent.com/50728605/169069763-d8354c2f-9deb-4376-8d51-a970f64e8958.png" width="400">
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/50728605/169071192-4cdb042b-0d10-4e33-854d-03840a4be5de.png" width="400">
</p>
