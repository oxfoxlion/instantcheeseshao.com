---
title: 【前端新手筆記】2-HTML常用標籤
date: 2024-06-14 23:06:23
tags:
 - HTML
 - 六角學院
 - 網頁開發
categories:
 - 網頁開發
 - 學習筆記
cover: https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F%E8%B5%B7%E6%80%9D%E6%96%87%E7%AB%A0_%E5%B7%A5%E4%BD%9C%E5%8D%80%E5%9F%9F-1-2.jpg?alt=media&token=87ed38ac-8343-48a4-9b4b-4eedea8e0bc3
---

上一篇文章中，我們有提到HTML標籤以及它的表達方式，這篇文章主要想要紀錄我常用HTML標籤。

## 網站標題

**標題有h1-h6**，其中最重要的是h1，一個網站只會有一個h1標題，通常就是該網站或文章的主旨。

```html
<h1>標題</h1>
```

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F2.png?alt=media&token=3c2d3bbe-70e4-40c3-921b-934a2a3368e2)


## 文字內容

文章的內容可以使用**p標籤**來呈現，每一個p標籤就是一個段落。

```html
<p>歡迎來到即溶啟思！我是站長 邵Shao，我喜歡閱讀、喜歡學習，而這是我練習輸出所學的一個平台。</p>
<p>我在這裡試著用最簡單的方式，分享啟發思考的知識，而我今天要跟大家分享什麼是HTML，和CSS有什麼差別？</p>
```
![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F3.png?alt=media&token=029622fc-b5b3-4d3b-9b68-84aeab025d9f)

### 斷行標籤

如果希望文字屬於同一個段落，但又希望在下一行顯示，可以使用 ```<br>```標籤

```html
<p>歡迎來到即溶啟思！我是站長 邵Shao，我喜歡閱讀、喜歡學習，而這是我練習輸出所學的一個平台。
    <br>我在這裡試著用最簡單的方式，分享啟發思考的知識，而我今天要跟大家分享什麼是HTML，和CSS有什麼差別？</p>
```

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F4.png?alt=media&token=b06e2444-07e9-4df9-bb58-bd49ce4e2e47)

## 嵌入連結

想要在網站中嵌入連結的話，就必須使用a標籤。

```html
<a href="http://instantcheeseshaocom.local/" title="即溶啟思" target="_blank">即溶啟思</a>
```
![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F5.png?alt=media&token=f3d60e57-4f3f-4697-9f2c-27842edfc1e6)

a標籤可以嵌入在其他標籤內

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F6.png?alt=media&token=1896c573-1dc3-47ea-9859-79a8bf45165d)

a標籤也可以被獨立撰寫

### a標籤屬性設定

屬性就是寫在標籤內，用於記錄這個標籤的資訊，以這種方式做表達：

```屬性="設定值"```

每種屬性都有必須填入的對應值。

#### 1. href屬性

用於填寫連結網址
```href="http://instantcheeseshaocom.local/"```

#### 2. title屬性

標明這個連結的名稱，當滑鼠移動到連結上方會顯示出來
```title="即溶啟思"```

#### 3. target屬性

設定使用者將如何開啟這個連結，比較常用是這兩個：

``` target="_blank" ```

* _self：直接在當前視窗中打開，如果沒有設定target屬性，就會以這個為預設，這麼一來原本在瀏覽的網站就會被轉到連結上。
* _blank：在新視窗中開啟。

完整的寫法就請參考上方的a標籤囉。

## 嵌入圖片

圖片可以用img標籤嵌入。

```html
<img src="http://instantcheeseshaocom.local/wp-content/uploads/2024/04/cropped-%E5%8D%B3%E6%BA%B6%E8%B5%B7%E6%80%9D%E9%A0%BB%E9%81%930226_%E5%B7%A5%E4%BD%9C%E5%8D%80%E5%9F%9F-1-scaled-1.jpg" alt="即溶啟思" title="即溶啟思">
```
![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F7.png?alt=media&token=c9d043b7-1ca5-4941-b682-d517a7c89812)

img標籤只能設定屬性，也不需要結束標籤

### img標籤屬性

#### 1. src屬性

在這裡填入圖片連結，可以是圖片網址，或者是描述該HTML檔案的相對位置。

#### 2. alt屬性

這是圖片的描述，當圖片失效顯示不出來的時候，就會以圖片描述的方式出現。
![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F8.png?alt=media&token=cbbad195-f5c2-45bd-8b41-ad9090d942fb)

#### 3. title屬性

一樣可以加入title屬性，讓使用者滑鼠移到圖片上方時顯示相對應的名稱。

## 製作列表

在HTML中，我常用兩種列表：無序列表與有序列表。

### 無序列表

無序列表用```<ul>```標籤來表示，當中的每一點則用```<li>```標籤表示。

```html
<ul>
  <li>無序列表</li>
  <li>就是沒有順序</li>
  <li>這樣子</li>
</ul>
```

![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F9.png?alt=media&token=7d043ec7-a88f-4ab5-8a16-fa7265a3e76c)

### 有序列表

有序列表用```<ol>```標籤來表示，內容每一點一樣用```<li>```標籤表示。

```html
<ol>
  <li>第一點</li>
  <li>第二點</li>
  <li>第三點</li>
</ol>
```
![](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/html%E6%A8%99%E7%B1%A4%2F10.png?alt=media&token=e9590f3f-284e-4fdb-8787-50b21dcb0747)

以上就是簡單的常用標籤分享，之後希望可以分享標籤的組合技，以及排版用的標籤，那就先這樣子囉!!希望你們會喜歡我的分享。