


# Tables

## (HIG 원문)

A table presents data as a scrolling, single-column list of rows that can be divided into sections or groups. Use a table to display large or small amounts of information cleanly and efficiently in the form of a list. Generally speaking, tables are ideal for text-based content, and often appear as a means of navigation on one side of a split view, with related content shown on the opposite side. For guidance, see Split Views.

iOS provides three styles of table: plain, grouped, and inset grouped.

Plain. Rows can be separated into labeled sections, and an optional index can appear vertically along the right edge of the table. A header can appear before the first item in a section, and a footer can appear after the last item.

Partial screenshot of the Mailboxes screen in the Mail app, which uses a plain table to list several items.
Grouped. Rows are displayed in groups, which can be preceded by a header and followed by a footer. This style of table always contains at least one group and each group always contains at least one row. A grouped table doesn’t include an index.

Partial screenshot of Driving and Navigation settings for the Maps app, which uses a grouped table to list types of roads to avoid separately from items to be shown in navigation.
Inset grouped. Rows are displayed in groups that have rounded corners and are inset from the edges of the parent view (as shown on the right of the image above). This style of table always contains at least one group and each group always contains at least one row and can be preceded by a header and followed by a footer. An inset grouped table doesn’t include an index. The inset grouped style works best in a regular width environment. Because there's less space in a compact environment, an inset grouped table can cause text wrapping, especially when content is localized.

Screenshot of Sound settings on iPad. The left view is a plain table of top-level settings in which Sound is selected. On the right is the Sound settings detail view, which uses the inset grouped table style to separate settings into three groups.
Think about table width. Thin tables can cause truncation and wrapping, making them hard to read and scan quickly at a distance. Wide tables can also be difficult to read and scan, and can take away space from content.

Begin showing table content quickly. Don’t wait for extensive table content to load before showing something. Fill onscreen rows with textual data immediately and show more complex data—such as images—as it becomes available. This technique gives people useful information right away and increases the perceived responsiveness of your app. In some cases, showing stale, older data may make sense until fresh, new data arrives.

Communicate progress as content loads. If a table’s data takes time to load, show a progress bar or spinning activity indicator to reassure people that your app is still running.

Keep content fresh. Consider updating your table’s content regularly to reflect newer data. Just don’t change the scrolling position. Instead, add the content to the beginning or end of the table, and let people scroll to it when they’re ready. Some apps display an indicator when new data has been added, and provide a control for jumping right to it. It’s also a good idea to include a refresh control, so people can manually perform an update at any time. See Refresh Content Controls.

Avoid combining an index with table rows containing right-aligned elements. An index is controlled by performing large swiping gestures. If other interactive elements reside nearby, such as disclosure indicators, it may be difficult to discern the user’s intent when a gesture occurs and the wrong element may be activated.

For developer guidance, see UITableView.
 


## (한글 번역)
>### 특징
- 데이터를 스크롤 할 수 있고, 섹션 혹은 그룹으로 나뉘어지는 여러 행, 하나의 열의 리스트로 보여준다.

- 테이블은 텍스트기반의 콘텐츠가 이상적
- 스플릿뷰의 한사이드에서 네비게이션의 수단으로 종종 사용됨.
![image](https://user-images.githubusercontent.com/69894461/167611893-2fcce708-e036-4d82-84a7-4754aebbfc02.png)

>### 테이블 스타일
1. ### plain
- index 표기 (optional)
![image](https://user-images.githubusercontent.com/69894461/167611964-5a099917-cbce-4341-9c9b-1d8accf2f62f.png)

2. ### grouped
- index 표기 포함x
![image](https://user-images.githubusercontent.com/69894461/167612085-cf9b81b7-77a1-4db2-9359-a2e549bbd8ef.png)


3. ### inset grouped
- index 표기 포함x
- a regular width environment에 적합
- compact environmet에서는 원치않은 텍스트 줄바꿈이 일어날 수 있음. especially when content is localized
(각 디바이스에 content가 적용될 때로 생각했음.) 
 
![image](https://user-images.githubusercontent.com/69894461/167612155-22aa0f03-fef8-40f9-9b9e-7834045fd493.png)
![image](https://user-images.githubusercontent.com/69894461/167612199-a2a71875-7c9d-4e74-8c99-310d4ed4ba59.png)


>### 가이드라인
<br>
### **테이블의 너비 생각하기**

- 너무 너비가 작으면 콘텐츠 절단 및 줄바꿈이 발생함

  → 읽기 어렵고 약간 멀리서 스캔하기가 어려움.

### **가능한 빨리 테이블 콘텐츠를 보여주어라.**

- 많은 테이블 콘텐츠를 보여주려고 로딩하게 만들지마라.
- 텍스트 데이터를 즉시 보여주고,, 그 다음에 이미지같은 복잡한 데이터를 보여지도록 하기

### **콘텐츠가 로딩중일 때는 프로그래스바 혹은 인디케이터를 보여주라.**

### **항상 최신콘텐츠를 유지하라.**

- 업데이트 될때 스크롤링 위치는 변하지 않게하기

→ 새로운 데이터를 처음 혹은 끝에 추가하기.

- 새로운 데이터 추가가 끝나면 스크롤 가능하도록
- 새로고침 컨트롤을 만드는 것도 좋은 아이디어

### **오른쪽배치의 원소들이 있는 테이블 행들에 index를 결합하는 것을 피하라.**

- 인덱스는 large 스와이핑 제스처s에 의해 컨트롤됨
- 그래서disclosure indicator같은 것이 옆에 있다면 유저의 의도를 파악하기 어려움. → 인덱스를 조작하기 위함인지, disclosure를 위함인지.

→ 완벽히 이해 못함.

### Table Rows
### 구성
1. ### Basidc
- 왼쪽 optional 이미지, 왼쪽 정렬 타이틀
![image](https://user-images.githubusercontent.com/69894461/167613070-01cc1d7e-504d-496c-bd52-b38972f58716.png)


2. ### Subtitle
- 시각적으로 유사한 rows를 구분지울 수 있음

![image](https://user-images.githubusercontent.com/69894461/167613101-28384071-0d1b-47d3-a37c-65dedb3ddc6a.png)

3. ### Right Detail
![image](https://user-images.githubusercontent.com/69894461/167613165-3f490c39-81de-4f14-a26d-7f9b703cf7ac.png)


4. ### Left Detail
![image](https://user-images.githubusercontent.com/69894461/167613223-269e2bfc-6421-4d5a-a6e4-28da40b7c70a.png)



### **잘림을 피하기 위해 텍스트를 간결하게 하라.**
<br>

### **삭제버튼을 위한 커스텀 타이틀을 이용하는 것을 고려하라.**

만약 하나의 행이 제거기능을 제공하고 이가 명확성을 제공한다면

시스템에서 제공되는 delete 타이틀을 커스텀 타이틀로 대체하라.

—> 예시가 필요하다..

### **콘텐츠를 선택하면 피드백을 제공하라.**

- 새로운 뷰를 보여주던가 혹은 어떤것이 바뀌도록 하라.

### **표준이 아닌 테이블 행들은 커스텀 테이블 셀 스타일로 디자인하라.**


## Point of this component (이 타이틀은 나중에 결정하시죠)
