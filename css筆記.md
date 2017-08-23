## 格線
- 排版
off set push pull hidden
## 導覽
## 表格＆內容
## 表單
- form group
- input group
  - form-control
  - label form
## js 外掛

所有的尺寸的default都是medium


## relative
- 位移參考的是原來位置的四個邊
https://codepen.io/TengLee/pen/PKEQLZ


## abosolute
五個步驟
1. 先從流浮上
2. 找父元素有無定位設定，除了static以外，relative, absolute, fixed都可定位
3. 當父元素有無定位設定會一直定位到window
4. 捲軸往下卷absolute會留在最一開始window的位置
https://codepen.io/TengLee/pen/braRXj


### absolute置中
- 上下左右＝0
- margin = auto
  - 當沒有設margin auto 變成抓不到邊界因此取預設值left=0, top=0移到左上
- 父層不能是static

https://codepen.io/TengLee/pen/braRXj


## 垂直置中
- inline, inline-block用verticle middle
- block用absolute margin auto
https://codepen.io/TengLee/pen/vJppdR


### verticle align
- 沒特別設定的話為baseline
- baseline: 默认。元素放置在父元素的基线上。
- middle: 把此元素放置在父元素的中部。
https://codepen.io/TengLee/pen/vJppdR?editors=1100


### 多個inline-block置中 偽元素
- 子原素皆設verticle-align;
- 偽元素之必要
```
::before {
content: '';
display:inline-block;
height: 100%;
vertical-align: middle;
}
```
https://codepen.io/TengLee/pen/vJppdR


###padding margin的心得
當同一階層 用margin 特別是margin-bottom
當不同階層 用padding 特別是padding-top


## ul li 去除空白文字的方法
ul font-size: 0;
li font-size: 16px;
https://codepen.io/TengLee/pen/XaVEWP


### z-index
z-index要有position


### body 跟 html多高？
- 首先要知道div外層包著body包著html包著window
- window 和 body的高度如果內容物有高度則有多高就有高
- 如果無內容物則為零，在window上方
- 渲染body background會渲染在window
https://codepen.io/TengLee/pen/BdJQWy


### float
- clear的意思是避開浮動
- 父元素設overflow auto之所以可以包著子元素是因為overflow auto會去抓自元素的邊界


### display grid


### css 去除瀏覽器預設
```
html {
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: inherit;
  padding: 0;
  margin: 0;
}
```


###解決img下的多餘空白
- 1、將圖片轉換為塊級對像
- 2、設置圖片的垂直對齊方式
- 3、設置父對象的文字大小為0px
- 4、改變父對象的屬性
- 5、設置圖片的浮動屬性
- 6、取消圖片標籤和其父對象的最後一個結束標籤之間的空格。
http://dancewing.pixnet.net/blog/post/24572377-%E8%A7%A3%E6%B1%BAimg%E4%B8%8B%E7%9A%84%E5%A4%9A%E9%A4%98%E7%A9%BA%E7%99%BD
