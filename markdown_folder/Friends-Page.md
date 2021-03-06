<link href="md_config/style.css" rel="stylesheet" />

# Cocoatalk - actual

Git repo for cocoatalk webpage

## 1) Position

- Fixed + (top, bottom, right, left) + (width, height)
- 요소가 표시되는 지점을 옮기는 것뿐

## 2) Box-sizing

<img src='images/2021-09-05-20-17-15.png' /> 
<img src='images/2021-09-05-20-21-06.png' />
<img src='images/2021-09-05-20-20-44.png' />

<br>

- [참조링크 MDN](https://developer.mozilla.org/ko/docs/Web/CSS/box-sizing)
- Example

  ```CSS
    xxx {
      box-sizing: border-box;
    }
  ```

- 위 box-sizing 결과
  1. 결과적으로 padding 무시하도록 할 수 있게 됨
  2. padding / borderline 등을 쓰면 width, height가 정애진 상태에서 자동으로 그만큼 box 영역이 커지는데, 이를 방지할 수 있음
     - 보통 width, height는 원래 content 영역 크기를 지정하기 때문

## 3) flex and span

- Span 은 원래 width, height 줄 수 없는데, flex property 부과하면 줄 수 있게 됨  
  -> display: block / display: inline-block

## 4) Position sticky + value

- This will stick the element in a given position relative to screen(Offset) and then it will be sitcked to that position

- CSS

  ```CSS
    .status-bar {
      display: flex;
      justify-content: center;
      padding: 5px 3px;

      position: -webkit-sticky;
      position: sticky;
      top: 0rem;
      margin-bottom: 0.2rem;
      /* top: 0;
      width: 100%; */
      background-color: ivory;
      font-size: 1.3rem;
    }
  ```

## 5) em, rem

[중요 참조링크](https://medium.com/watcha/watcha-%EA%B0%9C%EB%B0%9C-%EC%A7%80%EC%8B%9D-px-em-rem-f569c6e76e66)
[참조 링크1](https://www.codingfactory.net/10748)

## 6) Always, before creating Something

- See if you can reuse that element
- if yes, it should be made as a component style in CSS

## 7) apply same for 2 elements in CSS

- CSS
  ```CSS
    .user-display,
    .user-display--columns.main {
      display: flex;
      align-items: center;
    }
  ```
