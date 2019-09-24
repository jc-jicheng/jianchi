## HTML
### doctype
​    定义：doctype标签是一种标准通用语言的文档类型声明，它的目的是告诉浏览器应该用什么样的文档类型来定义(DTD)来解析HTML文档
​    作用：声明文档的解释类型(document.compatMode),避免浏览器的怪异模式
​    BackCompat:怪异模式，又称混杂模式，是指浏览器按照自己的方式来解析代码，使用一种较为宽松的向后兼容的方式来显示页面
​    Css1Compat:标准模式，又称严格模式，是指浏览器按照W3C标准来解析代码显示页面

### title
​     定义网页的标题
​     SEO检索网页时，首先检索的就是title，
​     搜索引擎检索：title>h1-h3>strong>em>img&alt>a
### meta
​    meta是HTML文档在head标签里定义的一个对文档进行描述的功能性标签
​    meta标签的作用：
​        1.搜索引擎优化（SEO）
​        2.定义页面使用语言
​        3,。自动刷新并指向新的页面
​        4.实现网页转换时的动态效果
​        5.控制页面缓冲
​        6.页面定级评价
​        7.控制网页显示的窗口

### 块级标签：
​    属性：
​        独占一行，换行显示
​        可以设置宽高，(设置宽高一首，后边仍然不会出现任何元素)
​        块级标签可以嵌套块级标签（p标签、h标签除外）
​        块级标签可以嵌套行级标签
​    p
​    h
​    div
​    ul>li
​    ol>li
​    dl--dt--dd:dl标签的子元素只能是dt和dd
​    form
​    br
​    hr
​    

### 行级标签
    属性：
        行内显示
        不能设置宽高，内容撑开宽高
        行标签只能嵌套行标签（a标签不能嵌套a标签）
        支持左右margin，不支持上下margin
    span
    a
    strong
    var 
    em
    b--i--u
    img(行内块标签)
    input

 ### a标签  
   href:书写a标签的跳转路径，当不知道a标签的跳转路径时，可以写###或:"javascript:;"
   title:鼠标悬浮，提示给用户的信息
   target:设置页面打开的方式，默认是_self：在当前页面中打开，_blank：在新标签页打开
   a标签的锚链接：直接将href的值赋值为要跳转的位置的，id名

 ### img标签
​    行内块标签
​    src：是用来引入路径的
​    img是自身拥有宽高属性的，可以设置宽高
​    alt:
​        1.当图片因为网速或者路径等原因出错加载不出来时，对用户的提示
​        2.SEO在爬网页时，是通过alt属性来得知这个图片的信息的
​    title：
​        鼠标悬浮，提示

### form标签
​    包含表单元素，配合提交按钮进行数据的提交
​    action:你要提交的位置
​    method:数据传输的方法，post:传输量大，安全 get：传输量小，内容在地址栏显示
​    
### input标签
​    属性：
​        type:控制input的样式，默认为text--单文本输入框
​        name:表单元素的名称
​        value:表单的值，也可以是表单中的内容
​    当我们提交的时候，是以name=value的形式发送给服务器的
​    类型
​        text:单行文本输入框
​        password:密码框
​        radio:单选框
​        checkbox:多选框，多选框的每一个name值要一样
​        file:上传文件
​        hidden：隐藏域，此表单不会展示给用户，里边的name和value我们已经书写好了，直接会随着点击提交按钮的时候提交
​        button:单纯的按钮元素，什么都不执行
​        reset:重置按钮
​        submit:提交按钮
#### select--option:
   下拉列表
   name属性是书写在select上的，values属性是书写在option上的
#### textarea   
   多行文本输入框
   name值必须书写
#### label
​    作用：当点击和表单相关联的文字时，也能让表单获取焦点
​    用法：
​        1.让label包含住相关联的文字，并且label标签上的for属性的值和input的id值相等
​        2.label不允许书写for属性，直接使用label将关联文字和表单元素都包含住

### table标签
    表格：分为标题（caption）和表格内容
    每一行都是一个tr标签，
    在每一行中再分列，每一列都是一个td标签

   

