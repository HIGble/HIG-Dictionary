# Text Views

## HIG 원문
A text view displays multiline, styled text content. Text views can be any height and enable scrolling when the content extends outside of the view. By default, content within a text view is left-aligned and uses the system font in black. If a text view is editable, a keyboard appears when you tap inside the view.


Keep text legible. Although you can use multiple fonts, colors, and alignments in creative ways, it’s essential to maintain the readability of your content. It’s a good idea to adopt Dynamic Type so your text still looks good if people change text size on their device. You should also test your content with accessibility options enabled, such as bold text. See Accessibility.

Show the appropriate keyboard type. iOS provides several different keyboard types, each designed to facilitate a different type of input. To streamline data entry, the keyboard displayed during the editing of a text view should be appropriate for the type of content in the field. For a complete list of available keyboard types, see the UIKeyboardType constant of UITextInputTraits.

## 한글 번역

>### 특징
- 멀티라인으로 텍스트 콘텐츠 보여줌
- 콘텐츠 양이 방대하면 스크롤링을 가능케 함.
- left-aligned가 디폴트
- editable가능하다면 탭할때 키보드가 나타난다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/23d9be5c-c7df-4289-b0ab-277358c4d67d/Untitled.png)

>### 가이드라인
### 텍스트를 읽을수 있도록 유지하라.

- 다양한 폰트,컬러, 배치를 사용할 수 있지만 가독성을 유지하는게 가장 중요함
- 동적 타입을 채택하라 ( 디바이스에 따라 텍스트크기가 변하는 )
- 콘텐츠의 접근성 옵션이 가능케 해야함. ( 접근성은 Reduce Transparency, VoiceOver, Button Shapes)

### 적절한 키보드 타입을 보여주어라.

- 인풋의 타입에 따라 적절한 키보드 타입 보여주기.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d4acec24-f176-4936-bb30-41a15b84b1f9/Untitled.png)


## Point of this component (이 타이틀은 나중에 결정하시죠)
