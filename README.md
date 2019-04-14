简介
animate.css 是一个来自国外的 CSS3 动画库，它预设了抖动（shake）、闪烁（flash）、弹跳（bounce）、翻转（flip）、旋转（rotateIn/rotateOut）、淡入淡出（fadeIn/fadeOut）等多达 60 多种动画效果，几乎包含了所有常见的动画效果。

虽然借助 animate.css 能够很方便、快速的制作 CSS3 动画效果，但还是建议看看 animate.css 的代码，也许你能从中学到一些东西。

兼容
浏览器兼容：当然是只兼容支持 CSS3 animate 属性的浏览器，他们分别是：IE10+、Firefox、Chrome、Opera、Safari。

使用方法
1、引入文件
<link rel="stylesheet" href="animate.min.css">
2、HTML 及使用
<div class="animated bounce" id="dowebok"></div>
给元素加上 class 后，刷新页面，就能看到动画效果了。animated 类似于全局变量，它定义了动画的持续时间；bounce 是动画具体的动画效果的名称，你可以选择任意的效果。

如果动画是无限播放的，可以添加 class infinite。

你也可以通过 JavaScript 或 jQuery 给元素添加这些 class，比如：

$(function(){
    $('#dowebok').addClass('animated bounce');
});
有些动画效果最后会让元素不可见，比如淡出、向左滑动等等，可能你又需要将 class 删除，比如：

$(function(){
    $('#dowebok').addClass('animated bounce');
    setTimeout(function(){
        $('#dowebok').removeClass('bounce');
    }, 1000);
});
animate.css 的默认设置也许有些时候并不是我们想要的，所以你可以重新设置，比如：

#dowebok {
    animate-duration: 2s;    //动画持续时间
    animate-delay: 1s;    //动画延迟时间
    animate-iteration-count: 2;    //动画执行次数
}
注意添加浏览器前缀。