## CSS
​    选择器的优先级：
​        !important>行内书写>id>class>标签名


 ### 知道宽高的元素在不知道宽高的父级中 水平垂直居中   
    1. {
        position:absolute;
       top:0;
       bottom:0;
       left:0;
       right:0
       margin:auto;
    }  
    2.
    {
        width:100px;
        height:100px;
        position:absolute;
        top:50%;
        left:50%;
        margin-top:-50px;
        margin-left:-50px;
    }

 ### 设置图片水平垂直居中 
```javascript
    {
        div{
            height:100px;
            line-height:100px;
            text-align:center;
        }
        img{
            vertical-align:middle;
        }
    } 
```


   ### 使用css书写三角形
   ```javascript
   {
            width：0；
            height:0;
            transparent是透明的意思
            border-top:100px solid transparent;
            border-left:100px solid transparent;
            border-right:100px solid transparent;
            border-bottom:100px solid skyblue;
        }
   ```

   ###  文本样式设置
   text-decoration
        下划线：text-decoration:underline yellow;
        上划线：text-decoration:overline ;
        删除线：text-decoration:line-through;
    去掉超链接的下划线：
        text-decoration:none;
   text-indent
        首行缩进：text-indent:2em;
        em：是相对于字体大小的，1em等于一个字体大小
   text-align:可被继承
        left
        right
        center
   字符间距
        letter-spacing:字符与字符的距离
        word-spacing:单词与单词的距离
             

 ###  背景设置

​    背景颜色：background-color:
​    背景图：
​        1.使用img引入
​        2.使用background-image,通过url方法引入
​            background-image:url("路径") 0 0 no-repeat;
​            如果不写no-repeat,浏览器默认沿着x轴y轴平铺       

### 盒模型
​    盒模型概念：元素的盒模型指CSS布局中HMTML中的每个元素在浏览器中的解析都可以看作一个盒子，拥有盒子一样的外形和空间
​    盒子模型属性：
​        内容--------height,width
​        padding（内边距）
​        边框（border）------border:1px solid red;
​        margin（外边距)   

    怪异盒模型：
        设置的宽度等于内容+内边距+边框
        所占空间大小计算=内容+外边距
    标准盒模型
        设置的宽度等于内容
        所占空间大小计算=内容+内边距+边框+外边距
    内边距(padding):可以显示背景颜色，可以显示背景图片，4个值：上下左右四个方向
         padding主要用来撑开内容和边框的距离，实际运用中还基本用来撑开父子之间的距离
    边框：border-width     border-color     border-style
    外边距（margin）：不能显示背景颜色，不能显示当前元素任何内容，撑开兄弟之间的距离
         两个元素的margin上和下回出现叠加现象（多个标签有默认的上下margin样式，为了防止多行之间默认的margin叠加，造成空隙过大，所以设计了垂直方向叠加的状态）
         如果一个元素是父级的第一个元素或者最后一个元素，那么他们的上外边距或下外边距会进行塌陷，把自己的margin变成父级的margin（依然是为了防止空隙过大，当变成父级的margin之后，就可以和上一个元素上下叠加了）
         margin还能够进行居中操作，给定宽度以后，设置margin的左右为auto，那么元素就会在父级中水平居中，因为高度不定，所以我们基本没有垂直方向的auto居中
         margin的负值：
                左负：向左移动，原来位置不保留
                右负：不移动，元素的显示的宽不改变，但是占用的空间变小
                上负：向上移动，原来的位置不保留
                下负：不移动，元素显示的高不改变，但是占用的空间变小
     
    盒模型：内容、内边距额边框，这些是3个盒子
            其中内容盒子叫做:content-box
            内边距盒子叫做：padding-box
            边框盒子叫做：border-box


​    

