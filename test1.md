大喵教育前端培训
================

## 阶段性测试 2019.12.06

### 大喵教育版权所有，请勿泄漏



01. 列出至少 7 个常用 Linux 命令及其基本使用方法

git add
git commit -m""
git push
git status
git log
git diff
git checkout


ls
cd 路径
touch 文件
echo 内容
cp src dest 从原路径拷贝到另一个路径
mv src dest
cat file1 file2 file3
目的是输出文件的内容按照指定的顺序 > somefile
split -b 20m a.mp4
把文件拆分成20m大小的文件们: aa ab ac ad ae ba... 也有参数取数字
pwd 打印出当前工作目录
vi file 启动并编辑文件
esc 退出编辑模式进入正常模式
i(nsert) 进入编辑模式
:w(rite) 保存
:q(uit) 退出
:wq 保存并退出

nano
没有编辑和退出模式，光标可移动



02. 什么是 html 实体？常见 html 实体有哪些？
 以&开头以;结尾的字符串，用来表示显示在视窗里，不属于代码的符号。常见的有 &nbsp; &amp; &gt; &lt; &copy; &quot; &apos; &trade;

转义字符
有些特殊字符在html中不能明文出现，需要通过特殊的形式表达
这种特殊的形式
&name;
&十进制;
&#十六进制;

03. 计算机为什么使用二进制？

二进制足够简单，而且有布尔逻辑的理论支撑，很方便映射到真/假，方便计算和排除数据误差。
由八个二进制位构成的一个字节也有256个字符，足够储存信息。

04. 什么是 Unicode？如何表示，有什么作用？最通用的 Unicode 实现是？

Unicode 是一套让全世界所有国家所有字符在同一编码环境编号的字符标准，方便“跨语言，跨平台”（百度百科）的文字处理。由十六进制编码表示。

“Unicode编码的实现方式称为Unicode转换格式（Unicode Transfomation Format，UTF）。Unicode编码的实现方式主要由UTF-8,UTF-16,UFT-32等，分别以字节（BYTE）、字（OWORD，2个字节）、双子（DWORD，4个字节，实际只用了31位，最高位为0）作为编码单位。”
————————————————
版权声明：本文为CSDN博主「cakincqm」的原创文章，遵循 CC 4.0 BY-SA 版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/chengqiuming/article/details/88761846


Unicode 是一个将全球字符统一编码的标准，该标准为每个符号指定了唯一且不重复的编号 （e.g.5 和 五)
U+6211(16进制)
最通用的实现是UTF-8及UTF-16，变长编码，把字符占了几个字节的事情表达出来

ascii码
所有英文字符都在127以内
如果每个字符用定长字节来保存，对简单的字符有点浪费 -->每个字符不定长度，变长编码
具体的编解码形式称为某种实现

05. 什么是 GUI，什么是 CLI，什么是接口/界面？现实生活中有哪些例子？
* GUI - Graphics User Interface，图形化**用户**界面/接口
* CLI - Command Line Interface，命令行界面
接口/界面是人与计算机进行信息交换的媒介。比如在桌面上创建一个文件夹。

06. 在什么情况下 html 标签可以不需要闭合？

非自闭合标签也可以不用闭合，因为在一些情况下自动闭合
自闭合标签

07. 在一些情况下某些非自闭合标签的结束标签可以省略的原因是什么？

这种场景一般是可以【推断出】此标签肯定已经结束了，比如父元素里面没有其它标签，或者p里面不可能再套一个p

ul
li
li
/ul

中间两个li不需要闭合，因为li里面不能套li
ul闭合了li一定会闭合

08. 什么是费茨定律？它有哪些应用？
* 执行某项操作所需的时间跟
        * 鼠标与目标的距离成反比
        * 跟目标大小成正比
比如软件界面图标大小和位置的设计

在交互设计者，目标的可达程度与。。。反比，正比
网站把字和按钮设计得很大
快捷键
stroke it，鼠标手势
命令行
运行窗口:菜单在最上面

