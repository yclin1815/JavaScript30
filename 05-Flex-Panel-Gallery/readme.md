## 簡介

用 CSS 的 flex 語法控制 DOM 元素的排列，監聽`click`與`transitionend`事件，新增或移除 class 來製作動畫效果。

[Demo](https://yclin1815.github.io/JavaScript30/05-Flex-Panel-Gallery)

## 步驟

1. 用flex對畫面進行排版
* `justify-content` 分佈方式
* `flex-direction` 直或橫向排列方式
* `flex` flex-grow flex-shrink flex-basis

2. 用偽類別`:nth-child`對特定DOM元素設定位移樣式，再用JS監聽事件新增或移除類別來製作動畫效果

3. 監聽`click`切換`open`類別，修改字體大小和flex比例

4. 監聽`transitionend`，當CSS有transition時才發動，傳入`e.propertyName`判斷包含flex的變化時才切換`open-active`類別

## 補充

* 點擊不同元素時，前一個打開的元素不會自動關閉，宣告一個變數`lastClick`存取前一次點擊的元素，若下一次點擊是不同目標時，會先將前一次的關閉(移除class)。

