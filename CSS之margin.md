# CSS之margin

标签： CSS

---
### 1.特性-改变容器尺寸：

 - 可视尺寸-clientWidth（标准）=border以内尺寸
 - 占据尺寸-outWidth=margin以内尺寸
 
![images01][1]

### 2.百分比单位

 - 普通元素的百分比margin都是相对于容器的宽度计算的； 
 - 绝对定位元素的百分比是相对于第一个定位的祖先元素的宽度计算的。

![image02][2]
 
### 3.垂直方向的margin重叠解决方案

 - 对于父子元素，可在父级增加overflow：hidden
 - 对于其他元素，对应垂直方向增加border、padding、内联元素（如：&nbsp)

### 4.应用
 - 等高布局：用负值margin-bottom占据空间，同时用正值padding-bottom填补缺失的空间。

        .f{
            float: left;
            width: 100px;
            text-align: center;   }   
        .s1{
            background: #444;
            color:#fff;}   
        .s2{
            background:#bbb;
            margin-bottom: -42px;
            padding-bottom: 42px;   }
            
            <div class="f s1">
              123<br>
              123<br>
              123<br>
              123<br>
              123<br>
            </div>
            <div class="f s2">
              456 <br>
              456 <br>
              456 <br>
            </div>
![images03][3]

 - 两端对齐

        div{
          width: 1280px;}
        ul{
          padding: 0;
          margin: 0;
          background:#ccc;
          margin-right: -20px;
          overflow: hidden;
          list-style:none;
        }
        li{
          float: left;
          margin-right: 20px;
          background: #ddd;
          width: 240px;/* 宽度240=（1280-20*4）/5 */
        }
    
    

 - 两栏自适应布局
 ![此处输入图片的描述][4]
    

    
 


  [1]: https://github.com/liva92/CSS/blob/master/images/margin_client.png
  [2]: https://github.com/liva92/CSS/blob/master/images/margin02.png
  [3]: https://github.com/liva92/CSS/blob/master/images/margin03.png
  [4]: https://github.com/liva92/CSS/blob/master/images/margin04.png