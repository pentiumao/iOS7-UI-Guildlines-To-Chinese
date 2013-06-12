###Bars

#### 状态栏(The Status Bar)
状态栏用来展示设备以及当前环境的重要信息。

默认状态栏 | 浅色内容状态栏
:-----------:  | :-----------: 
![status bar](https://developer.apple.com/library/prerelease/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/status_bar_default_2x.png)  | ![status bar](https://developer.apple.com/library/prerelease/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/status_bar_light_2x.png)
 
你可以为整个应用全局设置状态栏的样式也可以为每个View Controller单独设置。想获取更多信息，请查阅[UIApplication Class Reference](https://developer.apple.com/library/prerelease/ios/documentation/UIKit/Reference/UIApplication_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006728)来了解 *UIStatusBarStyle* 常量以及查阅[UIViewController Class Reference](https://developer.apple.com/library/prerelease/ios/documentation/UIKit/Reference/UIViewController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006926)来了解 *preferredStatusBarStyle* 属性。

##### 外观和行为(Appearance and Behavior)

状态栏是透明的。无论设备在哪种朝向状态下，状态栏都会在屏幕的顶端出现并展示了用户需要的信息，比如网络状况，日期以及电量。

##### 指导(Guidelines)

尽管状态栏并不像其它控件一样使用频繁，但是明白它在你的应用中的作用也是非常重要的。

* **轻易不要隐藏状态栏。** 因为状态栏是透明的，所以通常没有必要隐藏它。一旦它被隐藏意味着用户如果要看时间或者查看Wi-Fi状态必须跳出你的应用。

* **如果用户在全屏观看视频或浏览其它多媒体时应该隐藏状态栏和其它所有控件。** 如果选择如此，需要保证用户能够通过轻点屏幕来呼出状态栏或者相应的控件。除非有特殊情况，应尽量避免重新定义其它手势来达到此目的，因为用户很难发现并记住它。

* **不要创建自定义的状态栏。** 用户依赖系统提供的状态栏的一致性。尽管你可能在应用中隐藏它，但是创建自定义的状态栏是不被推荐的。

* **给状态栏设置一个适合你应用的内容颜色。** 默认显示黑色内容的状态栏和浅色内容的应用比较搭配。而浅色内容的则比较适合深色内容的应用。

* **尽可能不要在状态栏上放置无用的内容。** 特别是，不要试图让用户通过点击状态栏获取内容或者激活应用的控件。

* **在适当的情况下显示网络活动指示器。** 网络活动指示器可以告诉用户漫长的网络访问正在进行中。想了解如何实现，请查阅[Network Activity Indicator](https://developer.apple.com/library/prerelease/ios/documentation/UserExperience/Conceptual/MobileHIG/Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW44)。

