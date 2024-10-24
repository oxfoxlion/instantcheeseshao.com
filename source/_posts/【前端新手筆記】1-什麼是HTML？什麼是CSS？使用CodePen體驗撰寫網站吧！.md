---
title: 【前端新手筆記】1-什麼是HTML？什麼是CSS？使用CodePen體驗撰寫網站吧！
date: 2024-05-21 22:06:40
tags:
 - Codepen
 - CSS
 - HTML
 - 六角學院
 - 網頁開發
categories:
 - 網頁開發
 - 學習筆記
cover: https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E4%BB%80%E9%BA%BC%E6%98%AFHTML%E3%80%81CSS%2F1.jpg?alt=media&token=1181bfd4-543c-4f4d-b250-33fcdeedf747
---
## 前言

今年4月底，我報名了六角學院的2024軟體工程師體驗營，成為了我學習網站前端設計的起點。

這個課程原價799元，因為剛好有追蹤柚智夫妻這個粉專，就用他們提供的折扣碼，買到了699元的課程。這個課程涵蓋60個小時從HTML、CSS到JavaScript的超完整教學影片，加上每週校長的直播課程、認真經營的Discord社群，甚至還有助教逐一批改作業並提供結業證書，超級精實的內容，剛好遇上我離職的這段期間，就決定要放下一切認真學習了。

歡迎來到即溶啟思！我是站長 邵Shao，我喜歡閱讀、喜歡學習，而這是我練習輸出所學的一個平台，我在這裡試著用最簡單的方式，分享啟發思考的知識，而我今天要跟大家分享什麼是HTML，和CSS有什麼差別？

## 什麼是HTML？

HTML簡單的來說就是**網站的骨架**，我們可以透過HTML的語法來告訴瀏覽器，我的網站放入了**哪些內容**以及這些內容的**結構**，好讓瀏覽器知道該如何顯示我的內容。

## 什麼是CSS？

如果HTML是網站的骨架，CSS就好比是**網站的裝潢**，決定了網站的外觀；舉例來說，我們透過HTML插了一塊寫有網站標題的門牌，CSS則決定這塊門牌應該要長成什麼樣子，包含顏色、字體、裝飾等等。

## 圖示HTML與CSS之間的關係

接下來我想透過一張圖片來加深大家對於HTML與CSS分工的印象，請見下圖：

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E4%BB%80%E9%BA%BC%E6%98%AFHTML%E3%80%81CSS%2F1.jpg?alt=media&token=1181bfd4-543c-4f4d-b250-33fcdeedf747)

從這張圖應該大概可以理解，HTML是建築師，負責將房子蓋好，至於房子最終應該要長成什麼樣子，還是要看CSS這位裝潢師傅怎麼設計了。而這兩者是互相協作的關係，就好像在蓋房子之前，我們就會先規劃房子要長成什麼樣子，好讓建築師去設計架構，而裝潢師傅再依據架構去裝潢。同理CSS在裝潢網站時需要依據HTML當中的架構來撰寫相應的程式碼，HTML也需要根據網站最終希望長成什麼樣子，來撰寫適合CSS的架構。

## HTML和CSS實際上是如何協作的呢？

### 運用CodePen來體驗

這個部分我們可以透過 [codePen](https://codepen.io/) 這個網站來淺淺的體驗一下HTML與CSS的撰寫方式。

首先進到[CodePen](https://codepen.io/)首頁，並點選右上角Sing Up註冊，如果已經有帳號的話，點選Log In就可以囉。

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E4%BB%80%E9%BA%BC%E6%98%AFHTML%E3%80%81CSS%2F2.png?alt=media&token=cf4cbf18-290f-4a77-a68c-becc5241b55d)

登入之後，就可以看到如下方的畫面：紅色框的部分是Pens，也就是我已經建立的CodePen檔案，那我們點選左邊用黃色框起來的這個Pen就可以開啟新的CodePen檔案了。

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E4%BB%80%E9%BA%BC%E6%98%AFHTML%E3%80%81CSS%2F3.png?alt=media&token=e4c02245-3d2b-4d0d-9c28-9f3a919baacc)

開啟之後，首先看到左手邊有三個區塊，分別為HTML、CSS、JS，也就是決定網站的三個關鍵組成部分。

我們今天主要是要講HTML和CSS，所以只會用到上面的這兩個區塊。

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E4%BB%80%E9%BA%BC%E6%98%AFHTML%E3%80%81CSS%2F4.png?alt=media&token=de9d7ecf-69cb-45a5-81f7-67c3fbc3d082)

### 如何運用HTML在網站中放入一個標題

接下來我們先談談要如何在HTML當中為我們的網站放入一個標題。

首先，在HTML中想要蓋出一個網頁，你需要各種元素，包含了標題的元素、段落的元素、連結的元素、圖片的元素等等，而這些元素是以**標籤**的形式表達的。

以標題元素 H1為例，H1是網站中最主要的標題，通常用於標示網站的名稱或該文章的主旨，它的標籤長這樣子的：
```html
<h1>即溶啟思</h1>
```

從這裡我們可以看到，標籤的開頭是```<h1>```，結尾則是```</h1>```，結尾比開頭多了一個斜線”/”，意味著結束，而中間則可以書寫文字內容。

那麼接下來就請你將這段話寫到CodePen中吧！

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E4%BB%80%E9%BA%BC%E6%98%AFHTML%E3%80%81CSS%2F5.png?alt=media&token=dada3dba-d5cf-49d9-ae4f-fe20fb0c56c9)

如果你有順利完成的話，就會看到右手邊的白色框框中呈現出我們目前所撰寫的網站內容囉。

### 如何透過CSS修改標題樣式

那麼我們剛剛透過HTML將我們的網站門牌H1標題放上去囉，接下來你可能會想知道要怎麼透過CSS來修改H1標題的樣式。

在CSS中首先要使用**選擇器**，將要編輯的HTML標籤給選擇起來，請參考下方程式碼。

```html
h1{ 
  font-size:40px;
  color:white;
  background:black;
}
```

從這個程式碼中我們可以看到要編輯的是”h1″標籤，後面用{ }大括號將我們對於H1標籤設定的內容框起來，這樣瀏覽器就知道我們希望如何來呈現H1標籤囉，換你試試看吧。

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E4%BB%80%E9%BA%BC%E6%98%AFHTML%E3%80%81CSS%2F6.png?alt=media&token=37e18951-5aa6-4366-8fe6-11283bc50c1d)

如果你有嘗試成功，就會看到標題產生變化囉。

最後補充一下，CSS中有許多屬性，屬性還跟隨著不同的值(Value)來產生不同的變化，而屬性的後方需要加上冒號” : “，並且在書寫完設定的值之後，還要再加上一個分號” ; “，瀏覽器才會知道該如何區分不同的屬性喔。

我們在這邊做的設定意思如下：

1. font-size:40px; 是設定文字的尺寸為40px
2. color:white; 是設定文字的顏色為白色
3. background:black; 是設定背景為黑色

## 結語

那麼這就是我們今天的分享，談到了HTML和CSS在網站中的功能，也介紹了CodePen這個工具，讓大家可以自行體驗看看HTML和CSS的差異及交互作用，下一次再來詳細介紹兩者的撰寫方式吧！

感謝你閱讀我的學習筆記，我會繼續努力練習，我們下次見。

最後也感謝[六角學院](https://www.hexschool.com/)認真教學的老師和助教，幫助我學習！有興趣學習網站前端工程的同學們，可以關注一下唷。