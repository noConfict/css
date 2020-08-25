

# 5.boot对于弹性布局的封装

d-*-inline/inline-block/block/table/flex/inline-flex*:sm/md/lg/xl 关于弹性的设置1.主轴方向 flex-*-/row/row-reverse/column/column-reverse2.是否换行 flex-*-wrap/nowrap;3.项目在主轴上的排列方式 justify-content-*-between/around/start/center/end4.交叉轴对齐方式 align-items-*-center/start/end/baseline

# 6.表单

文本框和密码框的基本类，form-control由于不同页面对input的需求不同，需要自己修改大量样式

四.组件（代码不需要背，对照笔记可以完成）

boot把页面中常用的js特效进行了封装，让我们快速开发不需要我们写js，使用自动属性来调用事件1.哪个元素激活的事件2.事件激活后影响的是哪个元素(影响的目标)

## 1.按钮组

结构div.btn-group 水平按钮组 >.btndiv.btn-group-vertical  垂直按钮组 >.btn  水平按钮组 >.btn

## 2.下拉菜单

结构div.dropdown  相对定位 >.btn  .dropdown-toggle  在最后添加一个向下的箭头提示 +ul.dropdown-menu  display：none；事件：1.在按钮上写自定属性来激活事件 data-toggle="dropdown"2.事件目标，由于btn和ul有一个共同结构父级，不需要手动绑定目标

## 3.信息提示框

结构div.alert .alert-info  .alert-dismissible  让内部的小×字体颜色同父元素定义的字体颜色 >.btn.close事件1.在×上写自定属性data-dismiss="alert"2.不需要指定目标

## 4.导航

### ①水平导航

ul.nav  弹性，x轴，可换行，去点，去左内边距 >li.nav-item  >a.nav-link

### ②选项卡导航

结构ul.nav.nav-tabs  让所有nav-link有边框 >li.nav-item  >a.nav-link   .active  设置当前a为选中状态div.tab-content >div.tab-pane  内容都隐藏   .active   内容显示事件1.给a写自定属性 data-toggle="tab"2.事件目标需要绑定id  div#d1  a[href="#d1"]

### ③胶囊导航

结构ul.nav.nav-pills  让所有nav-link有边框 >li.nav-item  >a.nav-link   .active  设置当前a为选中状态div.tab-content >div.tab-pane  内容都隐藏   .active   内容显示事件1.给a写自定属性 data-toggle="pills"2.事件目标需要绑定id  div#d1  a[href="#d1"]

# 5.导航栏

div.navbar  弹性，x轴，主轴两端对齐，交叉轴居中  .navbar-expand-* 主轴x，不换行，主轴起点对齐 >ul.navbar-nav 弹性，y轴。配合祖先元素的navbar-expand-*让主轴变为x  >li.nav-item  >a.nav-linknavbar-expand-*响应式导航栏，在某个屏幕以上li横向显示，在这个屏幕以下li纵向显示

# 6.折叠

.btndiv.collapse  display:none;事件1.给btn添加自定义属性 data-toggle="collapse"2.要绑定id  data-target="#zd"

# 7.卡片

div.card  弹性，y轴 >div.card-header +div.card-body +div.card-footer

# 8.手风琴（卡片+折叠）

div#parent >div.card>div.card-header>a [data-toggle="collapse"]      +div.collapse[data-parent="#parent"]        >div.card-body

# 9.折叠导航栏

div.navbar.bg-dark  .navbar-dark  让内部a标签变为浅色         让内部按钮为浅色         让内部导航文本为浅色  .navbar-expand-lg 让内部ul的li在lg以上横向，在lg以下纵向显示           让内部的按钮在lg以上隐藏，在lg以下显示           配合.navbar-collapse让折叠的部分在lg以上显示 >a.navbar-brand  行内块，字号，行高，内外边距 +button.navbar-toggler  与父元素.navbar-expand-lg配合   >span.navbar-toggler-icon +div.collapse  display：none   .navbar-collapse 配合父元素.navbar-expand-lg，让折叠的部分在lg以上显示  >ul.navbar-nav    >li.nav-item>a.nav-link

# 10.媒体对象

div.media  弹性，x轴 >img +div.media-body

# 11.模态框 

div.modal  固定定位 >div.modal-dialog  >div.modal-content   >div.modal-header  内容的头部信息   +div.modal-body   内容主题   +div.modal-footer  内容的底部

# 12.徽章

.badge  基本类.badge-danger/info.....badge-pill 胶囊徽章

#  13.巨幕

jumbotron  巨大的内边距，有灰色背景，有圆角

# 14.面包屑导航

ul.breadcrumb >li.breadcrumb-item修改中间的链接字符.breadcrumb-item + .breadcrumb-item::before{ content:">";}

# 15.分页组件

ul.pagination  弹性，x轴 >li.page-item  让第一个li和最后一个li中的a有圆角  >a.page-link  让第一个li和最后一个li中的a有圆角

# 16.进度条

div.progress >div.progress-bar   .w-100   .progress-bar-striped   .progress-bar-animated

# 17图片居中

```
<div class="text-center">
	<img class="w-25 " src="图片路径" alt="">
</div>
```





 

 

 

 

 

 