双击选中一个单词
双击选中一个段落

09. 为什么英文很重要？
因为大部分最尖端和编得最好的技术资料，最丰富的交流平台都是英语的。


10. 将二进制 `10010` 数转换为十进制数
18

11. 将十六进制数 `ABCDEF` 转换为十进制数
11259375

12. 将十进制数 `435` 分别转换成二进制数和十六进制数
110110011
1b3

转8进制

13. 列出 HTML 中常见的全局属性
  name
  id
  class
  title
  alt
  tabindex
  style
  data-*
  可以用在任何一个元素上就叫它全局属性
  lang
  dir
  contenteditable
  contextmenu


14. 什么是操作系统的路径（Path）？它的作用及应用场景是？
它是一个列表，每一项是一个【文件夹的完整/绝对路径】
可以用来设置访问文件的快捷方式

操作系统中的一个有序文件夹列表
environment variable
eva
当用户在命令行或windows的运行窗口输入命令是，会按序在路径列表中查找相应的可执行程序来执行

借由运行窗口加快我们打开软件的速度

15. 什么是文本文件？什么是二进制文件？它们最明显的区别是？

文本文件是用ASCII/Unicode编写的文件，除了txt 有 ini/cfg/html/css/js/.gitignore 等
"Binary" files are any files where the format isn't made up of readable characters.
  文本文件可以直接用键盘编辑，这是二进制文件无法完成的

实际上二者的并无本质区别，都是硬盘上的文件
当一个文件十一文本编码的方式编码了几乎可以用键盘输入的字符时，我们会称其为文本文件，其它都是二进制

基于字符编码
基于值编码


16. 为什么说 html 与数学公式有诸多相似之处？
二者都用符号表达一些抽象概念

因为它们都是树状结构
括号/标签的嵌套规则是相同的


17. 几种常见图片格式有什么区别和特点？
jpg:
有损压缩
每8*8的像素点为单位对图像进行转换，在64范围内的点做了平滑处理，适合均匀颜色渐变的现实社会的照片，不适合清晰和锐利的
一个像素点：3byte，3个字节，每个字节代表RGB中的一种颜色从0到255的256种程度的浓度

png:
portable network graphic
无损压缩，在视频里只保存每帧之间有差异的部分
适合存储大片完全相同颜色的图片，典型的就是软件的截图，不适合用来保存照片，支持透明色（Alpha通道）
每个点实际上由4个字节组成 Red Green Blue Alpha


支持最高256级透明


gif:
颜色只有256种，用一个字节储存像素点，原始图片颜色数量不足256时无损压缩
gif图片一般长宽都比较小，意味着它里的颜色数量比较小
并没有存储每张图的所有点，而只存储了变化了的那些点 （第一帧肯定存储完整的）
支持透明，但支持两种透明，要么某个点完全透明，要么完全不透明



psd:* Photoshop
    * 保存了Photoshop在构造这张图片的过程中的所有信息
      * 图层
      * 名字
      * 选区
    * 浏览器是不认识这种格式的

 webp:
 * Google发明
    * 有损压缩
    * 各方面都胜过jpg
    * 适合在移动端使用
* 支持alpha通道
很多网站使用这个格式

与jpg相比质量相同体积更小
体积相同质量更高
支持透明


bmp
不压缩，体积大，取决于图片尺寸

18. `data-*` 属性一般是用来干嘛？
一类自定义数据属性，它赋予我们在所有 HTML 元素上嵌入自定义数据属性的能力，并可以通过脚本(一般指JavaScript) 与 HTML 之间进行专有数据的交换。所有这些自定义数据属性都可以通过所属元素的 HTMLElement 接口来访问。 HTMLElement.dataset 属性可以访问它们。(MDN)

不会因为标准的改变而产生额外的语义


19. 用什么方法扩大一个 checkbox 的可点击区域？
和label/button等其它元素关联起来，加入图片和文字

