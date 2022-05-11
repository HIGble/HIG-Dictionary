# [Sheets](https://developer.apple.com/design/human-interface-guidelines/ios/views/sheets/)

## (HIG 원문)
> A sheet helps people perform a distinct task that’s related to the parent view without taking them away from their current context. For example, Mail uses a sheet to help people compose an email without leaving their mailboxes, and Translate uses a sheet to display a dictionary view that helps people define the word they want to translate.<br/><br/>
A screenshot of an in-progress email on iPhone. A very small horizontal strip of the inbox view is visible above the top of the compose sheet. The keyboard is visible in the bottom half of the screen.<br/><br/>
A screenshot of the translation view on iPhone, showing the word hello in English and in Arabic. The dictionary sheet is visible in the bottom half of the screen, providing the definition of hello in both languages.<br/><br/>
For developer guidance, see [UISheetPresentationController](https://developer.apple.com/documentation/uikit/uisheetpresentationcontroller).<br/><br/>
A sheet appears as a card that partially covers the underlying content. The card’s top corners are rounded to visually distinguish it from the parent view. You can customize a sheet’s corner radius to coordinate with the corner radii you use elsewhere in your app; for developer guidance, see [preferredCornerRadius](https://developer.apple.com/documentation/uikit/uisheetpresentationcontroller/3852556-preferredcornerradius).<br/><br/>
People typically expect to resize a sheet when they scroll its contents or drag the grabber, which is a small horizontal indicator that can appear at the top edge of a sheet. In iOS 15 and later, sheets can resize according to their detents. Designed for iPhone, detents specify particular heights at which a sheet naturally rests. The system defines two detents: large is the height of a fully expanded sheet and medium is about half the fully expanded height.<br/><br/>
A diagram showing an iPhone in portrait containing a solid rounded rectangle with a dashed outline that occupies almost all of the screen. The solid rectangle is labeled Large.<br/><br/>
A diagram showing an iPhone in portrait containing a dashed outline of a rounded rectangle that occupies most of the screen. A solid square shape with rounded corners appears in the bottom half of the outlined rectangle, labeled Medium.<br/><br/>
Sheets automatically support the large detent. Adding the medium detent allows the sheet to rest at both heights, whereas specifying only medium prevents the sheet from expanding to full height. For developer guidance, see [detents](https://developer.apple.com/documentation/uikit/uisheetpresentationcontroller/3801903-detents).<br/><br/>
By default, a sheet is modal, presenting a focused experience that dims the parent view and prevents interaction with it. After people finish interacting with a modal sheet, they dismiss it — or it dismisses automatically — before resuming their task in the parent view. In iOS 15 and later, a sheet can also be nonmodal. When a nonmodal sheet is onscreen, people can continue their task in the parent view while also interacting with the sheet.<br/><br/>
**Use a sheet for nonimmersive content and simple tasks.** A sheet allows part of the parent view to remain visible behind it, helping people retain their original context as they interact with the sheet. Use a full-screen modal presentation to offer immersive content such as videos, photos, or camera views, or to enable a complex task such as marking up a document or editing a photo. The full-screen modal style covers the entire screen, minimizing visual distraction. For developer guidance, see [UIModalPresentationStyle.fullScreen]((https://developer.apple.com/documentation/uikit/uimodalpresentationstyle/fullscreen)).<br/><br/>
**In an iPhone app, consider supporting the medium detent to allow progressive disclosure of the sheet’s content.** For example, a share sheet displays the most relevant items within the medium detent, where they’re visible without resizing. To view more items, people can scroll or expand the sheet.<br/><br/>
**Use a nonmodal sheet when you want to present supplementary items people can use without pausing the main task.** When people choose an item in a nonmodal sheet, the parent view can update in response, providing feedback on the item’s effect and letting people continue their task while the sheet remains onscreen. For example, Notes uses a nonmodal sheet to help people apply different formatting to different text selections as they edit a note. To enable a nonmodal sheet experience, you support the medium detent and remove dimming from the parent view (for developer guidance, see [largestUndimmedDetentIdentifier](https://developer.apple.com/documentation/uikit/uisheetpresentationcontroller/3858107-largestundimmeddetentidentifier)).<br/><br/>
**A screenshot of an in-progress note on iPhone.** Two words have been selected and are shown highlighted in yellow. In the bottom half of the screen, the format sheet shows that the selected words use the body font in bold.<br/>
The Notes format sheet lets people apply formatting to selected text in the editing view.<br/><br/>
**A screenshot of the same in-progress note on iPhone.** A different word has been selected and highlighted in yellow. The format sheet shows that the selected word uses the body font in italics.
Because the sheet is nonmodal, people can make additional text selections without dismissing the sheet.<br/><br/>
**In general, include a grabber in a resizable sheet.** A grabber shows people that they can drag the sheet to resize it; they can also tap it to cycle through the detents. In addition to providing a visual indicator of resizability, a grabber also works with VoiceOver so people can resize the sheet without seeing the screen. For developer guidance, see [prefersGrabberVisible](https://developer.apple.com/documentation/uikit/uisheetpresentationcontroller/3801906-prefersgrabbervisible).<br/><br/>
**Don’t display a sheet on top of a popover.** Although you can display a sheet within a popover, nothing should appear on top of a popover (except possibly an alert). In rare cases when you need to present a sheet after people take an action in a popover, close the popover before displaying the sheet.

---
## (한글 번역)
### Definition
- 현재의 컨텍스트에서 벗어나지 않으면서 상위뷰와 관련된 고유한 작업을 수행할 수 있도록 도와준다.
    - 예시1: Mail앱에서 사용자가 수신함을 벗어나지 않으면서 메일을 작성할 수 있도록 처리한다.
    - 예시2: 번역앱에서 사전 뷰를 시트로 보여줌으로써 원하는 단어를 찾을 수 있도록 한다.<br/><br/>
<img width="600" alt="스크린샷 2022-05-10 오후 8 45 59" src="https://user-images.githubusercontent.com/50728605/167621268-627053b4-2fcd-4f04-b1e3-c61a7753b6ee.png"> <br/>

#### 형태
- 시트는 뒤의 컨텐츠를 밑으로 깔고 있는 카드 형태로 나타난다.
- 카드 형태는 상위 뷰와의 차이를 나타내기 위해 위의 모서리가 둥근형태를 가진다. 둥근형태의 정도는 사용자 정의(customize)가 가능하다.<br/><br/>
- 일반적으로 **시트의 내용을 스크롤**하거나 **시트 상단 가장자리에 나타날 수 있는 작은 수평표시인 그래버(grabber)** 를 통해 시트의 크기를 조정한다고 기대한다.
- iOS15 이후: 시트의 크기는 시트의 멈춤쇠(detent)에 따라 조절이 가능하다.
    - detent 뜻: 풀리기 전까지 움직이지 못하게 하는 기계의 고정장치
    - detent 예시: 돌림판에서 회전을 멈추게 하는 부분
    - 아이폰용으로 설계된 멈춤쇠(detent)는 시트가 자연스럽게 놓이는 특정 높이를 지정한다.
    - 이때, 시스템은 2가지의 멈춤쇠(detent)를 정의한다
        1. large: 높이가 완전히 확장된 시트
        2. medium: 노피가 반만 확장된 시트<br/>
    <img width="500" alt="스크린샷 2022-05-10 오후 8 48 23" src="https://user-images.githubusercontent.com/50728605/167621555-92420356-8395-46e9-b0f5-2de8e2b0d602.png"><br/>
    
- 시트는 대부분 large detent를 지원한다.<br/>
- 일반적으로 시트는 "모달(modal)"이다. 모달은 상위 뷰를 어둡게 하고 상호작용을 방지하면서 주의를 집중시키는 환경을 제공한다.
- 모달 시트와 상호작용이 끝난 후 상위뷰로 돌아가서 남은 작업을 하기 전에 이를 해제시키거나 자동으로 해제가 된다.
- iOS15 이후: 시트는 비모달(non-modal)일 수 있다. 비모달 시트가 온스크린(화면에 있는)이면, 사용자는 시트와 상호작용하면서 부모뷰에서 작업을 진행할 수 있다. 

***

### Guidelines
1. **비몰입 콘텐츠 및 간단한 작업에는 시트를 사용하기**
    - 시트를 사용하여 부모 뷰의 일부를 시트 뒤에 표시할 수 있으므로 사람들이 시트와 상호작용할 때 원본 내용을 유지할 수 있다.
    - 전체화면 모달 프레젠테이션은 몰입형 콘텐츠(비디오, 사진, 카메라 뷰)를 제공하거나 복잡한 작업(문서, 사진편집)을 수행할 수 있다.
    - 전체화면 모달 스타일은 전체화면을 덮기 때문에 시각적 산만함을 최소화한다.<br/>
    
2. **아이폰 앱에서 시트 내용을 점진적으로 공개할 수 잇도록 medium detent를 지원하는 것을 고려하기**
    - 예시: 공유 시트는 medium detent 안에 크기 조정없이 볼 수 있는 가장 관련성이 높은 항목을 표시한다. 이는 더 많은 항목을 보기 위해서는 스크롤이나 시트를 확장할 수 있어야 한다.<br/>
    
3. **사용자가 주요 작업을 일시중지하지 않고 사람들이 사용할 수 있는 보조 항목을 제시하려면 비모달(nonmodal) 시트를 사용하기**
    - 비모달에서 항목을 선택하면 부모뷰가 응답함으로써 업데이트가 된다. 업데이트가 되면 항목의 효과에 대한 피드백을 제공하고 시트가 화면에 남아있는 동안 사용자는 작업을 계속할 수 있다.
    - 예시: Notes에서 비모달 시트를 사용하여 사람들이 메모를 편집할 때, 텍스트 선택 항목에 다른 서식을 적용할 수 있다.
    - 비모달 시트 환경을 활성화하기 위해서는 medium detent를 지원하고 상위 뷰의 흐릿함을 제거해야 한다.<br/>
    <img width="600" alt="스크린샷 2022-05-10 오후 8 49 22" src="https://user-images.githubusercontent.com/50728605/167621716-17a68551-59ea-451a-827c-6943d1e2acec.png"><br/>

    
4. **일반적으로 크기 조정 가능한 시트에 그래버(grabber)를 포함하기**
    - 그래버는 시트를 끌어 크기를 조절할 수 있음을 알려준다.
    - detent 사이를 순환하기 위해 시트를 누를 수도 있다.
    - 추가로, 화면을 보지 않고 시트의 크기를 조정할 수 있도록 VoiceOver와 함께 작동하기도 한다.<br/>
    
5. **팝업 위에 시트를 표시하지 않기**
    - 팝업 내에 시트를 표시할 수는 있지만, 팝업 위에는 나타나서는 안된다(경고는 제외될 수도 있다)
    - 드물게 사용자가 팝업에서 작업을 수행한 후 시트를 표시해야하는 경우, 시트를 보여주기 전에 팝업을 닫아야 한다.

---
## Point of this component (이 타이틀은 나중에 결정하시죠)

---
### Reference
