### 1、css盒模型
每个盒子都有四个属性： content、 padding、 margin、 border
### 2、块级元素、行内块级元素、行内元素、空元素
块级元素：div、ul、 ol、 li、 dl、 dt、 h1、h2、h3、...p   
行内块级元素：img、input、  
行内元素：a、 b、 span、img、input、 strong、 select   
空元素: br、 hr 、meta、link、 img、  
### 3、css 实现垂直水平居中
3-1、使用relative定位  
```
    父元素{ position:relative; }  
    子元素{  
        position: absolute;        //父元素需要相对定位
        top: 50%;
        left: 50%;
        margin-top:-100px ;   //二分之一的height，width
        margin-left: -100px;
    }
```
3-2、