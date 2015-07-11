coffce-less
---
一个模块化的Less基础类库，包含栅格系统、原子类、常用class和浏览器兼容等模块。


##使用：
首先在你的less里引入 coffce.less，再根据你的需要，调用各个模块的init初始化模块

    npm install coffce-less
```
// your less
@import "coffce";

// 栅格系统
.init-grid();
// 常用class
.init-common();
// margin原子类
.init-margin();
// padding原子类
.init-padding();
// 生成全部模块
.init-all();
```

##栅格模块
**.init-grid(@count, @padding, @width)**

参数 | 默认值 | 描述
---- | ----- | ---
@count | 12 | 栅格列数
@padding | 15px | 每个栅格左右的padding
@width | 100% | container的宽度，设为百分比则为响应式布局


**用法与Bootstrap相同：**

class | 描述
----- | ----
.cf-container | 容器
.cf-row | 行，必须放置在cf-container中
.cf-column-1、.cf-column-2... | 列，必须放置在cf-row中
.cf-column-offset-1、.cf-column-offset-2... | 列偏移

##margin和padding模块
todo
##common模块
todo
##License
MIT



    
    

