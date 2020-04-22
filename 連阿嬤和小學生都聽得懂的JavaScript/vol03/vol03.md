# 連阿嬤和小學生都聽得懂的程式語言 - JavaScript
## JavaScript 基礎篇 - 資料型態篇 - 字串、數字

聊完了變數之後，我們來了解JS裡面有哪些資料型態吧。  
JS裡面的資料型態有7種：
1. 字串 string
2. 數字 number
3. 布林 boolean
4. 未定義 undefined
5. 陣列 array
6. 物件 object  

前面4種屬於基本形態，後面2種則是引用型態(各位可以理解成進階型態)。

### 字串、數字
```javascript
var name = 'Kevin'; // 聲明一個變數叫做名字(name)，且它的值為'Kevin'
var location = 'Taipei'; // 聲明一個變數叫做地點(location)，且它的值為'Taipei'
var chineseName = '小明'; // 聲明一個變數叫做中文名字(chineseName)，且它的值為'小明'
var store = "Starbucks 星巴克"; // 聲明一個變數叫做店(store)，且它的值為'Starbucks 星巴克'
```

&nbsp;&nbsp;用單引號(' ')或雙引號(" ")所包覆起來的，稱為**字串**。字串可以是任何字母的組合，可以和數字、特殊符號(例如：?!@#$%等等)與字母的組合，也可以混和空白在裡面(例如上面例子中Starbucks與星巴克之間)，只要前後用一組單引號(或雙引號)包起來，就是一組字串。必須注意的是，開頭與結尾的引號必須一致：單引號開頭就得用單引號結尾
```javascript
var place = 'Home'; // 合法的字串
var place2 = 'House"; // 不合法的字串
var place3 = 'I live in "Taipei"'; // 合法的字串
```
&nbsp;&nbsp;上面的例子中，可以看到 *place2* 的字串是不合法的。由於沒有用單引號結尾，電腦會認為你的字串還沒結束，導致後面 // 之後的注釋也被判別為前面字串的一部分(看顏色可以區分)  
&nbsp;&nbsp;如果想要在字串裡面使用引號的話，必須用和開頭結尾不一樣的引號，例如上面的 *place3*。

```javascript
var number = 10;
```
&nbsp;&nbsp;變數除了能存字串之外，也能存數字。變數裡存數字除了方便做運算之外，有時因為程式的需求，需要做些改變，使用變數會顯得非常方便。  
例如：
```javascript
var cost = 100; // 聲明一個變數cost，值為100
var discount = 0.95; // 聲明一個變數discount，值為0.95
if(discount > 0.9) { // 如果discount大於0.9
    cost = cost * 0.9; // cost等於 100 * 0.9
} else { // 否則的話...
    cost = cost * discount; // cost等於 100 * discount裡面的值
}
```
以上是一個很簡單的流程控制，後面會再詳細的介紹。程式碼不難，一行一行看下來，可以簡單拆解成：
1. 聲明一個變數叫做cost，且值等於100
2. 聲明一個變數叫做discount，且值為0.95
3. 進入條件式if判斷：
    1. 如果discount的值大於0.95的話，則cost將重新計算為100 * 0.9
    2. 否則的話(也就是discount並沒有大於0.9)，則將cost重新計算為100 * discount的值。(* <- 這是四則運算乘號)

以上為了方便展示，將discount和cost都寫成固定值了。想像一下如果這是一個大賣場算折扣的計算機程式，discount一般來說都會是由賣場人員輸入的，程式經過判斷之後再去算出應該要付多少錢。使用變數將我們要計算的值存進去將會非常方便。