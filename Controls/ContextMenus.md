

# [Context Menus](https://developer.apple.com/design/human-interface-guidelines/ios/controls/context-menus/)

## (HIG 원문)
> (영문 내용)
Context Menus
In iOS 13 and later, you can use context menus to give people access to additional functionality related to onscreen items without cluttering the interface.
<img width="338" alt="image" src="https://user-images.githubusercontent.com/64766255/167635962-cc23dc98-6606-43eb-a874-95e1119cfd18.png">

<br></br>
Context menus are similar to Peek and Pop, but with two key differences:
<br></br>
Context menus are available on all devices running iOS 13 and later; Peek and Pop is available only on devices that support 3D Touch.
Context menus immediately display contextually relevant commands; Peek and Pop requires a swipe up to view commands.
To reveal a context menu, people can use the system-defined touch and hold gesture or 3D Touch (3D Touch can make context menus appear more quickly). When open, a context menu displays a preview of the item and lists the commands that act on it. People can choose a command or drag the item to another area, window, or app.
<br></br>
Adopt context menus consistently. If you provide context menus for items in some places but not in others, people won’t know where they can use the feature and may think there’s a problem with your app.
<br></br>
Include only the most commonly used commands that apply to the item. For example, in the context menu for a Mail message, it makes sense to include commands for replying and moving the message, but it doesn’t make sense to include formatting or mailbox commands. Listing too many commands can overwhelm people.
<br></br>
Include a glyph with each command in a context menu. A glyph reinforces the meaning of a command, helping people instantly understand its function. When you use SF Symbols, you can choose an existing symbol that represents your command or edit a related symbol to create a custom glyph. If your context menu includes a submenu, you don't need a glyph for it because it automatically displays a system-provided chevron symbol that indicates the presence of additional commands.
<br></br>
Use submenus to manage complexity. A submenu is a context menu item that reveals a secondary menu of logically related commands. Give submenus intuitive titles that describe their contents so people can predict the submenu's commands without revealing them. Concise, action-oriented titles also let people skip over submenus they don’t need in their current context.
<br></br>
Keep submenus to one level. Although submenus can shorten a context menu and clarify the commands that people can perform, more than one level of submenu complicates the experience and can be difficult for people to navigate.
<br></br>
Place the most frequently used items at the top of the menu. When people open a context menu, their focus is on the top area of that menu. Placing the most common items at the top of the menu helps people find the item they’re looking for.
<br></br>
Use separators to group related menu items. Creating visual groupings can help people scan a menu more quickly. For example, you might use a separator to group actions related to editing the item and another to group actions related to sharing the item. Typically, you don’t want more than three groups in a context menu.
<br></br>
Avoid providing a context menu and an edit menu for the same item. It can be confusing to people and hard for the system to detect intent when both features are enabled for the same item. For additional guidance, see Edit Menus.
<br></br>
Avoid providing an action button that opens the item preview. People can tap to open the item they’re previewing, so there’s typically no need to provide an explicit Open button.
<br></br>
For developer guidance, see UIContextMenuInteraction.

---
## (한글 번역)
Context Menus
iOS13부터, Context Menu 를 통해 유저가 스크린상의 아이템과 관련된 추가적인 기능에 접근할 수 있다.

Context menu 는 Peek 과 Pop 과 비슷하지만 두가지 차이점이 있다.
- Context menu는 iOS13 이상에서 적용되고, Peek 과 Pop 은 3D 터치를 지원하는 기기에서만 적용가능하다.
- Context menu는 문맥적으로 관련된 명령들을 바로 보여주고, Peek 과 Pop 은 명령들을 보기 위해 스와이프업을 필요로 한다. 

Context menu를 나타내기 위해선, 시스템 정의된 터치, 홀드 제스쳐, 3D 터치 (더욱 빠르게 Context menu가 나타남)를 사용할 수 있다. 메뉴가 열렸을 때, Context menu는 해당 아이템의 프리뷰와 작동 가능한 명령들의 리스트를 보여준다. 사용자는 명령을 선택하거나 아이템을 드래그 하여 다른 영역, 윈도우 또는 앱으로 이동시킬 수 있다.

### Context menu 를 일관되게 적용하자.
만약 Context menu를 일부 영역에만 적용시키면, 사용자는 어느 영역에서 기능을 사용할 수 있는지 알 수 없고 앱에 문제가 있다고 생각할 수 있다.

### 해당 아이템에 가장 흔하게 사용되는 명령만을 포함하자.
예를 들어, 메일 메세지의 Context menu에서 메세지 답장, 이동을 포함하는 것은 자연스럽지만 formatting, mailbox 명령을 포함하는 것은 부자연스럽다. 또한 너무 많은 명령을 나타내는 것은 사용자를 부담스럽게 한다.

### 각 명령에 하나의 심볼(아이콘)을 포함하자.
심볼(아이콘)은 명령의 의미를 강조해 사용자가 즉각적으로 해당 기능을 이해할 수 있게 해준다. SF Symbols 을 통해 저장된 기존 심볼들과 커스텀 심볼을 사용할 수 있다. 만약 Context menu가 보조항목(서브메뉴)를 포함한다면, 시스템 내장된 chevron 심볼을 통해 추가적인 명령들을 나타내기 때문에 심볼(아이콘)을 필요로하지 않는다.  

### 복잡성을 관리하기 위해 보조항목(서브메뉴)를 사용하자.
보조항목(서브메뉴)은 논리적으로 연결된 명령에 부차적으로 나타나게 된다. 사용자가 보조항목(서브메뉴)에 진입하지 않아도 해당 명령들을 예상할 수 있게 보조항목(서브메뉴)에 직관적인 제목을 붙여주자. 간결하고 행동지향적인 제목은 사용자가 현재 필요로 하지 않는 보조항목(서브메뉴)를 스킵할 수 있게 해준다.

### 보조항목(서브메뉴)는 한단계만 유지하자.
비록 보조항목(서브메뉴)가 Context menu를 간결하게 해주고 유저가 행할 수 있는 명령을 명확하게 해주지만, 한계층 보다 많은 경우 사용자 경험을 복잡하게 하고 이동에 어려움을 초래한다.

### 가장 자주 사용되는 아이템을 메뉴 제일 위에 위치시키자.
사용자가 Context menu 를 열 때, 가장 상단의 메뉴 항목에 집중된다. 가장 자주 사용되는 아이템을 메뉴 제일 위에 위치시키는 것은 사용자가 그들이 원하는 기능을 원활히 찾도록 도와준다.

### Separators 를 사용해 관련된 메뉴 항목을 그룹화 하자.
시각적인 그룹화는 사용자가 메뉴를 빠르게 살필 수 있도록 도와준다. 예를 들어, separator를 통해 아이템을 수정하는 명령들과 공유하는 명령들을 구분해서 그룹화할 수 있다. 일반적으로, Context menu에서 3개 이상의 그룹을 사용하지 않는다.

### Context menu 와 Edit menu 를 동시에 제공하는 것을 피하자.
한 아이템에 Context menu 와 Edit menu 를 동시에 제공하는 것은 사용자를 혼란스럽게 하고 시스템적으로 의도를 파악하는데 어려움을 준다.
* Edit menu
<img width="352" alt="image" src="https://user-images.githubusercontent.com/64766255/167636031-d13dc96b-e7b8-44bf-ac0a-bd6598058218.png">

### 아이템 프리뷰를 오픈하는 버튼의 사용을 피하자.
사용자는 탭(터치)을 통해 아이템을 열어 프리뷰할 수 있으므로, 명백하게 오픈 버튼을 필요로 하지 않는다.



---
