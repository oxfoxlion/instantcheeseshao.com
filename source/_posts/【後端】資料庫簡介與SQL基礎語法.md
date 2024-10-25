---
title: 【後端】資料庫簡介與SQL基礎語法
date: 2024-10-25 15:20:03
tags:
 - SQL
 - 六角學院
 - 網頁開發
categories:
 - 網頁開發
 - 學習筆記
cover:
 https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E5%BE%8C%E7%AB%AF%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9.png?alt=media&token=988c9905-ba8e-46ba-8d5b-797c03390126
---
這兩天報名了六角學院的後端工程師體驗營，今天馬上把預習影片看完，來寫筆記了!!

## 什麼是資料庫

日常生活中我們會使用到非常多的資料庫，比方說去超市買菜，每個商品條碼的背後都是一個資料庫，紀錄了商品的價格、庫存、折扣是多少等資料，其實它就像是一個Excel表，以統一的格式進行紀錄，並且透過系統(伺服器)去管理這些資料。

![欄與列](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E5%B1%AC%E6%80%A7%E8%88%87%E8%B3%87%E6%96%99.png?alt=media&token=7fc936e6-ee01-4700-9f19-398d4d5437f2)

就拿我之前賣餅乾時候計算包裝的試算表來說明吧，這裡每一橫列(row)都是一筆資料(紅色框框)，每一直欄(column)都是一個屬性(綠色框框)，記載這筆資料的某個訊息。

其實就跟Notion的Database是一樣，每一筆資料都可以設定多個不同的屬性，並且透過表格的方式可以看得出差異、能夠做比較。
![notion資料庫](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2FNotion.png?alt=media&token=b0836539-0ac1-4221-9f6d-714609587e76)

如果單獨把Notion的其中一筆資料拉出來看，就會長這樣，這樣應該就很容易感受得出來屬性與資料的差異在哪裡了。不同於課表這類一般的表格，資料庫的資料是一筆一筆向下新增，每筆資料都會共用一樣的這些屬性，而屬性可以有多個。

![一筆資料](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E4%B8%80%E7%AD%86%E8%B3%87%E6%96%99.png?alt=media&token=f14ad2b7-2511-4243-acd5-5b7edf6d9298)

## 什麼是SQL

SQL(Structured Query Language) 中文稱作結構化查詢語言，是用來管理資料庫的程式語言

## 資料表建立與寫入

### 如何建立資料表

建立資料表可以使用CREATE TABLE語法加上自訂義資料表名稱，接著用括號將欄位(columns)制定出來

```SQL
-- 建立 資料表 自訂名稱(屬性 資料型別Type,屬性 資料型別Type);
CREATE TABLE products(
  品項 VARCHAR(20), --屬性名稱 僅限文字(上限20字), 以逗號隔開，再輸入下一個欄位設定 
  品牌 VARCHAR(20),
  單價 INTEGER, -- integer是整數的意思
  數量 INTEGER
); --以分號表示這段程式碼結束了
```

### 如何寫入資料

建立好資料表之後，我們就可以開始來新增一筆一筆的資料，使用INSERT INTO 加上自訂資料表的名稱來進行寫入，請看下方程式碼

```SQL
-- 選擇要寫入的資料表(選擇要寫入的屬性欄位)，注意順序
INSERT INTO products (品項,品牌,單價,數量)
VALUES 
('7*10cm封口袋','蝦皮',35,100), --VALUE後面就可以加入資料，記得還沒結束的話要使用逗號隔開
('9*11.5cm封口袋','蝦皮',40,100),
('10*13cm封口袋','蝦皮',50,100); --已經結束了的話用分號隔開
```

## 如何查找資料

建立好資料之後當然要先確認一下資料有沒有正確被記錄，所以我們使用SELECT語法來查看

```SQL
-- 選擇 萬用字元在這邊表示所有的屬性 然後透過FROM指定要查詢的資料表
SELECT * FROM products;
```

![查詢結果](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E7%B5%90%E6%9E%9C1.png?alt=media&token=5e8c0321-6277-4e62-9ae3-9299c3cc1dbd)

```SQL
--如果只要查詢部分的資料，可以把萬用字元替換成屬性名稱
SELECT 品項,單價 FROM products;
```

![查詢結果](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E7%B5%90%E6%9E%9C2.png?alt=media&token=d7b5ce6e-9e5e-461f-8bdb-2ac42774efd8)

### 如何設定屬性的別稱
一樣使用SELECT，先選擇我們要的爛位，並透過AS制定別稱，最後再指向我們要修改的資料表。

