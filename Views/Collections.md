# Collections

## (HIG 원문)
> (영문 내용)
A collection manages an ordered set of content, such as a set of photos, and presents it in a customizable and highly visual layout. Because a collection doesn’t enforce a strictly linear format, it’s particularly well-suited to displaying items that vary in size. Generally speaking, collections are ideal for showing off image-based content. Backgrounds and other decorative views can optionally be implemented to visually distinguish subsets of items.


Collections support both interactivity and animation. By default, you can tap to select, touch and hold to edit, and swipe to scroll. If your app requires it, more gestures can be added for performing custom actions. Within a collection, animations can be enabled whenever items are inserted, deleted, or reordered, and custom animations are also supported.

Avoid creating radical new designs when a standard row or grid layout is sufficient. A collection should enhance the user experience, not become the center of attention. Make it easy to select an item. If it’s hard to tap an item in your collection, people will get frustrated and lose interest before reaching the content they want. Use adequate padding around content to keep the layout clean and prevent overlapping of content.

Consider using a table instead of a collection for text. It’s generally simpler and more efficient to view and digest textual information when it’s displayed in a scrollable list.

Use caution when making dynamic layout changes. The layout of a collection can be changed at any time. If you dynamically change the layout while people are viewing and interacting with it, be sure the change makes sense and is easy to track. Unmotivated layout changes can make your app seem unpredictable and difficult to use. If context is lost due to a layout change, people are likely to feel like they’re no longer in control.


## (한글 번역)
### 특징

![image](https://user-images.githubusercontent.com/69894461/166132911-555ea90c-2b0e-464f-83d9-73a760e71362.png)

- 정렬된 content Set(ex: photo Set)
- 엄격한 linear format 강요하지 않음
- interactivity( select,edit,swipe to scroll), animation(삽입, 삭제, 재정렬, 커스텀) 지원함

### 가이드라인

- 표준 그리드 레이아웃으로 충분하다면 급진적인 새로운 디자인 피하기

ex: 아이템  탭하면 선택되기, 충분한 패딩, content 겹치기 금지.

- for 텍스트 → 컬렉션 말고 테이블 사용하기
- 동적인 레이아웃 변화를 만들때 신중하기

→ 맥락에 맞게 (이치에 맞게), 따라가기 쉽게 만들기

## Point of this component (이 타이틀은 나중에 결정하시죠)
