# Image Views

## HIG 원문
> An image view displays a single image or an animated sequence of images over a transparent or opaque background. Within an image view, images may be stretched, scaled, sized to fit, or pinned to a specific location. Image views are noninteractive by default. <br><br>
If possible, make sure all images in an animated sequence are consistently sized. Ideally, images should be prescaled to fit the view so the system doesn't have to do any scaling. If the system must perform scaling, it's easiest to achieve the desired results when all images are the same size and shape. <br><br>
For developer guidance, see UIImageView. <br><br>
**NOTE**<br>
An image that’s been configured as a template image discards its color and adopts any tint that’s been applied to the enclosing image view. See Custom Icons. For developer guidance, see UIImageRenderingModeAlwaysTemplate in UIImage.

<br>

## 번역
**이미지 뷰**는 하나의 이미지 또는 이미지의 [애니메이션 시퀀스](https://www.youtube.com/watch?v=epiGRw0CNSs) 를 투명하거나 또는 불투명한 배경 위에 보여준다. 이미지 뷰 내에서, 이미지를 늘리거나, 크기를 변경하거나, 사이즈를 맞추거나, 크기에 맞게 조정하거나 또는 특정 위치에 맞게 고정할 수 있다. 이미지 뷰는 기본적으로 상호작용을 하지 않는다. 

가능하다면, 반드시 애니메이션 시퀀스에 있는 모든 이미지들을 동일한 사이즈로 만들어라. 이상적으로, 이미지는 시스템이 크기를 조정할 필요가 없도록 미리 크기가 조정이 되어있어야 한다. 시스템이 크기를 조절해야만 한다면, 모든 이미지들이 같은 모양과 크기를 가지는 것이 원하는 결과를 얻는 가장 쉬운 방법이다.

템플릿으로 설정된 이미지는 이미지가 지니고 있던 색상을 버리고 이미지를 둘러싸고있는 뷰에 적용된 색상이 적용된다.

- **애니메이션 시퀀스란?**<br>
애니메이션이 실행되는 일련의 과정을 의미한다. 애니메이션 기능이 추가된 이미지라고 생각하면 될 듯하다.
- **UIImageRenderingModeAlwaysTemplate?**<br>
Always draw the image as a template image, ignoring its color information. <br>
: 이미지가 가진 색상 정보를 무시하고 템플릿 이미지로 그린다.


<br>

## 결론
이미지는 정보를 시각적으로 보여주는 콘텐츠를 의미한다. HIG에서 말하는 이미지 뷰는 이미지 자체만을 가진 하나의 뷰라고 생각된다. 이미지 뷰의 기본 설정으로 유저와 상호작용을 하지 않도록 되어있다. 이미지 뷰는 어떤 내용을 시각적으로 보여주는 용도로만 사용해야지 유저와의 상호작용을 위한 동작을 넣어서는 안된다는 의미를 내포하고 있는 것으로 보인다.

일련의 과정에 있는 애니메이션을 적용할 때는 애니메이션이 적용되는 이미지들은 전부 같은 크기로 하는 것을 권장한다.


<br>

## 예시


<br>

## 구성요소
UIKit - [UIImageView](https://developer.apple.com/documentation/uikit/uiimageview)<br>
SwiftUI - [Image](https://developer.apple.com/documentation/swiftui/image)