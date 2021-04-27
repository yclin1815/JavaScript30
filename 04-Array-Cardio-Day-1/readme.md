## 簡介

共有8個小題目，使用了不同的陣列方法

[Demo](https://yclin1815.github.io/JavaScript30/04-Array-Cardio-Day-1)

## 步驟

#### 1.篩選出1500~1599年出生的inventor

使用`filter()`方法，此方法會將符合條件的資料以陣列回傳。

#### 2.將inventors姓氏與名字組合回傳陣列

用`map()`方法將需要的屬性值組合再回傳。

#### 3.依照出生年份由老排到年輕

`sort()`方法會將陣列中的每個值逐一比對，帶入`(a, b)`兩個參數，以`a - b`或`a > b ? 1 : -1`來判斷，若回傳值是大於 0 ，表示 b 排序在 a 前面，負數則相反，等於 0 表示 a 和 b 排序一樣位置不動。

#### 4.加總所有inventors在世的時間

`arr.reduce(function(accumulator,currentValue,currentIndex,array) {     }, initialValue);`

reduce()方法總共有四個參數，會回傳一個結果的值（不是陣列）：

1. `accumulator`：累加器
2. `currentValue`：當前元素
3. `currentIndex`：當前元素的索引（選擇性）
4. `array`: 呼叫 reduce() 方法的陣列（選擇性）

設定初始值：

* `initialValue`：第一次呼叫時要傳入的累加器初始值。（選擇性）
若沒有提供初始值，則原陣列的第一個元素將會被當作初始的累加器。

#### 5.依照壽命長短排序inventors

做法同第3題，這次要由大排到小所以將ab對調。

#### 6.列出網頁中含有de的路名

用`querySelectorAll()`來取得路名元件，再以`Array.from`將nodeList轉為Array才能使用`map()`方法將字串取出來，最後用`filter()` `includes()`過濾出結果。

#### 7.以姓氏排序

先用`split()`將每個值切開取得姓氏，再用`sort()`排序，最後回傳成陣列。
`split()`帶入的參數值為要當作切分點的字串

#### 8.計算陣列中每個名詞出現的次數

同第4題使用`reduce()`但這次將出使直設定為一個空物件`{}`，然後用一個判斷式來決定加入新的物件屬性或將已建立屬性遞增，最後回傳整個物件。