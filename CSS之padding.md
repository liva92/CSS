# CSS之padding

标签： CSS

---

### 1.padding对block元素的影响：

 - 一般情况下都会影响元素尺寸大小；
 - 对`width：auto`或者`box-sizing:border-box`的block元素，不影响尺寸。
### 2.padding对inline元素的影响
 - 水平padding影响尺寸；
 - 垂直padding不影响尺寸，但会影响背景色，因为占据了空间。
![images][1]

### 3.ol/ul内置的padding

 - 内置的padding单位为px,若果字号很小，间距就会很开；若果字号很大，序号就会溢出容器之外；
 - 一般网页开发`font-size：12~14px`,此时`padding-left:22~25px`,基本能实现图文左对齐。

### 4.表单内置padding

 - 所有浏览器 `input/textarea/button` 内置padding;
 - 部分浏览器`select` 内置pading,如FireFox/IE8+可以设置padding;
 - 所有浏览器 `radio/chexbox` 无内置padding;
 - `button` 元素的padding最难控制。
 解决方案：用lable标签设置padding
![images][2]

### 5.应用
- 绘图
![padding04][3]
- 使用百分比单位构建固定比例布局
1、空元素
![padding07][4]
2、包含子元素

       .box{
        padding: 50%;
        position: relative;
        }
      .example{
        position: absolute;
        top:0;
        right: 0;
        bottom: 0;
        left: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 60px;
    }
        <div class="box">
            <div class='example'>
                <h1>实现正方形</h1>
            </div>
        </div>

  ![images06][5]


 - 两栏自适应布局
![images][6]







  [1]: https://github.com/liva92/CSS/blob/master/images/padding02.png
  [2]: https://github.com/liva92/CSS/blob/master/images/padding03.png
  [3]: https://github.com/liva92/CSS/blob/master/images/padding04.png
  [4]: https://github.com/liva92/CSS/blob/master/images/padding07.png
  [5]: https://github.com/liva92/CSS/blob/master/images/padding06.png
  [6]: https://github.com/liva92/CSS/blob/master/images/padding05.png
