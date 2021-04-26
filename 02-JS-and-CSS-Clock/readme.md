## 簡介

使用JS與CSS製作指針時鐘

[Demo](https://yclin1815.github.io/JavaScript30/02-JS-and-CSS-Clock)

## 步驟

1. 使用CSS設定指針樣式
* `transition-timing-function`貝茲曲線調整動畫速度
* `transform-origin`旋轉軸心
2. `new Date()`取得現在時間，算出指針角度存入常數
3. `setInterval(setClock, 1000)`每秒更新一次

## 補充

當指針繞一整圈，最後一次動畫效果實際上是逆時針旋轉，造成指針跳動不自然的畫面

* 使用`if`判斷當角度為90度時，當次取消動畫效果