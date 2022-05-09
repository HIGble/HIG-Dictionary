# [Scroll Views](https://developer.apple.com/design/human-interface-guidelines/ios/views/scroll-views/)

## (HIG 원문)

> A split view manages the presentation of hierarchical content at the top level of your app. A split view consists of a two- or three-column interface showing a primary column, an optional supplementary column, and a secondary pane of content. Changes in the primary column drive changes in the optional supplementary column, which affect the content itself. Split views are useful for navigating multiple levels of content hierarchy, like traversing the mailboxes and messages in Mail to view each message.<br/><br/>
Split views can display a variety of content, but many system apps like Mail use a split view to create a sidebar-based interface. In this type of interface, the primary column shows a sidebar, the optional supplementary column shows a list view, and the secondary content pane shows details about the selected content. For related guidance, see [Sidebars](https://developer.apple.com/design/human-interface-guidelines/ios/bars/sidebars/).<br/><br/> 

![split-views_2x](https://user-images.githubusercontent.com/50728605/167324938-449d3df4-3d1c-452a-bac6-1216668d254e.png)

> **On iPad, use a split view instead of a tab bar.** Split views provide the same quick navigation as tab bars while making better use of the large display.<br/><br/> **Choose the appropriate style for each type of column.** For the primary column displaying the sidebar, use the sidebar appearance. This appearance is appropriate for app-level navigation and lists of collections, like the mailboxes in Mail. For the supplementary column displaying the list view, use the plain sidebar appearance. This appearance is appropriate for lists of individual pieces of content, like the messages in a mailbox. For developer guidance, see [UICollectionLayoutListConfiguration.Appearance](https://developer.apple.com/documentation/uikit/uicollectionlayoutlistconfiguration/appearance).<br/><br/> **Persistently highlight the active selection in the primary and supplementary columns.** Although the secondary pane's content can change, it should always correspond to clearly identifiable selections in the other columns. This selection helps people understand the relationship between the columns and keep themselves oriented.<br/><br/> **If appropriate, allow people to drag and drop content between columns.** Because split views provide access to multiple levels of hierarchy, people can quickly move content from one part of the app to another by dragging and dropping items between the columns. For related guidance, see [Drag and Drop](https://developer.apple.com/design/human-interface-guidelines/ios/user-interaction/drag-and-drop/).<br/><br/>
> For developer guidance, see [UISplitViewController](https://developer.apple.com/documentation/uikit/uisplitviewcontroller).

<br/><br/>

## (한글 번역/정리)
### Definition
- 최상위 수준에서 콘텐츠의 계층적 표시를 관리합니다.
- **구성:** 주(primary)열, 선택적보조(optional supplementary)열, 콘텐츠를 표시하는 창(secondary pane)
- primary열에서 일어나는 변화는 optional supplementary열에도 영향을 주고 이는 콘텐츠 자체에도 영향을 준다.
- 여러 수준의 콘텐츠 계층을 탐색하는데 유용하다 (eg. Mail에서 메일상자와 메시지를  왔다갔다 할 때)<br/>
대부분의 split view들은 Mail 앱과 같이 Sidebar를 사용한다.

***

### Guidelines
1. iPad에서 tab bar 대신에 split view 사용하기<br/>
    - Tab bar와 같이 빠른 경로 탐색을 주는 동시에 큰 화면을 효과적으로 사용한다.
2. 각 열의 유형에 적합한 스타일 선택하기
    - primary열에서 side bar를 사용하자. 이는 앱 수준에서의 경로탐색과 리스트들의 묶음(예를 들어, Mail앱의 mailbox=수신함)에 적절하다.
    - suuplementary 열에서는 리스트뷰를 보여주기 위해 일반 side bar를 사용한다. Mailbox에서 메시지와 같이 독립적인 컨텐츠들의 리스트를 표시하는데 적합하다. 
3. 기본 및 보조열에서 active selection는 지속적으로 강조 표시하기
    - 컨텐츠를 표시하는 창(second pane)의 컨텐츠는 변할 수 있어도, 항상 다른 열에서 명확하게 식별할 수 있는 선택항목과 일치해야 한다.
    - 이 선택은 사람들이 열 사이의 관계를 이해하고 자신의 위치/방향을 유지하는 데 도움이 된다.
4. 만약 적절하다면, 사용자가 열 사이에 내용을 끌어 놓을 수 있도록(drag and drop)하기
    - Split view는 여러 수준의 계층에 대한 접근을 제공한다. 따라서, 사용자가 열 사이에 항목을 끌언다 놓아 앱의 한 부분에서 다른 부분으로 콘텐츠를 빠르게 이동할 수 있도록 한다.

***

### 예시
- iPad에서 사용하는 Mail 앱

<br/><br/>

## Point of this component (이 타이틀은 나중에 결정하시죠)
