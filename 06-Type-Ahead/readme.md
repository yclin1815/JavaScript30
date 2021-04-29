## 簡介

使用`fetch()`接收json，找出包含關鍵字的資料，使用正則表達式處理字串，用template literal渲染到html中


[Demo](https://yclin1815.github.io/JavaScript30/06-Type-Ahead)

## 步驟

1. 將`fetch()`取回的json資料轉化後存進cities陣列

2. `findMatches(wordToMatch, cities)`過濾出陣列中包含wordToMatch的資料
* 先用new建立正則表達式物件`RegExp(wordToMatch, 'gi')`，g代表全部資料、i代表不分大小寫
* 與 city || state 對比後將符合的回傳

3. 監聽輸入欄位變動時執行`displayMatches()`，將`findMatches()`回傳陣列使用map方法做以下處理

* 先將地名中符合關鍵字串的部分用高亮樣式替代`<span class="hl">${this.value}</span>
* 將替代完成的字串做成html所需的template literal格式回傳
* 最後使用innerHTML方法渲染元素中

4. 前一步的template literal中所使用的人口數資料使用`numberWithCommas()`調整格式加入千分位','

* toString().replace(/\B(?=(\d{3})+(?!\d))/g, ',')
