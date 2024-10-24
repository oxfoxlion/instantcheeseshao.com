---
title: JavaScript學習筆記1-什麼是變數?變數的命名與型別重點
date: 2024-10-03 14:06:02
tags:
 - Codepen
 - JavaScript
 - 六角學院
 - 網頁開發
categories:
 - 網頁開發
 - 學習筆記
cover: https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/JavaScript1%2FDALL%C2%B7E%202024-10-03%2016.10.55%20-%20A%20notebook-style%20cover%20design%20for%20'JavaScript%20Learning%20Notes'%2C%20featuring%20the%20title%20handwritten%20in%20a%20casual%2C%20personal%20notebook%20style%20at%20the%20center.%20The.webp?alt=media&token=d7c168eb-d4a5-4187-9e25-766f4de88474
---
## JavaScript簡介

我們在前面的文章中有提到HTML用於建立網站的骨架，CSS則是網站的裝潢，今天要說的這個JavaScript則是用於在網站中添加互動性的元素。

舉例來說，迪士尼樂園裡面有一個料理鼠王的設施，有點類似旋轉咖啡杯，但是它會帶你深入料理鼠王的場景，當你搭乘旋轉咖啡杯抵達指定空間時，眼前的大銀幕就會開始演出小米在廚房中四處逃竄躲避廚師的畫面，而當你移動到另外一個房間，天花板上的灑水設備則會自動啟動朝你噴水，模擬小米被水噴到的體驗。

JavaScript的作用就像這個場景，在網站中的某個指定部分觸發互動效果，讓網站不僅是靜態的展示，而是有更多動態與互動的功能。

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/JavaScript1%2FIMG_4243.JPEG?alt=media&token=f17fee88-bf09-4280-80bb-41f90dd552f0)

## 什麼是變數

「變數」在生活中常被用在那些可能會產生變化、或是難以預測的事情上面，如果我今天說「這個活動可能會有變數」，意思是活動可能會暫停、取消或是改期等等，因為有可能不同於原本的計畫，我們就會稱為變數，與那些不會改變的事物做一個對比。

舉例來說舉辦一個活動可能會遇到不同的天候狀況，不同的天候狀況則會使決策團隊決定出不同的結果：晴天的時候我們在草地上進行，雨天的時候則在室內進行，颱風天就取消活動，因此我們就可以將天候狀況制定為一個變數，根據變數改變，我們去制定出一個規則並導出結果，而這個規則就是函式。

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/JavaScript1%2F%E8%9E%A2%E5%B9%95%E6%93%B7%E5%8F%96%E7%95%AB%E9%9D%A2%202024-10-03%20144052.png?alt=media&token=c7621c61-8d3e-49b0-8d33-3bd6055d05e7)

在JavaScript中，可以想像變數就是一個被貼有標籤的資料夾，必須要先去為這個資料夾命名，接著才去放裡面的資料。以天候狀況來說，我們先拿出一個資料夾，命名為天氣，接著在裡面放入寫有當天的天氣的小卡，也就是值(Value)，好讓函式根據這個值去判斷活動該如何進行。

接下來我們就示範一下如何制定變數，而函數我們留到下一次再來討論。

## 如何宣告變數

在JavaScript當中主要有三個方式可以宣告變數(為變數資料夾命名)：

1. let ： 宣告變數之後可以去修改變數的值，類似一個可以隨時替換內容的資料夾，比方說天氣可能一開始是晴天，後來變成雨天了。
```javaScript
let weather = 'sun';
weather = 'rain';
```

2. const ：宣告變數之後就不能夠修改，類似一個上鎖的資料夾，所以通常會放一些比較不會更動的資料，比方說太陽只有一個，或者是披薩的價錢。
```javascript
const sun = 1;
const pizzaPrice = 120;
```

3. var ： 宣告變數之後可以修改，也可以重新命名變數，擁有非常大的彈性，但是越來越少瀏覽器支援了。
```javascript
var num = 1;
var num = 2;
```

## 變數的命名原則

在命名變數時，有一些需要遵守的規則，我在這邊列出來：

* 不可以使用數字作為開頭。
* 不可以使用系統保留字，比方說let、const、var。
* 大小寫視為不同的變數
* 底線與美元符號可以作為開頭或放置於文字中間
* 文字中間不可以使用空白或是特殊字元

### 小駝峰命名法
另外在命名時我們也會為了將語意表達清楚而使用小駝峰命名法，也就是第一個單字以英文小寫開頭，第二個單字起以大寫開頭的命名方式：
* Ex. steakPrice 
就可以很清楚的知道這是牛排的價格

