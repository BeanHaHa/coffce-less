coffce-less
---
一个模块化的Less基础类库，包含Reset、栅格系统、原子类、常用class和浏览器兼容等模块。


##使用：
首先在你的less里引入 coffce.less，再根据你的需要，调用各个模块的init初始化模块

    npm install coffce-less
```
// your less
@import "coffce";

// reset
.init-reset();

// 生成栅格系统
.init-grid(...);

// 生成常用class
.init-common(...);

// 生成margin和padding
.init-margin(...);
.init-padding(...);

// 生成以上所有模块，这个方法对各个模块使用的都是默认参数，建议最好不要使用它
.init-all();
```
##Reset
**.init-reset()**<br>
重置所有标签样式

##栅格模块
**.init-grid(@count, @padding, @width)**<br>
生成一套与Bootstrap相仿的简易栅格化模块，如果你不了解栅格化，可以上Bootstrap官网看看文档，十分简单。

参数 | 默认值 | 描述
---- | ----- | ---
@count | 12 | 栅格列数
@padding | 15px | 每个栅格左右的padding
@width | 100% | container的宽度，设为百分比则为响应式布局
@pre | cf | 前缀，默认为cf，生成后的class为.cf-xxx


**生成后的class：**

class | 描述
----- | ----
.cf-container | 容器
.cf-row | 行，放置在cf-container中
.cf-column-1、.cf-column-2... | 列，放置在cf-row中
.cf-column-offset-1、.cf-column-offset-2... | 列偏移

##margin和padding模块
**.init-margin(@min, @max, @space, @pre)**<br>
**.init-padding(@min, @max, @space, @pre)**<br>
生成指定范围的margin和padding，作为栅格化的一些补充。如默认参数min: 0, max: 100, space: 5，将生成4个方向的margin-0、5、10...100。

参数 | 默认值 | 描述
---- | ----- | ---
@min | 0 | 最小值
@max | 100 | 最大值
@space | 5 | 步长
@pre | cf | 前缀，默认为cf，生成后的class为.cf-xxx


**生成后的class(下面的5只是个例子)：**

margin | padding | 描述
----- | ----- | -----
.cf-mt-5 | .cf-pt-5 | margin-top: 5px 与 padding-top: 5px
.cf-mb-5 | .cf-pb-5 | margin-bottom和padding-bottom
.cf-ml-5 | .cf-pl-5 | margin-left和padding-left
.cf-mr-5 | .cf-pr-5 | margin-right和padding-right
.cf-mlr-5 | .cf-plr-5 | margin-left和margin-right<br>padding-left和padding-right
.cf-mtb-5 | .cf-ptb-5 | margin-top和margin-bottom<br>padding-top和padding-bottom
.cf-ma-5 | .cf-pa-5 | margin和padding

##common模块
**.init-common(@pre)**<br>
生成一些常用的class，持续更新中，具体有哪些可以直接看coffce.less文件。

参数 | 默认值 | 描述
---- | ----- | ---
@pre | cf | 前缀，默认为cf，生成后的class为.cf-xxx

##浏览器兼容与前缀
这部分不需要init，具体有哪些可以直接看coffce.less文件。<br>
提供一些函数为css作简单的兼容处理，如在IE上使用滤镜模拟rgba、opacity等。<br>
提供一些函数为css加上前缀，不建议使用。建议用autoprefixer这类gulp插件来自动加上前缀。

##License
MIT



    
    