不能使用伪元素

20. 什么是 MIME Type？、
A media type (also known as a Multipurpose Internet Mail Extensions or MIME type) is a standard that indicates the nature and format of a document, file, or assortment of bytes.

媒体类型，即比文件扩展名更精确明确的文件类型描述

text/html
text/css
application/javascript
text/plain

21. 哪些标签可以使用 target 属性？哪些标签可以使用 href 属性？
target：<a>

base
a
form
area 图片上不同的区域变成链接

href：<a>, <animate>, <animateMotion>, <animateTransform>, <discard>, <feImage>, <image>, <linearGradient>, <mpath>, <pattern>, <radialGradient>, <script>, <set>, <textPath>, and <use>
base
link
meta

22. 什么是 BOM 头？
Unicode的学名是"Universal Multiple-Octet Coded Character Set"，简称为UCS。UCS可以看作是"Unicode Character Set"的缩写。在UCS 编码中有一个叫做 "Zero Width No-Break Space"，中文译名作“零宽无间断间隔”的字符，它的编码是 FEFF。而 FFFE 在 UCS 中是不存在的字符，所以不应该出现在实际传输中。UCS 规范建议我们在传输字节流前，先传输字符 "Zero Width No-Break Space"。这样如果接收者收到 FEFF，就表明这个字节流是 Big-Endian 的；如果收到FFFE，就表明这个字节流是 Little- Endian 的。因此字符 "Zero Width No-Break Space" （“零宽无间断间隔”）又被称作 BOM(即Byte Order Mark)。

作者：慕森王
链接：https://www.imooc.com/article/26166
来源：慕课网

unicode保存的文本文件二点两个字节的文件头
用来表明编码字节序的
byte order mark
windows 记事本软件会为文本文件添加bom头
现在大多数软件都可以识别，不用加
linux里面是不加的

23. group 类型的标签有哪些？
optgroup
colgroup
hgroup
thead 它的display 叫table header group
fileset
framset？

24. 什么是 SEO？
 Search Engine Optimism
 布置页面能让页面在搜索结果中尽量靠前

25. 分别列出每种常见浏览器的内核名称（自己查）。

1.、IE浏览器内核：Trident内核，也是俗称的IE内核；
2、Chrome浏览器内核：统称为Chromium内核或Chrome内核，以前是Webkit内核，现在是Blink内核；
3、Firefox浏览器内核：Gecko内核，俗称Firefox内核；
4、Safari浏览器内核：Webkit内核；
5、Opera浏览器内核：最初是自己的Presto内核，后来是Webkit，现在是Blink内核；
6、360浏览器、猎豹浏览器内核：IE+Chrome双内核；
7、搜狗、遨游、QQ浏览器内核：Trident（兼容模式）+Webkit（高速模式）；
8、百度浏览器、世界之窗内核：IE内核；
9、2345浏览器内核：以前是IE内核，现在也是IE+Chrome双内核

作者：一一Left一一
链接：https://www.jianshu.com/p/f4bf35898719
来源：简书
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

safari chrome new edge new Opera:webkit/blink
IE, old Edge:Trientend
FF:Gekco

26. 列表类标签有哪些？分别如何使用？需要注意些什么？
ol ul li
其直接子结点必须只能是li标签 list item
li内可以是任意其它标签
默认会在每多一层级的列表中缩进
并带有列表项标号，有序和无序的
多个同类项的重复，就应该使用ol/ul标签

 dl dt dd
 一个列表项是**一个dt**和**一个或多个dd**一起算一组
 此标签与ol/ul有些区别，在于
 一个dt可以对应多个dd



28. 为什么不同类型的标签的 fallback 内容要以不同的形式提供？

方便兼容不同浏览器
某些在正常使用时内部有内容，所以fallback不能放在其内部，如script
某些是空的，相当于替换元素，则fallback可以写在其内部，如iframe