### 浮动
​    float:left/right; 
​    设置浮动的元素和脱离文档流，浮动的元素，并不属于文档中的普通流，元素会漂浮于文档流之上
​    由于浮动的这一特性，导致本属于普通流的元素设置浮动后，如果父级不存在其他普通流，父级的高度就会为0，如果父级存在其他普通流，父级的高度也会受到影响
​    浮动只能在当前父元素中浮动，并且浮动元素不能操作上边的兄弟元素  
​    浮动对行标签和块标签的影响
​        对块标签的影响：行内显示，可以设置宽高
​        对行标签的影响：行内显示，可以设置宽高，可以设置上下margin
​    清浮动：
​        1.在父级中书写：overflow:hidden;
​        2.在浮动元素的下边书写一个块级空标签，然后给这个标签一个属性叫做clear:both;
​        3.伪类清浮动
​            .outer:after{
​                   content:"\200B";
​                   display:block;
​                   height:0;
​                   clear:both;
​            }
​       
### position定位
​    position属性：
​        static：静态的
​        relative:相对的，元素相对自身原始位置偏移某个距离，元素仍保持其为定位前的形状，不会脱离文档流，它原本所占的空间仍保留
​        absolute:绝对的，是控制元素相对于最近的定位父级的元素进行定位的（最近定位父级，必须拥有定位属性，并且值不能是static），绝对定位的元素脱离文档流，原来的位置不再保留，但是定位的元素不会挤到其他元素，
​        fixed:  固定的，相对于浏览器窗口定位，和其他元素没有任何关系
​    left和right一起书写时，只有left起作用，top和bottom一起书写时，只有top起作用
​    定位对行标签和块标签的影响
​        块标签：可以设置宽高，完美支持margin和padding
​        行标签：在没有设置宽的时候，宽度自适应

### css reset   
​    HTML标签在浏览器中都有默认的样式，不同的浏览器的默认样式之间存在差别，可能会造成布局上的混乱，css reset的作用就是重置这些默认样式，使样式表现一直

### 透明度设置   
    1.使用opacity设置
        opacity：0.5;
        opacity在IE8及以前的浏览器是不支持的，需要使用filter来设置
        filter:Alpha(opacity=50);
    2.使用rgba方法来设置
        background-color:rgba(0,0,0,0.6);
    3.直接测量纯色背景图的颜色,让后让其一背景图平铺
        background:url(../../) 0 0 repeat;

### display
​    display属性
​        none：是控制元素隐藏，并且不占用任何空间（如果要让元素显示，那么对元素设置display：block）
​        block：让元素以块属性标签显示，就是拥有快标签的属性，但是嵌套规则还是按原本的标签属性来
​        inline-block:让元素以行内块属性显示，既可以设置宽高，又能行内显示
​        inline:此元素将显示为内联元素，此元素前后没有换行符
​       
### overflow
​    overflow:visible:默认值，内容不会别修剪，会呈现在元素框之外
​    overflow：hidden：让自身超出的内容隐藏掉，我们目前是不能看到超出的内容的
​    overflow：scroll：无论元素大小术后超出，都会生成滚动条
​    overflow：auto：超出生成滚动条，不超出就不会生成滚动条   

### 最小-宽度/高度
​    min-height
​    min-width:为元素设置最小宽度后，该元素的宽度在“当前浏览器宽度”与"设置的最小宽度"当中去最大者

### CSS Sprites
​    是一种网页图片应用处理方式
​    将一个页面中涉及到的所有零星图片都包含到一张大图中，在用css精确的定位出背景图片的位置，会从整体上减少了图片的大小，大大减少了客户端向服务器请求的次数，减轻了服务器的压力，同时也利用了缓存机制，使用户觉得浏览速度加快   

###hack
   由于存在着不同的浏览器，同种浏览器有不同的版本，不同的浏览器对CSS的解析机制并不是完全相同的，从而导致不同浏览器之间页面的显示效果各不相同
   针对某种浏览器进行样式设置，从而达到所有浏览器显示的效果一直，这种标识不同浏览器的方法就是hack
   hack三种常见形式：CSS属性hack、CSS选择符hack、IE条件注释hack
   hack主要针对IE
   CSS属性hack
        下划线（_）:_width:400px------IE6
        星号（*） :*width:400px-------IE6,IE7
        加号（+）：+width:400px-------IE6,IE7   
   IE条件注释
        <!--[if 属性 IE版本号]>
        具体HTML代码
        <![endif]-->

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   

   