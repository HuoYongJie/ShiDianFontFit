# ShiDianFontFit （持续关注[信息公告牌](https://github.com/CharlinFeng/Show)）
####全自动的屏幕字体适配,一键实现微信，QQ，新浪微博，网易的效果
OC,兼容swift
Xcode 8
时间有限，先写个简化版本。

####先说为什么有这个，最近做了一个项目，使用的是苹果默认的布局，刚好这个项目所有页面的文字都比较小，在iphone5上面完美，6上面文字就有点小了，
6p上面基本就小的可怜了。最早期苹果的流式布局在客户眼里是不可理解的布局。他要的效果是，大屏幕，应该有对应比例的大字和对应更大的间距。
此效果在网易新闻，微信上面最明显：不同设备字体需要根据对应分辨率调整，
更重要的是，字体变大了，对应的布局的宽高也要变化。

####1.直接拖拽ShiDianFontFit文件夹到项目就可以了，所有的label和button都直接有了自动缩放效果。
####2.如果某个控件不需要这个效果，请设置tag = 999
####3.适配UILabel
####4.适配UIButton
####5.适配UITextfield
####6.适配UITextView
####7.适配NSLayoutConstraint


####8.更改了label的对应的约束也需要对应缩放的。约束变化是一个非常复杂的操作，这里不能全部缩放，因为只是和label或者button有关的才缩放，
到xib里面选中你需要缩放的layoutConstraint，里面有一个Identifier，请填写任意非空字符，此条约束即可以缩放。



##### 注意：1.约束添加了Identifier才会缩放，且考虑了线程，优化了性能。
##### 注意：2.缩放的规则是屏幕的宽度比（相对ip5）


####我做过测试了，将6,6p的截图和5的截图，缩放到同一个分辨率下，三者是完全一样大的。基于Runtime一键使用。