29. 分别写出在 head 中设定页面编码，设定 icon，引入样式表的标签

<head>
<meta charset="utf-8">
<meta name="charset" content="utf-8">
<link rel="favicon" href="xxx.ico">
<link rel="stylesheet" href="a.css">
</head>

30. 什么叫做可访问性，html 中为此做了什么工作？
残障人士使用浏览器的方便程度

为视力不好的人设置读屏软件，设计Web Accessibility Initiative -  Accessible Rich Internet Applications，设置role属性来为残障人士提供便利

软件在不同设备上是否能够正常使用
对不不同人群是否能正常使用

aria与role属性用来通过浏览器告诉读屏软件当前元素所代表的常见交互元素，如
下拉框
选项卡
列表框

表格th标签的id与td标签的headers属性

tabindex



31. 写出以下几个符号的 ascii 码：`a，A，0，CR，LF，空格，NBSP`。

97
65
48
13
10
32
160



32. 中英互翻
    * geek
    极客，对计算机方面很感兴趣的人
    * nerd
    书呆子
    * hacker
    黑客
    * edge
    尖端
    * bleeding/cutting edge
    前沿/尖端/可能存在风险的技术
    * HTML 实体
    html entity
    * coordinate
    坐标
    * polygon
    多边形
    * bit
    位
    * byte
    字节
    * alternative
    替换的选择
    * 属性
    attributee
    property
    * obsolete
    已弃用
    * 二进制
    binary
    * 十进制
    decimal
    * 十六进制
    hexadecimal
    * octal
    八进制
    * deprecate
    不建议使用
    * loop
    循环
    * 行
    column
    * 列
    row
    * horizontal
    水平的
    * 语义化
    semanticize(动词)
    semantic（形容词）
    * 可访问性
    accessibility


33. 用文字描述如下选择器将选择哪些（个）元素
  ```css
  div, h1 {}
  所有div 或者和 h1
  div[class] [id="abc"] {}
  存在class属性的div的里面的id值为abc的元素
  div:hover ul li > div {}
  div 处于hover 状态下后代元素中的ul的后代元素中的li的子元素div
  body :active {}
  body的后代元素中处于active状态下的元素
  div:hover::after {}
  div处于激活状态下的after伪元素
  ::selection {}
  所有元素的selection伪元素
  被鼠标选中的部分文字
  只能改color和background color
  :target {}
  所有元素的target伪类
  当前页面的目标元素
  目标元素：id的值为地址栏中#后面的内容的元素
  任何页面里面最多只有一个target元素

  input + ul + p ~ span {}
  和input同为兄弟元素并紧随其后的ul的紧随其后的兄弟元素的p之后紧随的一个span
  ```

34. 分别写出如下几个选择器的优先级
    ```css
    * * * {}
    0, 0, 0, 0
    div * span {}
    0, 0, 0, 2
    div[title] {}
    0, 0, 1, 1
    fieldset legend + input {}
    0, 0, 0, 3
    #some #thing .not:hover .abc:hover {}
    0, 2, 2, 2
    0 2 4 0
    ```

35. `em,px,rem,vw,vh` 分别代表多长？
em:当前元素font-size的大小
当用在font-size上时，取父元素的字号大小
px:一个像素的长度
css 像素，操作系统分辨率和显示器的物理分辨率相同时，一个px代表显示器的物理像素
rem:html（根元素）的font-size的大小
vw:视口宽度的百分之一
vh:视口高度的百分之一

vmax
vmin

vw vh 中的较大/小者

ch 0的宽度
ex x的高度


36. 显示器的物理分辨率为 `1920x1080`，操作系统设置的分辨率为 `1280x720`，网页的放大倍数为 `110%`，请计算一个 CSS 像素对应多少个显示器物理像素（面积与长度）？
2.475


1.65 长度
面积 2.7225



