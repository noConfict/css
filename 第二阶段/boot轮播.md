# 焦点轮播图

div.carousel#demo  相对定位第一部分，轮播图片 div.carousel-inner  w-100 溢出隐藏   >div.carousel-item  w-100 隐藏     .active  显示    >img事件，要写在最外层div中 data-ride="carousel"第二部分，轮播指示器 ul.carousel-indicators  绝对定位，弹性  >li需要重写样式.carousel-indicators li{ width: 12px;height: 12px; border-radius: 50%; background: #fff; margin-left: 0.25rem; margin-right: 0.25rem;}.carousel-indicators .active { background: #0aa1ed;}第三部分，左右箭头a.carousel-control-next/pre >span.carousel-control-next/pre-icon事件 a data-slide="next/pre" href="#demo".carousel-control-prev,.carousel-control-next{ width: 4%;height: 20%; background-color: #aaa; border-radius: 0.25rem; top:40%;}