```SQL
SELECT 
  品項 AS name, --一樣記得這邊要加入逗號
  單價 AS price
FROM products;
```

![透過AS制定別稱](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E7%B5%90%E6%9E%9C3.png?alt=media&token=b28b42d6-4dfb-40ef-899d-88ea2d825ead)

AS 語法也可以用來進行運算

```SQL
SELECT 
  品項 ,
  1000 / 單價 AS 最低出貨量
FROM products;
```

![AS 語法也可以用來進行運算](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E7%B5%90%E6%9E%9C4.png?alt=media&token=218b56b4-4f65-4cc8-8ebe-e623c0235d3d)

但是這邊制定的別稱以及運算結果，只會用在該次搜尋上，並不會把運用AS計算之後的結果記錄回資料表。

### 如何篩選資料

使用WHERE語法可以進行資料的篩選

```SQL
SELECT * FROM products -- 一樣要先指定資料表
WHERE 品項 = '7*10cm封口袋'; --WHERE後面接要查詢的屬性以及該屬性的值
```

![WHERE語法可以進行資料的篩選](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E7%B5%90%E6%9E%9C5.png?alt=media&token=420919a5-3aa6-46e8-96aa-308cb6bd05ed)

### 使用比較運算子篩選資料

一樣是使用剛剛搜尋資料的SELECT和WHERE語法，再加上一些條件就可以更精確地來搜尋我們要的資料
比方說透過比較運算子，我們可以查出單價小於40元的包裝

```SQL
SELECT * FROM products -- 一樣要先指定資料表
WHERE 單價 < 40; 
```
### 使用邏輯運算子篩選多個條件

如果有很多個條件要同時符合的話，可以使用邏輯運算子

```SQL
SELECT * FROM products -- 一樣要先指定資料表
WHERE 單價 < 40 
AND 品牌 = '蝦皮'; 
```

如果2個條件只要滿足其1，可以使用OR

```SQL
SELECT * FROM products -- 一樣要先指定資料表
WHERE 單價 < 40 
OR 品牌 = '蝦皮'; 
```

### 集合與範圍運算子

#### BETWEEN

可以查找介於兩個範圍之間的紀錄

```SQL
SELECT * FROM products -- 一樣要先指定資料表
WHERE 單價 BETWEEN 30 AND 50;  
```

#### IN()

可以查找所有符合的項目

```SQL
SELECT * FROM products -- 一樣要先指定資料表
WHERE 品牌 IN ('蝦皮','幸福家');  
```

#### NOT IN()

可以排除所有符合的項目

```SQL
SELECT * FROM products -- 一樣要先指定資料表
WHERE 品牌 NOT IN ('蝦皮','幸福家');  
```

## 如何更新資料

使用UPDATE 可以進行資料的更新

```SQL
UPDATE products --這邊不需要加上FROM
SET 品牌 = '幸福家',
    數量 = 250
WHERE 品項 = '7*10cm封口袋';
```

![更新結果](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E7%B5%90%E6%9E%9C6.png?alt=media&token=6c39638f-7b51-4faa-9351-a95d3c228d2d)

看到下方的結果就知道更新囉，但還是可以再執行一次SELECT確認一下
![執行一次SELECT確認更新結果](https://firebasestorage.googleapis.com/v0/b/instantcheeses.appspot.com/o/%E8%B3%87%E6%96%99%E5%BA%AB%E4%BB%8B%E7%B4%B9%2F%E7%B5%90%E6%9E%9C7.png?alt=media&token=db39dfad-d3f2-4108-b875-d968c413f062)

## 如何刪除資料

使用DELETE 可以進行資料刪除

### 單筆資料刪除法

```SQL
DELETE FROM products --這邊就加上FROM囉
WHERE 品項 = '10*13cm封口袋';
```

### 條件刪除法

搭配條件式可以進行多筆資料的刪除

```SQL
DELETE FROM products 
WHERE price BETWEEN 30 AND 50; --指定刪除價格範圍在30到50區間的品項
```

### 多個條件刪除法

刪除多個條件的方法也跟查詢多個條件的方法是一樣的
```SQL
SELECT * FROM products -- 一樣要先指定資料表
WHERE 單價 < 40 
AND 品牌 = '蝦皮'; 
```

那麼今天的筆記就到這邊，就這樣看影片、寫筆記竟然也用掉了一天的時間，太可怕了，我要繼續去完成其他的作業，下次見囉。