37. 写出如下代码显示在浏览器后**每个单词**的字号
    ```html
    <style>
      html {
        font-size: 20px;
      }
      section {
        font-size: 10rem;
      }
      p {
        font-size: 24px;
      }
      span {
        font-size: 150%;
      }
      .sucks {
        font-size: inherit;
      }
    </style>
    <body> 20px
      <section> 200px
        <h2>Brown</h2>  （300px）
        h2的字号不是继承下来的，会随着外层元素的字号变大而变大
        200*1.5
        <p>quick</p>  （24px)
        <p>jumps (24px) <span>over(36px) <span>lazy (36*1.4=54px)</span> dog (36px)</span></p>
        <p class="sucks">sucks (200px)</p>
      </section>
    </body>
    ```

38. 如何给css添加注释

ctrl + / 或者任意字符在选择器开头破坏css格式

39. 指出如下css代码中的错误
    ```
    p,h1,{

        background-color: rgba:(abc)
        font-varient; abc;
        colr: #ff048;
        font: "serif" 25px;
    }
    ```

    选择器和大括号之间有符号
    rgba和小括号之间有符号，第一项声明后没有分号，括号内容应该是百分比或者数字r，g,b,a
    第二项声明用了分号而不是冒号
    font-variant 和 colr拼错了
    font-variant:small-caps
    应该是 font:25px serif;

40. 写出如下结构中div元素的所有后代/祖先/子/父/兄弟元素
    ```html
    <section>
      <h1><span></span></h1>
      <main>
        <h2></h2>
        <div>
          <ul>
            <li><a href=""><img src="" alt=""></a></li>
          </ul>
        </div>
        <aside>
          <h3></h3>
        </aside>
      </main>
    </section>
    ```

    所有后代:ul li a img
    祖先:main section html
    子:ul
    父:main
    兄弟元素:h2 aside

41. 常见的替换元素有哪些？它们与非替换元素最大的区别什么？
<iframe>
<video>
<embed>
<img>
input
checkbox
radio
object
canvas
audio

HTML spec also says that an <input> element can be replaced, because <input> elements of the "image" type are replaced elements similar to <img>. However, other form controls, including other types of <input> elements, are explicitly listed as non-replaced elements (the spec describes their default platform-specific rendering with the term "Widgets").

Objects inserted using the CSS content property are anonymous replaced elements. They are "anonymous" because they don't exist in the HTML markup.

区别：they're elements whose contents are not affected by the current document's styles. The position of the replaced element can be affected using CSS, but not the contents of the replaced element itself.(MDN)

一般没有后代元素，标签，结点
有内在宽高
button是替换元素，但是有后代

42. 让 CSS 在 HTML 页面上生效有哪些方法，分别写出来。

1）使用link标签：<link rel="stylesheet" href="print.css" media="print">
2）使用style 标签
3）在文件开头使用@import 指令 @import "../aa.css";
4）在元素标签里用style 属性内联 <div style="color:red;font-size:45px;"></div>



43. 如何让页面打印时应用不同的效果？

加入属性media="print"
用link标签为页面设置打印时生效的样式表，并设置不同的样式

44. 假设 index.html 的路径为 http://user.coding.me/task/index.html ，如下引用的a.css和b.css路径分别为？
    ```html
    <!-- index.html的内容 -->
    <style>
        @import "../a.css";
    </style>
    ```
    ```css
    /* a.css的内容 */
    @import "b.css";
    ```
a.css:http://user.coding.me/a.css
b.css:http://user.coding.me/b.css

注释里b.css出现在a.css里面



45. 写出满足如下条件的选择器
    * 第  8个子结点之后，倒数第 5 个子结点之前的li结点
    * 【类名】以“damiao-”开头的元素
    class属性中的每个单词
    * rel 属性中有 nofollow 这个单词的标签

 li:nth-child(n+8):nth-last-child(-n+5)
 [class^="damiao-"],[class*=" damiao- "]
 rel~="nofollow"



46. 链接伪类的几种状态书写的顺序是什么？为什么？

