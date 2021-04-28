## 簡介

介紹Chrome中一些console的用法，適合用在除錯、觀察程式碼跑的流程，以及呈現資料

[Demo](https://yclin1815.github.io/JavaScript30/09-Dev-Tools-Domination))


### Breakpoints

中斷點有三種觸發模式(可複選)：

1. `subtree modifications` 當添加、改變、刪除子元素時觸發
2. `attributes modifications` 當元素屬性發生改變時觸發
3. `node removal` 當移除元素時觸發

在console對選取的元素按下`右鍵 > Break on...`選擇

### Console

1. `console.log()` 一般輸出
2. `console.log('%s', '參數')` %s可輸出後方參數的值
3. `console.log('%c', 'style')` %c使輸出帶有後方CSS樣式
4. `console.warn()`顯示驚嘆號icon
5. `console.error()`顯示叉叉icon
6. `console.assert( , '')`判斷true & false，如果是false就輸出後方錯誤訊息
7. `console.clear()`清除console的所有訊息
8. `console.dir()`輸出選取物件的所有屬性
9. `console.group() && console.groupCollapsed()`把輸出的資訊群組起來
10. `console.count()`顯示累加數量
11. `console.time() & console.timeEnd()`計算區域內執行的時間
12. `console.table()`將輸出繪製成表格