與之相對應則是大駝峰命名法，也就是第一個單字也以大寫開頭，但暫時還不會用到：
* Ex. SteakPrice

## 變數的型別

型別也就是資料的類型，舉例來說，我們存放在電腦資料夾裡的東西可能有圖片檔、文件檔、壓縮檔等不同類別的檔案，變數也有幾種不同的類型，主要分成兩大類，八小類：

### 第一大類：原始型別
* Number：顧名思義就是數字，包含了小數、負數
* String：字串，也就是文字，以```'單引號'```或```"雙引號"```將文字內容包裹起來
* Boolean：不是哥布林的布林，而是是非題，也就是true或false
* Undefined：當我們定義了一個變數，卻沒有給變數一個值的時候，就會顯示undefined，表示未被賦值
* Null：有被賦值，但是被賦予的是空值，就會顯示Null

以下是一個示範，我們可以先進行變數的命名之後，利用```console.log()```來印出該變數的值，也可以使用typeof來查詢變數的型別
大家可以把這段程式碼貼到codepen的javascript區塊，並打開console檢查我的註解與印出來的內容是否相同
值得注意的是null的型別按理來說應該是null，但是因為官方的錯誤，目前還是顯示為object

```javascript
let a = 1; //value為1 型別是Number
let b = 'Shao'; //value為'Shao' 型別是string
let c = true; //value 為 true 型別是boolean
let d; //沒有賦予任何value 型別為undefined
let e = null //有被賦予空值null 型別照理來說應為null 但因為官方錯誤目前顯示object

console.log(a)
console.log(typeof a)

console.log(b)
console.log(typeof b)

console.log(c)
console.log(typeof c)

console.log(d)
console.log(typeof d)

console.log(e)
console.log(typeof e)

```

### 第二大類：物件型別
物件型別包含了陣列與物件，這兩者以typeof查詢型別時都會顯示為object物件型別

* Array：陣列，以中括號紀錄多筆資料如下
```javascript
let arr = [0,1,2];
console.log(typeof arr);
```
* Object：物件，以大括號紀錄多筆帶有屬性的資料如下
```javascript
let obj = {
    name : 'Shao',
    age : 27,
    cats : 2
};

console.log(typeof obj);
```

## 型別的轉型
型別的轉型又有分為顯性轉型與隱性轉型，顯性轉型是指我們透過指令讓變數型別進行轉型，隱性轉型則是按照自動轉型的規則自動進行轉型，因此要特別注意隱性轉型的原則，否則容易造成與設想不同的結果。

### 顯性轉型
這邊示範兩個語法，一個是將數字轉為字串，另一個則是將字串轉為數字，不過其實方法還有很多，依據不同的需求使用不同的方式，這邊就只是簡單列出我所學到的方法而已。
#### Number 轉為 String 的方法
使用```toString()```進行轉型
```javascript
let b = 1; //宣告一個value為1的number型別變數
b = b.toString(); //重新賦值b為b的值轉為string
console.log(b); //查看b的值為'1'
console.log(typeof b); //查看b的型別為string
```

#### String 轉為 Number 的方法
使用```parseInt())```進行轉型
```javascript
let c = "2"; //宣告一個value為"2"的string型別變數
c = parseInt(c); //重新賦值c為c的值轉為number
console.log(c); //查看c的值為2
console.log(typeof c);//查看c的型別為number

let d = "shao";//嘗試看看將真的是文字的string型別變數
d = parseInt(d); //轉換為number
console.log(d);//顯示為NaN，意味著異常狀態
console.log(typeof d);//NaN的型別仍為number
```

### 隱性轉型的原則
在某些情況下JavaScript會自動將我們的變數進行轉型，來看看我目前碰到的一些狀況
```Javascript
let stringAddNumber = '1'+1; //String加上Number時，Number會自動被轉為String，因此這題是'11'而不是2，如果想要得出2，就需要先對number做轉型
let stringTimesNumber = '1'*2//在乘法的情況則相反，string會被視為Number，因此這題是2
let booleanAddBoolean = true + true ; //Boolean和Boolean相加時，true被視為1，False被視為0，因此這題的值為2，型別為number
let booleanAddNumber = true + 10 ; //Boolean加上Number，true被視為1，因此值為11，型別為number
let nullAddNumber = null + 10 ;//null是空值，所以加上Number時以number為主，值為10，型別為number
let nullAddString = null + '10';//但如果是加上String時，又會被視為字串所以結果是'null10',型別為string
```

那麼今天的筆記就先到這邊，謝謝你的閱讀~