link visited focus hover active
因为focus hover active在前面的话会被同等优先级但是位置在后的静态伪类 link 和 visited 的覆盖，因为链接的状态无论动静全是link/visited/unvisited



47. 如下 font 属性的值哪一个是书写正确的？
    * font: serif 24px;
    * font: serif bold 24px/1.2;
    * font: bold 24px/1.2 serif;（这个）

48. 详述你对盒模型的理解。

我的理解是盒模型通过各元素各边框之间的位置关系画出美观和方便交互的浏览器界面
元素之间的嵌套关系和宽高的设置对盒模型很重要

每个元素都会生成一个或多个矩形框
这些矩形框可以嵌套
每个矩形框可以有可选的外边距 边框 内边距
外边距可以为负，另外两者不行
宽度设定 margin- border- padding- content-box
可以为每个盒子设置宽高，用width height属性
宽高实际设置的时哪个盒子的大小取决于box-sizing属性的值
可以时border-box的宽高，也可是content-box的

49. 元素的高度写百分比在什么情况下【无效】，为什么？在什么情况下【有效】，有效时是以哪个元素的高度为基准值？

行内非替换元素设定高度无效
对常规流块级元素而言，html/body没有设定初始值的情况下无效，因为子元素会把父元素撑高，同时父元素的高度会影响子元素的取值，形成一个逻辑错误。

给一个祖先元素和其后代元素定位的同时给祖先元素设定高度，会以离子元素最近的祖先元素的高度为基准值生效

设定html和body的高度之后常规流块级子元素以父元素高度为基准值生效。


父元素的高度为auto时

在父元素的高度不由子元素撑起时，生效

50. 字体的 italic 与 oblique 的区别是？
italic是另一个专门设计好的斜体字体， 而oblique则是在正体的文字基础上变幻出来的一个斜体字
现在这两个差不多了，大多数情况下浏览器会优先选择为这个字体设计的斜体字 italic


51. 什么是模拟信号？什么是数字信号？它们的区别是？

以二进制形式计算表达信号的时候叫数字信号
衰减严重，误差小，适合近距离传输

而当我们直接使用设备介质里面的物理量的来作为我们最终表达的这个信号的时候，是模拟信号
衰减比较小，误差大，适合远距离传输

模拟：将设备，介质中的物理量直接读出经过转换后使用
数字：将设备，介质中的物理量读出并理解为0和1

区别：数字信号几乎可以完全消除误差
模拟信号会被干扰

数字信号传输距离近，抗干扰能力弱
模拟信号传输距离远，抗干扰能力强



52. 将如下 markdown 转换成 html
    ```md
    ## 四季变换

    一年有四季，
    四季有其对应的节气

    * 春
        - 立春
        - 惊蛰
        - 元宵
    * 夏
        - **小米**发布会
        - 华为发布会
    * 秋
        - 开学了
        - 军训了
    * 冬
        - 下雪了
            + 打雪仗了
        - 来暖气了
        - 开空调了

    > 知识就是力量，法国就是培根。

    [春](http://baike.baidu.com/item/%E6%98%A5/6983693)
    ![春](https://www.google.com.hk/images/nav_logo242_hr.png)




    <!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>JS Bin</title>
</head>
<body>
<h2>四季变换</h2>
  <p>一年有四季，</p>
  <p>四季有其对应的节气</p>
n
  <ul><span>春</span>
    <li>立春</li>
    <li>惊蛰</li>
    <li>元宵</li>
  </ul>
  <ul><span>夏</span>
    <li><strong>小米</strong>发布会</li>
    <li>华为发布会</li>

  </ul>
  <ul><span>秋</span>
    <li>开学了</li>
    <li>军训了</li>
  </ul>
  <ul><span>冬</span>
    <li>下雪了
      <ul><li>打雪仗了</li></ul>
    </li>
    <li>来暖气了</li>
    <li>开空调了</li>
  </ul>

  <blockquote>知识就是力量，法国就是培根。</blockquote>

  <a href="http://baike.baidu.com/item/%E6%98%A5/6983693">春</a>

 <img src="https://www.google.com.hk/images/nav_logo242_hr.png" alt="春">

</body>
</html>
    ```
