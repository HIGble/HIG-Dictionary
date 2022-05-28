# Text Fields

Author: 익명 <br/>
Status: Complete<br/>
Tags: Controls<br/>
속성: 2022년 5월 25일 오후 2:46<br/>
원문: https://developer.apple.com/design/human-interface-guidelines/ios/controls/text-fields/<br/>
참고: https://www.notion.so/Text-Fields-fa5ab227ca49415f8bf6cf571e146f1b<br/>

# Overview

---

- 높이값이 고정되어있고, 한 줄로 되어있다.
- text field를 탭하면 키보드를 자동으로 올라오게 한다.
    - (cf) 과거에는 often with rounded corners가 있던 것 같지만, 현재는 아래 영역을 모두 채우는 듯하다.
- 이름이나 이메일 주소와 같은 소량의 정보를 요청할 때 text field를 사용하라.

[예시] (왼쪽)이름/이메일 주소 입력  (오른쪽)검색창(App Store)

![스크린샷 2022-05-25 오후 3.01.23.png](Text%20Fields%20c4e763490fb7495581b62d0803b7ca5d/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-05-25_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_3.01.23.png)

[Text field example.MP4](Text%20Fields%20c4e763490fb7495581b62d0803b7ca5d/Text_field_example.mp4)

# Guideline

---

- **목적을 잘 전달하기 위해 힌트를 보여줘라.**
    - text field는 필드 안에 다른 텍스트가 없다면, placeholder text(입력 전 영역 안에 보이는 회색 글씨)를 추가할 수 있다.
    - placeholder text로 설명이 충분하면 label을 별도로 사용하는 것을 피한다.
- **텍스트필드의 오른쪽 끝에 지우기(클리어) 버튼을 표시하여 사용자가 입력한 내용을 지울 수 있도록 하라.**
    - 사용자가 탭 한 번으로 Delete버튼을 사용하지 않고도 text field에 입력한 내용을 모두 지울 수 있다.
- secure text fields를 사용하여 개인정보를 숨겨라.
    - 비밀번호와 같은 예민한 정보에 대해서는 항상 secure text field를 사용해야한다.
    - [예시] youtube 로그인 화면
        - (cf) 최근에 보면 체크박스를 통해 비밀번호가 보이는 기능도 추가를 했다. 다만, 디폴트는 항상 hide이다.
        
        [Secure text field example.MP4](Text%20Fields%20c4e763490fb7495581b62d0803b7ca5d/Secure_text_field_example.mp4)
        
- **이미지와 버튼을 사용하여 text field의 명확성과 기능을 제공하라**
    
    ![스크린샷 2022-05-25 오후 3.29.22.png](Text%20Fields%20c4e763490fb7495581b62d0803b7ca5d/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-05-25_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_3.29.22.png)
    
    - Text field의 양 끝에 커스텀 이미지나 시스템에서 제공하는 버튼(eg. 북마크)을 넣을 수 있다.
    - 보편적으로는 왼쪽끝에는 필드의 목적을 알려주고, 오른쪽 끝에는 북마크와 같은 추가적인 기능들을 넣는다.
        - “북마크”를 계속 HIG에서 예시로 주는데, 이는 iOS보다는 웹에서 더 맞는 기능이 아닐까 싶습니다…
            
            ![스크린샷 2022-05-25 오후 3.37.43.png](Text%20Fields%20c4e763490fb7495581b62d0803b7ca5d/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-05-25_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_3.37.43.png)
