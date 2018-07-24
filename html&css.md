### 1、css盒模型
每个盒子都有四个属性： content、 padding、 margin、 border
### 2、块级元素、行内块级元素、行内元素、空元素
块级元素：div、ul、 ol、 li、 dl、 dt、 h1、h2、h3、...p   
行内块级元素：img、input、  
行内元素：a、 b、 span、img、input、 strong、 select   
空元素: br、 hr 、meta、link、 img、  
### 3、css 实现垂直水平居中
3-1、使用定位margin调整left&right值实现  
```
    父元素{ position:relative/absolute/fixed }  
    子元素{  
        position: absolute;        //父元素需要相对定位
        top: 50%;
        left: 50%;
        margin-top:-100px ;   //二分之一的height，width
        margin-left: -100px;
    }
```
3-2、使用定位  子 left&right&top&bottom : 0 +  margin:auto;   
```
<style>
    *{
        margin: 0;
        padding: 0;    
    }
    .p{
        /*父元素为除了static以外的定位方式*/
        position: relative;
        /* position: absolute; */
        /*position: fixed;*/
        width: 500px;
        height: 500px;
        border: 1px solid red;
    }
    .c{
        /*子元素为绝对定位*/
        position: absolute;
        width: 200px;
        height: 200px;
        /*top、bottom、left和right 均设置为0*/
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;
        /*margin设置为auto*/
        margin:auto;
        border: 1px solid green;    
    }
</style>
<div class="p">
    <div class="c">
        子元素
    </div>
</div>
```
3-3、父 table-cell + vertical-align: middle + 子 margin: 0 auto;   
```
<style type="text/css">
    *{
        margin: 0;
        padding: 0;    
    }
    .p{
        width: 500px;
        height: 500px;
        border: 1px solid red;
        display: table-cell;
        /*实现垂直居中*/
        vertical-align: middle;
    }
    .c{
        width: 200px;
        height: 200px;
        border: 1px solid green;
        /*margin: 0 auto; 实现水平居中*/
        margin: 0 auto;    
    }
</style>
<div class="p">
    <div class="c">
        子元素
    </div>
</div>
```
3-4、flex布局  
```
<style type="text/css">
    * {
        margin: 0;
        padding: 0;
    }
    
    .p {
        width: 500px;
        height: 500px;
        border: 1px solid red;
        /*flex 布局*/
        display: -webkit-flex; /*webkit内核，Safari */
        display: flex;
        /*实现垂直居中*/
        align-items: center;
        /*实现水平居中*/
        justify-content: center;
    }
    
    .c {
        width: 200px;
        height: 200px;
        border: 1px solid green;
    } 
</style>
<div class="p">
    <div class="c">
        子元素
    </div>
</div>
```
### 4、