53. 如下表单提交后将跳转到什么地址
    ```html
    <form action="https://www.baidu.com/s" target="_blank">
      <input type="text" value="bb" name="a">
      <input type="checkbox" name="b" id="b" value="123" checked>
      <input type="checkbox" name="b" id="b" value="456" checked>
      <input type="checkbox" name="b" id="b" value="789">
      <input type="radio" name="c" id="c" value="a2">
      <input type="radio" name="c" id="c" value="a5" checked>
      <input type="radio" name="c" id="c" value="a4">
      <select name="select">
        <option value="01">0001</option>
        <option value="02">0002</option>
        <option value="03" selected>0003</option>
        <option value="04">0004</option>
        <option value="05">0005</option>
      </select>
      <button>提交</button>
    </form>
    ```
https://www.baidu.com/

s?a=bb&b=123&b=456&c=on&select=03

54. 列出 input 的 type 有哪些值，以及为各个值时分别需要怎么使用。
button
关联图片，或者用value加入文字
checkbox
单选
color
选择色号
date
选择年月日
datetime-local
选择时间和日期
email
输入邮箱地址
file
上传文件
accept

hidden
隐藏选项，以此设置一些默认的值
image
上传图片
src alt

month
选择月份
number
选择数字，可以设置默认值
max 和 min 一起用（？）

password
输入的字符不可见
radio
单选：在name属性相同是可以从多个选项中选出一项
range
在一个长条中选出一个大概的值
min max step
reset
重置为默认值
search
显示一个可以输入搜索词的输入框
submit
提交
tel
输入电话号码
text
显示一个输入框
max length minlength 一起用
time
输入时间
url	输入链接
week
输入第几年的第几周

55. 想要让一个文本输入框在页面打开后自动获得光标要怎么办？
在标签内加入autofocus属性

56. 如何在文本框里放置提示性文字？
在标签内加入placeholder=""


57. option 标签的主体内容太长影响用户体验，你会如何解决？
      在css 中加入设置合适的height值并加入overflow:scroll声明

 用其它标签画出select的样式
 github等前端网站有现成的

 将内容截断只展示一部分，但将完整内容写title属性上

58. 想要在 textarea 标签中默认显示一段 html 代码最安全的做法是什么？、
在textarea 标签里嵌套 <pre><code></code></pre>


将开始的尖括号转义

59. 如何禁用一组输入框？
在这组标签里加入disabled属性


<fieldset disabled>
<legend></legend>
input*3
</fieldset>


60. 如下表格渲染出来后是什么效果？不要直接将代码贴入jsbin中看效果
最右边有一块棕色，背景色为粉色
左边有一块红色
红色下方一块绿色

    ```html
    <table border=1>
      <caption>美国队长</caption>
      <col>
      <col bgcolor=red>
      <col>
      <colgroup bgcolor=pink>
        <col>
        <col>
        <col bgcolor=brown>
      </colgroup>
      <thead>
        <tr>
          <th>01</th>
          <th>02</th>
          <th>03</th>
          <th>04</th>
          <th>05</th>
          <th>06</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>abc</td>
          <td colspan=3 rowspan=2>abc</td>
          <td>abc</td>
          <td>abc</td>
        </tr>
        <tr>
          <td>abc</td>
          <td colspan=2 rowspan=3>abc</td>
        </tr>
        <tr bgcolor=lightgreen>
          <td colspan=2 rowspan=2>abc</td>
          <td>abc</td>
          <td>abc</td>
        </tr>
        <tr>
          <td>abc</td>
          <td>abc</td>
        </tr>
      </tbody>
    </table>
    ```



