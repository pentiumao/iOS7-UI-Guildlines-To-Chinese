##Bars

#### 状态栏(The Status Bar)
状态栏用来展示设备以及当前环境的重要信息。

默认状态栏 | 浅色状态栏
:-----------:  | :-----------: 
![status bar](https://developer.apple.com/library/prerelease/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/status_bar_default_2x.png)  | ![status bar](https://developer.apple.com/library/prerelease/ios/documentation/UserExperience/Conceptual/MobileHIG/Art/status_bar_light_2x.png)
 
你可以为整个应用全局设置状态栏的样式也可以为每个View Controller单独设置。想获取更多信息，请查阅[UIApplication Class Reference](https://developer.apple.com/library/prerelease/ios/documentation/UIKit/Reference/UIApplication_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006728)来了解*UIStatusBarStyle*常量以及查阅[UIViewController Class Reference](https://developer.apple.com/library/prerelease/ios/documentation/UIKit/Reference/UIViewController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006926)来了解*preferredStatusBarStyle*属性。

##### 外观和行为(Appearance and Behavior)

状态栏是透明的。无论设备在哪种朝向状态下，状态栏都会在屏幕的顶端出现并展示了用户需要的信息，比如网络状况，日期以及电量。

##### 指导(Guidelines)

Although you don’t use the status bar in the same way that you use other UI elements, it’s important to understand its function in your app.

**Think twice before hiding the status bar**. Because the status bar is transparent, it’s not usually necessary to hide it. Permanently hiding the status bar means that users must switch away from your app to get the time or find out whether they have a Wi-Fi connection.

**Consider hiding the status bar—and all other app UI—while people are actively viewing full-screen media**. If you do this, be sure to allow people to retrieve the status bar and appropriate app UI with a single tap. Unless you have a very compelling reason to do so, it’s best to avoid defining a custom gesture to redisplay the status bar because users are unlikely to discover such a gesture or remember it.

**Don’t create a custom status bar**. Users depend on the consistency of the system-provided status bar. Although you might hide the status bar in your app, it’s not appropriate to create custom UI that takes its place.

**Choose a status bar content color that coordinates with your app**. The default appearance displays dark content, which looks good on top of light-colored app content. The light status bar content looks good on top of dark-colored app content.

**As much as possible, avoid putting distracting content behind the status bar**. In particular, you don’t want to imply that users should tap the status bar to access content or activate controls in your app.

**When appropriate, display the network activity indicator**. The network activity indicator can appear in the status bar to show users that lengthy network access is occurring. To learn how to implement this indicator in your code, see Network Activity Indicator.

