# Collections

## (HIG 원문)
> (영문 내용)

Alerts convey important information related to the state of your app or the device. An alert consists of a title, an optional message, one or more buttons, and optional text fields for gathering input. Aside from these configurable elements, you can’t customize the visual appearance of an alert.

A screenshot of an alert on top of the Maps app. The alert has a title, a message, and a button labeled OK.
For developer guidance, see UIAlertController.

Minimize alerts. Alerts disrupt the user experience so it’s important to use them infrequently and only to deliver critical information. For example, an alert can notify people about a problem or give them the opportunity to confirm a purchase or a destructive action.

Use an action sheet — not an alert — to offer choices related to an intentional action. For example, when people cancel the Mail message they’re editing, an action sheet provides three choices: delete the edits (or the entire draft), save the draft, or return to editing. Although an alert can also help people confirm or cancel an action that has destructive consequences, it doesn’t provide additional choices related to the action. For guidance, see Action Sheets.

Avoid scrolling alerts when possible. For example, an alert might scroll if the text size is large enough. Minimize the potential for scrolling by keeping alert titles short and including a brief message only when necessary.

Alert Titles and Messages
Write short, descriptive, multiword alert titles. Although less text is generally better, single-word titles rarely provide enough information. As much as possible, create a title that succinctly describes the situation without needing additional message text. If the title is a complete sentence, use sentence-style capitalization and appropriate ending punctuation; if the title is a sentence fragment, use title-style capitalization and don’t add ending punctuation. For guidance, see capitalization.

If you must provide a message, write short, complete sentences. Create a message that’s short enough to fit on one or two lines so people don’t have to scroll. Use sentence-style capitalization and appropriate ending punctuation.

Be direct, and use a neutral, approachable tone. Alerts describe problems and serious situations, so it’s important to avoid being oblique or accusatory, or masking the severity of the issue.

Avoid explaining the alert buttons. If your alert text and button titles are clear, there’s no need to explain what the buttons do. In rare cases where you need to provide guidance on choosing a button, use a term like choose to account for people’s current interaction method, and use the exact button title without quotes.

Alert Buttons
Create succinct, logical button titles. Aim for a one- or two-word title that describes the result of selecting the button. Prefer verbs and verb phrases that relate directly to the alert title and message — for example, View All, Reply, or Ignore. Use OK for simple acceptance, and avoid using Yes and No. Always use Cancel to title a button that cancels the alert’s action. As with all button titles, use title-style capitalization and no ending punctuation.

Place buttons where people expect them. In a typical two-button alert, the button people are most likely to tap is on the trailing side and the Cancel button is on the leading side. An alert that contains more than two buttons displays them in a stack, with the most likely button at the top and the Cancel button at the bottom.

Identify destructive buttons. If an alert button results in a destructive action, such as deleting content, use the destructive button style to ensure the system displays it appropriately. For developer guidance, see the UIAlertAction.Style.destructive. In this scenario, be sure also to include a Cancel button in the alert so people can explicitly opt out of the destructive action. Use the default style for the Cancel button so people can also activate it by pressing Return on a keyboard.

Let people cancel an alert by exiting to the Home screen. Accessing the Home screen while an alert is visible exits the app, dismissing the alert without performing any action. People also appreciate canceling an alert by pressing Escape (Esc) on a keyboard or using the standard keyboard shortcut Command-Period (.).


## (한글 번역)
![](https://velog.velcdn.com/images/dnfl8721/post/5ef84433-eb99-4980-9f23-904b89ecc104/image.png)

>**1) 특징**

- 앱이나 디바이스의 상태와 관련된 중요한 정보를 전달
- 구성 : title, optional message, 1개이상의 button  (인풋을 받는 optional textField)
- 이외의 구성은 커스터마이징 불가

>**2) 전체적인 가이드라인**

1. alert사용 최소화하기

    → 유저경험 저하요소

    → ex) **구매 확인**이나 **destructive action**(like 삭제나 취소)일때 사용
    

2. 의도적인 행위(와 관련된 추가적인 선택지 like edit)을 제공하려고 할 때는 alert말고 action sheet를 사용하기
    
    → alert은 destructive action(삭제,취소)을 제공하지만 그 이외의 action은 제공하지 않음
    

    → 가능한 경고창에서 스크롤하는 거 피하기

    → title이나 message를 짧게!
    
>### Alert Titles and Messages

**titles**

- 짧고, 핵심만 제공하는 **2개 이상의 단어**로 타이틀 구성하기

    → 1개의 단어로는 핵심정보 제공 미흡

    →  타이틀이 **문장형**이면 **sentence-style capitalization + 마침표o**

    → 타이틀이 **문장형이 아니라면** **title-style capitalization + 마침표x**

- 무슨 말이야?
    - *Sentence-style capitalization:* **This line provides an example of sentence-style capitalization.**
    - *Title-style capitalization:* **This Line Provides an Example of Title-Style Capitalization.**


**messages**

- 1~2라인에 맞추서 작성하기(스크롤안되도록)

- sentence-style capitalization + 마침표o

  → **This Line Provides an Example of Title-Style Capitalization.**

- 직접적으로 말하되 중립적이고 접근하기쉬운(부드러운) 톤으로 말하기

- alert 버튼 설명하는 거 피하기



**Alert Buttons**

- **1개의 단어 혹은 2개의 단어**로 버튼선택의 결과를 표현하기

- 타이틀이나 메시지와 관련된 **동사**로 표현하는거 선호

- ex: View All, Reply, Ignore, Ok  그러나 Yes,No는 피하기

- 취소행위를 하는 버튼에는 **Cancel**로 표현하기

- **title-style capitalization + 마침표x**
- **버튼 2개면 오른쪽 Cancel버튼, 버튼 3개면 가장 아래쪽에 Cancel**
- 콘텐트 지우는 것과 같은 destructive action을 초래하는 버튼은 **적절히 보여주기**
( [UIAlertAction.Style.destructive](https://developer.apple.com/documentation/uikit/uialertaction/style/destructive))

![](https://velog.velcdn.com/images/dnfl8721/post/2b60be7a-d9cb-4970-85a6-7b1e024f03a8/image.png)



- Cancel button은 default style (그런데 style 코드칠때 default도 있지만 .cancel 종류도 있어서 이거 사용하면 될듯. 차이는 .cancel은 버튼이 3개이상이면 자동으로 맨 아래에 위치시켜줌)


![](https://velog.velcdn.com/images/dnfl8721/post/8e0ef96b-f6d4-4325-bc8d-44ce7286077b/image.png)


- 경고창이 켜지더라도 홈스크린으로 넘어가면  경고창 취소되도록 해라 (dismiss해라)

## Point of this component (이 타이틀은 나중에 결정하시죠)