61. 写出如下标签或属性值的英文全称

    标签：html,div,p,a,em,tr,th,td,col,ul,ol,li,dl,dt,dd,pre,nav
    hypertext markup language
    division
    paragraph
    anchor
    emphasis
    table row
    table header
    table data
    colum
    unordered list
    ordered list
    list item
    definition list
    definition term
    definition description
    preformatted
    navigator



    属性：coord,rect,poly,href,src
    coordinate
    rectangular
    polygon
    hypertext reference
    source

62. 请说出你对命令行程序的理解，以及其与 GUI 程序的区别

命令行是用文字命令控制电脑,参数来调整行为
但是gui可以用鼠标和其它方式，并且文件夹等路径用图像表示

63. 请确认以下标签分别属性什么类别（Content Category）？

    p, meta, h1, fieldset, option, input, area

P:flow content
meta:metadata content; flow/phrasing content if the itemprop attribute is present
h1:heading content
fieldset:form-associated content
option:none
input:phrasing content
area:flow content if it is a descendant of a <map> element


64. 解释 box-sizing 可以取哪些值，以及每个值的意义

border-box:此时设置的宽高为元素border-box的宽高
padding-box：此时设置的宽高为元素padding-box的宽高

65. 简述 ie7 市场份额比 ie6 低的原因并在网络上找出目前各大浏览器在中国和全球的市场份额

因为中国很大一部分家庭电脑在 windows XP 流行的时候装了这个系统的盗版，并且也因为盗版，很多电脑没有升级系统，因此在没有很大推力去接触新版本浏览器的情况下，国内用户对XP内置的ie6浏览器接受程度很高。一些政府，银行的网站只兼容ie6，导致这个版本一直没有被淘汰。

ie7只能装在xp上，而用xp的用户大概率是不会升级浏览器的
很多老旧的软件系统只能兼容ie6

can I use

Nov 2019
Worldwide：
Chrome 64.3%
Safari 16.68%
Firefox 4.49%
Samsung Internet 3.27%
UC browser 2.95%
Opera 2.35%

China：
Chrome 63.26%
UC browser 9.8%
QQ browser 8.82%
Safari 8.72%
Android 1.77%
Firefox 4.49%

https://gs.statcounter.com/browser-market-share/all/china/#monthly-201811-201911



66. 画出如下代码中 div 及其子元素的渲染结果，并指出 p 标签中【每个行内元素的，内容区，行内框的范围】，p 元素的行框，并指明理论的行框高度。有尺子的可以以 1mm 为 2px 来绘制。

P:
inline box:
76px+15px+4px=95px

86px

span.a:
inline box:24px
span.b:
inline box:36px
span.c:
content box:0*60px
img:
content box:46*46px





    ```html
    <!DOCTYPE html>
    <html>
    <head>
      <meta charset="utf-8">
      <title>JS Bin</title>
      <style>
        p {
          font-size: 20px;
          line-height: 120%;
          margin: 30px;
          margin-left: auto;
          margin-right: -20px;
          width: 300px;
          background-color: tan;
        }

        这几项是设定布局的


        .a {
          display: inline-block;
        }

        .b {
          font-size: 30px;
          vertical-align: 15px;
        }

        .c {
          display: inline-block;
          width: 60px;
          height: 60px;
          background-color: pink;
          margin: 8px;
        }

        img {
          box-sizing: border-box;
          width: 50px;
          height: 50px;
          border: 2px solid;
          margin: 4px;
          vertical-align: -10px;
          margin-bottom: -5px;
        }
        div {
          width: 400px;
          border: 1px dotted;
        }
      </style>
    </head>
    <body>
      <div>
        <p>
          <span class=a>foo</span>
          <span class=b>bar</span>
          <span class=c></span>
          <img src="https://drscdn.500px.org/photo/205228769/m%3D1170_k%3D1/d721302d063d447aa3bd6301dc1cba87" alt="">
        </p>
      </div>
    </body>
    </html>
    ```
