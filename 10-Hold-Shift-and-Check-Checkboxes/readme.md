## 簡介

使用Shift ＋ 滑鼠左鍵達成一次勾選多個連續的checkbox

[Demo](https://yclin1815.github.io/JavaScript30/10-Hold-Shift-and-Check-Checkboxes)

## 步驟

1. 宣告`shiftClick` `lastClick`兩個變數，存取shift點擊與前一次點擊的DOM元素。

2. 監聽checkbox被點擊時執行`handleCheck`，將判斷條件分成四種狀況，用event物件的shiftKey屬性判斷點擊時是否有按住shift。

* `e.shiftKey && this === lastClick`
按住shift重複點擊同一個checkbox，會造成判斷連續區間的inBetween狀態無法關閉，先將狀況獨立出來，屬於原始的選取行為，不需要執其他行方程式，單純紀錄`shiftClick`。

* `e.shiftKey && this.checked && lastClick`
a. 按住shift點擊且成功勾選，使用`forEach`逐一判斷，第一次遇到`shiftClick`或`lastClick`時，開啟`inBetween`狀態，第二次遇到時關閉，如果`inBetween`狀態被設為開啟即勾選checkbox。
b. 若`lastClick`不存在(即第一次點擊)，不屬於選取區間行為，故不屬於此種狀況。
c. 最後會將此次點擊存入`lastClick`。

* `e.shiftKey && !this.checked`
按住shift點擊且成功取消勾選，執行原理同上。

*  其他狀況
原始選取行為，將元素存入`lastClick`用於下次點擊時比對使用。