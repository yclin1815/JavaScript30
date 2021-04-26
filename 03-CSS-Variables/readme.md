## 簡介

使用CSS variable定義樣式，配合JS即時套用新的數值，讓使用者可以修改畫面上的CSS樣式。

[Demo](https://yclin1815.github.io/JavaScript30/03-CSS-Variables)

## 步驟

1. 用`var(--指定變數)`設定CSS樣式
2. `querySelectorAll`取得使用者可操作的元素
3. `forEach`監聽所有變動事件，執行`update()`
4. `setProperty`修改CSS變數值

## 補充

*新增grayscale變數，增加一個濾鏡效果