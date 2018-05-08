# Tabchange
页面中Tab栏在PC端竖向排列，手机端横向排列，并且可以左右滑动

我在最开始拿到这个需求的时候，用css就实现了左右滑动，但是会自动出现滚动条，而滚动条是我不需要的，但是目前还没有找到办法将滚动条去掉，当时的实现思路是：

tab栏在手机端的时候肯定会超出屏幕，因此设置了超出部分隐藏，即:

.myTabPhone ul{
    display: -webkit-box;
    overflow: hidden;
    overflow-x:auto;
}
在想办法将滚动条去掉的过程中，找到了这个方法：但是这仍然不是我想要的结果；

.myTabPhone ul::-webkit-scrollbar {
    display: none;
}
最后，看到了一篇帖子，然后做出了现在的效果

