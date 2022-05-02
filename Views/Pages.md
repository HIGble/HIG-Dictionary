# Pages

## HIG 원문
> A page view controller provides a way to implement linear navigation between pages of content, such as in a document, book, notepad, or calendar. A page view controller uses one of two styles to manage transitions between pages during navigation—scrolling or page-curl. A scrolling transition has no specific appearance; pages fluidly scroll from one to the next. A page-curl transition causes pages to curl over as you swipe across the screen, turning like pages in a physical book. <br><br>
**If appropriate, implement a way to navigate nonlinearly.** When a page view controller is used, pages flow sequentially and there’s no way to jump between nonadjoining pages. If people may need to access pages out of sequence in your app, implement a custom control that provides this functionality. <br><br>
For developer guidance, see UIImageView.

<br>

## 번역
페이지 뷰 컨트롤러는 문서, 책, 노트패드 또는 캘린더와 같은 콘텐츠 안에서 페이지를 탐색할 수 있는 선형 네비게이션을 구현하도록 한다. 페이지 뷰 컨트롤러는 화면 전환을 위해 스크롤링(scrolling)또는 페이지컬(page-curl) 두가지 중 한가지 방식을 사용한다. 스크롤링은 특별한 효과가 없다. 페이지는 부드럽게 다음 페이지로 넘어간다. 페이지컬은 화면을 스와이프 할 때, 실제 책을 넘기는 것처럼 화면이 말린다.<br><br>

가능하다면, 비선형적인 방식으로 구현해라. 페이지 뷰 컨트롤러를 사용할 경우, 페이지가 순차적으로 넘어가기 때문에 서로 인접하지 않은 페이지로 넘어갈 수 없다. 만약 사람들이 서로 인접하지 않은 페이지에 접근해야 한다면, 커스텀 컨트롤을 통해 이러한 기능을 구현해라.


- **페이지컬(Page-curl)이란?**<br>
종이가 말리는 듯한 효과를 주는 것으로 현실에 있는 대상의 질감과 행위를 그대로 묘사하려는 [스큐어모피즘](https://macnews.tistory.com/1607)적인 애니메이션 효과로 볼 수 있다.

<br>

## 결론
페이지 뷰 컨트롤러는 책을 넘기는 듯한 애니메이션을 가진 선형적인(순차적으로 페이지를 넘길 수 있는)  네비게이션을 가진 뷰이다. 하지만 페이지에 순차적으로만 접근 가능하기 때문에 원하는 페이지에 접근을 하려면 커스텀을 통해 원하는 페이지로 이동할 수 있는 기능을 추가해야 한다. 따라서, 유저의 편의를 위해선 비선형적인 방식으로 구현을 하자.

<br>

### 예시
애플 도서 어플

<br>

<!-- ### 제언
애니메이션이 아니라 뷰 자체가 이런 애니메이션을 가진 것이라면 기능을 키고 끄는게 불가능 한 것일까? -->

### 구성요소
UIKit - [UIPageViewController](https://developer.apple.com/documentation/uikit/uipageviewcontroller)<br>
SwiftUI - 정해진 애니메이션이 존재하지 않는 것으로 보인디. 계속 리서치해보고 추가하도록 하겠습니다.