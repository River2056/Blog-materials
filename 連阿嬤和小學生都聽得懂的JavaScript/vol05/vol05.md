# 連阿嬤和小學生都聽得懂的程式語言 - JavaScript
## JavaScript 基礎篇 - 資料型態篇 - 陣列

### 陣列
&nbsp;&nbsp;陣列可以說是JS裡面最常用的資料型態之一了，跟陣列本身相關的函式(後面會提到)也非常的多。可以說能不能成為JS達人，對陣列的了解非常的關鍵。首先來看一下陣列長怎樣吧!
```javascript
var arr = [1, 2, 3, 4, 5]; // 聲明一個陣列叫做arr，裡面的值都為數字

var arr2 = ['egg', 'apple', 'carrots', 'banana', 'tomatoes']; // 聲明一個陣列叫做arr2，裡面的值都是字串

var arr3 = [23, 'Taiwan', 527, 10, 'Taipei']; // 聲明一個陣列叫做arr3，裡面放了各種值，包含字串與數字
```
&nbsp;&nbsp;用方括號框起來即為陣列，裡面的元素則用逗號隔開。陣列的好處是，可以讓你將相關的元素放進同一個群組裡面，就像一個籃子，裡面裝你想裝的東西。  
&nbsp;&nbsp;當你發現寫程式時，聲明了很多變數去儲存各種不同的值時，這時你可以將這些值都裝進一個陣列裡面。除了讓程式碼更好理解之外，也能節省一些由於過多變數造成的記憶體浪費。  
&nbsp;&nbsp;那麼陣列裡的值要怎麼取出來使用呢?
```javascript
// 假如想取arr裡面的1時
arr[0] // 結果為1

// 假如想取arr裡面的3時
arr[2] // 結果為3

// 想取出arr3裡的'Taiwan'時
arr3[1] // 結果為'Taiwan'
```
從上面的結果中，有沒有發現規律呢? 陣列的起始值是從0開始算的。所以第一個元素在陣列裡，位置是0。要取出陣列裡的值，只要在變數後面的方括號裡，寫上索引值，就能順利取出。

一般來說，一個陣列我們通常會放同性值的東西，所以上面的*arr3*不太常看到，但是要在裡面放什麼，確實是沒有限制的，甚至你在陣列裡，再放一個陣列也行，例如：
```javascript
var expenses = [
    ['rent', 'electricity', 'food'],
    [6500, 1500, 8000],
    ['Kevin', 'Jerry']
];

var dailyExp = [
    '20200401', [100, 80, 280], '20200402', [120, 80, 300]
];
```
expenses這個陣列放了三個小陣列, dailyExp則是字串參雜小陣列。如果要取出裡面的值的話...
```javascript
// 取出expenses裡的'rent'
// 由於rent在第一個小陣列裡面
// 所以應該先取出第一個陣列，在用索引值取出'rent'
expenses[0] // 取出陣列['rent', 'electricity', 'food']
expenses[0][0] // 取出第一個陣列裡的第一個元素，也就是'rent'

// 隨堂小練習
expenses[1][2] // 請問結果是什麼呢?
dailyExp[3][1] // 請問結果是什麼呢?
```
上面的例子有兩層陣列，要再追加第三、第四層也是沒問題的，這樣複雜度會增加，寫程式時也容易搞混，所以通常不建議這麼做。