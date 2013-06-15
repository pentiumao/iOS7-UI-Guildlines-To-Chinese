## Bars

On This Page

* 	The Status Bar
* 	[Navigation Bar
* 	Toolbar
* 	Toolbar and Navigation Bar Buttons
* 	Tab Bar
* 	Tab Bar Icons
* 	Search Bar
* 	Scope Bar


<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW2"></a>

### The Status Bar 

  The **status bar** displays important information about the device and the current environment.

Default status bar | Light-content status bar
:-----------:  | :-----------: 
<img src="../image/UI Elements/Bars/status_bar_default_2x.png"  width="320" height="20">  | <img src="../image/UI Elements/Bars/status_bar_light_2x.png"  width="320" height="20">

  You can set the style of the status bar globally for the entire app or you can let individual view controllers set the style as appropriate. To learn more, read _[UIApplication Class Reference](../../../UIKit/Reference/UIApplication_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006728)_ for information about the `UIStatusBarStyle` constant and _[UIViewController Class Reference](../../../UIKit/Reference/UIViewController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006926)_ for information about the `preferredStatusBarStyle` property.

<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW31"></a>

#### Appearance and Behavior

  The status bar is transparent. In all orientations, the status bar appears at the upper edge of the device screen and contains information people need, such as the network connection, the time of day, and the battery charge.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW32"></a>

####  Guidelines

  Although you don’t use the status bar in the same way that you use other UI elements, it’s important to understand its function in your app.

  **Think twice before hiding the status bar.** Because the status bar is transparent, it’s not usually necessary to hide it. Permanently hiding the status bar means that users must switch away from your app to get the time or find out whether they have a Wi-Fi connection.

  **Consider hiding the status bar—and all other app UI—while people are actively viewing full-screen media.** If you do this, be sure to allow people to retrieve the status bar and appropriate app UI with a single tap. Unless you have a very compelling reason to do so, it’s best to avoid defining a custom gesture to redisplay the status bar because users are unlikely to discover such a gesture or remember it.

  **Don’t create a custom status bar.** Users depend on the consistency of the system-provided status bar. Although you might hide the status bar in your app, it’s not appropriate to create custom UI that takes its place.

  **Choose a status bar content color that coordinates with your app.** The default appearance displays dark content, which looks good on top of light-colored app content. The light status bar content looks good on top of dark-colored app content.

  **As much as possible, avoid putting distracting content behind the status bar.** In particular, you don’t want to imply that users should tap the status bar to access content or activate controls in your app.

  **When appropriate, display the network activity indicator.** The network activity indicator can appear in the status bar to show users that lengthy network access is occurring. To learn how to implement this indicator in your code, see [Network Activity Indicator](Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW44).

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW3"></a>

### Navigation Bar

  A **navigation bar** enables navigation through an information hierarchy and, optionally, management of screen contents.

<figure class="figure">
	<span class="caption"></span>
	<img src="../image/UI Elements/Bars/nav_bar_7_2x.png" alt="image: ../Art/nav_bar_7_2x.png" width="320" height="44">
</figure>

  A navigation bar is contained in a navigation controller, which is a programmatic object that manages the display of a hierarchy of custom views. To learn more about defining a navigation bar in your code, see [“Navigation Controllers”](../../../WindowsViews/Conceptual/ViewControllerCatalog/Chapters/NavigationControllers.html#//apple_ref/doc/uid/TP40011313-CH2) and [“Navigation Bars”](../UIKitUICatalog/UINavigationBar.html#//apple_ref/doc/uid/TP40012857-UINavigationBar).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW37"></a>

#### Appearance and Behavior

  A navigation bar generally appears at the upper edge of an app screen, just below the status bar. A navigation bar can display the title of the current screen or view, centered along its length. When navigating through a hierarchy of information, users tap the Back button—or swipe from the edge of the device—to return to the previous screen. Otherwise, users can tap content-specific controls in the navigation bar to manage the contents of the screen.

  A navigation bar is translucent and all controls in the bar are borderless.

  On iPhone, a navigation bar always displays across the full width of the screen, and changing the device orientation can change the height of the navigation bar automatically. 

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW45"></a>

#### Guidelines

  You can use a navigation bar to enable navigation among different views, or provide controls that manage the items in a view.

  **When it adds value, use the title of the current view as the title of the navigation bar.** If titling a navigation bar seems redundant, you can leave the title empty. 

  When the user navigates to a new level, two things should happen:

*   The bar title should change to the new level’s title, if appropriate.

*   A back button should appear to the left of the title, and it should be labeled with the previous level’s title.

  **Make sure it’s easy to read the text in the navigation bar.** The system font provides maximum readability, but you can specify a different font, if appropriate.

  **Consider putting a segmented control in a navigation bar at the top level of an app.** This is especially useful if doing so helps to flatten your information hierarchy and make it easier for people to find what they’re looking for. If you use a segmented control in a navigation bar, be sure to choose accurate back-button titles. (For usage guidelines, see [Segmented Control](Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW27).)

  **Avoid crowding a navigation bar with additional controls, even if there appears to be enough space.** The navigation bar should contain no more than a view’s current title, the Back button, and one control that manages the view’s contents. If instead, you use a segmented control in the navigation bar, the bar shouldn’t display a title and it shouldn’t contain any controls other than the segmented control.

  **Use system-provided buttons according to their documented meaning.** For more information, see [Toolbar and Navigation Bar Buttons](#//apple_ref/doc/uid/TP40006556-CH12-SW33). If you decide to create your own navigation bar controls, see [Bar Button Icons](BarIcons.html#//apple_ref/doc/uid/TP40006556-CH21-SW1) for advice on how to design them.

  **If appropriate, customize the appearance of a navigation bar to coordinate with the look of your app.** For example, you can supply a custom background image or tint for the bar and you can specify translucency. In some cases, it can be a good idea to supply a resizable background image; to learn more about creating a resizable image, see [Creating Resizable Images](ResizableImages.html#//apple_ref/doc/uid/TP40006556-CH30-SW1). Take care to provide a background image of the right height in an iOS 7 app; for more information, see [“Navigation Bar”](../TransitionGuide/Bars.html#//apple_ref/doc/uid/TP40013174-CH8-SW3) in _[iOS 7 UI Transition Guide](../TransitionGuide/index.html#//apple_ref/doc/uid/TP40013174)_.

  Make sure that the look of your customized navigation bar is consistent with your app’s appearance and style. For example, don’t combine an opaque navigation bar with a translucent toolbar. Also, it’s best to avoid changing the image, color, or translucency of the navigation bar in different screens in the same orientation.

  **Make sure that a customized back button still looks like a back button.** Users know that the standard back button allows them to retrace their steps through a hierarchy of information. If you decide to replace the system-provided chevron with a custom image, be sure to supply a custom mask image, too. iOS 7 uses the mask to make the button title appear to emerge from—or disappear into—the chevron during transitions.

  **On iPhone, be prepared for the change in navigation bar height that occurs on device rotation.** In particular, make sure that your custom navigation bar icons fit well in the thinner bar that appears in landscape orientation. Don’t specify the height of a navigation bar programmatically; instead, you can take advantage of the [UIBarMetrics](../../../UIKit/Reference/UIBarPositioning_Protocol/Reference/Reference.html#//apple_ref/c/tdef/UIBarMetrics) constants to ensure that your content fits well.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW4"></a>

### Toolbar

  A **toolbar** contains controls that perform actions related to objects in the screen or view. 

<figure class="figure">
	<span class="caption"></span>
	<img src="../image/UI Elements/Bars/toolbar_2x.png" alt="image: ../Art/nav_bar_7_2x.png" width="320" height="44">
</figure>

  A toolbar is typically contained in a navigation controller, which is an object that manages the display of a hierarchy of custom views. To learn more about defining a toolbar in your code, see [“Displaying a Navigation Toolbar”](../../../WindowsViews/Conceptual/ViewControllerCatalog/Chapters/NavigationControllers.html#//apple_ref/doc/uid/TP40011313-CH2-SW4) in _[View Controller Catalog for iOS](../../../WindowsViews/Conceptual/ViewControllerCatalog/Introduction.html#//apple_ref/doc/uid/TP40011313)_ and [“Toolbar”](../UIKitUICatalog/Toolbar.html#//apple_ref/doc/uid/TP40012857-CH14).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW46"></a>

#### Appearance and Behavior

  On iPhone, a toolbar always appears at the bottom edge of a screen or view, but on iPad it can instead appear at the top edge.

  A toolbar is translucent and its items are displayed equally spaced across its width. The precise set of toolbar items can change from view to view, because the items are always specific to the context of the current view.

  On iPhone, changing the device orientation from portrait to landscape can change the height of the toolbar automatically. 

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW47"></a>

#### Guidelines

  Use a toolbar to provide a set of actions users can take in the current context.

  **Use a toolbar to give people a selection of frequently used commands that make sense in the current context.** An alternative is to put a segmented control in a toolbar to give people access to different perspectives on your app’s data or to different app modes (for usage guidelines, see [Segmented Control](Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW27)).

  **Maintain a hit target area of at least 44 x 44 points for each toolbar item.** If you crowd toolbar items too closely together, it’s hard for people to tap the one they want. 

  **Use system-provided toolbar items according to their documented meaning.** See [Toolbar and Navigation Bar Buttons](#//apple_ref/doc/uid/TP40006556-CH12-SW33) for more information. If you decide to create your own toolbar items, see [Bar Button Icons](BarIcons.html#//apple_ref/doc/uid/TP40006556-CH21-SW1) for advice on how to design them.

  **On iPhone, be prepared for the change in toolbar height that occurs on device rotation.** In particular, make sure your custom toolbar icons fit well in the thinner bar that appears in landscape orientation. Don’t specify the height of a toolbar programmatically; instead, you can take advantage of the [UIBarMetrics](../../../UIKit/Reference/UIBarPositioning_Protocol/Reference/Reference.html#//apple_ref/c/tdef/UIBarMetrics) constants to ensure that your content fits well.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW33"></a>

### Toolbar and Navigation Bar Buttons

  iOS makes available many of the standard buttons users see in toolbars and navigation bars.

  As with all system-provided buttons, you should avoid using the buttons described in <span class="x-name-no-link">“Standard buttons available for toolbars and navigation bars (plain style)”</span> to represent actions other than those for which they are designed. In particular, avoid choosing a button based on its appearance, without regard for its documented meaning.

  To find out which symbol names to use to specify these buttons, see the documentation for [UIBarButtonSystemItem](../../../UIKit/Reference/UIBarButtonItem_Class/Reference/Reference.html#//apple_ref/c/tdef/UIBarButtonSystemItem) in _[UIBarButtonItem Class Reference](../../../UIKit/Reference/UIBarButtonItem_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40007519)_.

<div class="tableholder">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW58"></a>
  <table class="graybox" border="0" cellspacing="0" cellpadding="5">
    <caption class="tablecaption"> Table 33-1 Standard buttons available for toolbars and navigation bars</caption>
    <thead>
        <tr>
            <th scope="col" class="TableHeading_TableRow_TableCell"> 
            	Button
			</th>
            <th scope="col" class="TableHeading_TableRow_TableCell">
			  Name
			</th>
            <th scope="col" class="TableHeading_TableRow_TableCell">
			  Meaning
			</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td scope="row">
            
            <img src="../image/UI Elements/Bars/UIButtonBarAction.png">

</td>
            <td>

  Share

</td>
            <td>

  Open an action sheet that lists system-provided and app-specific services that act on the specified content

</td>
        </tr>
        <tr>
            <td scope="row">
  <img src="../image/UI Elements/Bars/UIButtonBarCamera.png">

</td>
            <td>

  Camera

</td>
            <td>

  Open an action sheet that displays a photo picker in camera mode

</td>
        </tr>
        <tr>
            <td scope="row">

<img src="../image/UI Elements/Bars/UIButtonBarAirPlay.png">

</td>
            <td>

  AirPlay

</td>
            <td>

  Open an action sheet that displays nearby AirPlay enabled devices.

</td>
        </tr>
        <tr>
            <td scope="row">

<img src="../image/UI Elements/Bars/UIButtonBarLocate.png">


</td>
            <td>

  Locate

</td>
            <td>

  Use Location Services to display the user’s current location

</td>
        </tr>
        <tr>
            <td scope="row">
            
<img src="../image/UI Elements/Bars/UIButtonBarCompose.png">

</td>
            <td>

  Compose

</td>
            <td>

  Open a new message view in edit mode

</td>
        </tr>
        <tr>
            <td scope="row">

<img src="../image/UI Elements/Bars/UIButtonBarBookmarks.png">

</td>
            <td>

  Bookmarks

</td>
            <td>

  Show app-specific bookmarks

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UIButtonBarSearch.png">

</td>
            <td>

  Search

</td>
            <td>

  Display a search field

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UIButtonBarNew.png">

</td>
            <td>

  Add

</td>
            <td>

  Create a new item

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UIButtonBarTrash.png">

</td>
            <td>

  Trash

</td>
            <td>

  Delete current item

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UIButtonBarOrganize.png">

</td>
            <td>

  Organize

</td>
            <td>
  Move or route an item to a destination within the app, such as a folder

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UIButtonBarReply.png">

</td>
            <td>

  Reply

</td>
            <td>

  Send or route an item to another location

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UIButtonBarRefreshLandscape.png">

</td>
            <td>

  Refresh

</td>
            <td>

  Refresh contents (use only when necessary; otherwise, refresh automatically)

</td>
        </tr>
    </tbody>
  </table>
</div>

  In addition to the buttons shown in <span class="x-name-no-link">“Standard buttons available for toolbars and navigation bars (plain style)”</span>, you can also use the system-provided Edit, Cancel, Save, Done, Redo, and Undo buttons to support editing or other types of content manipulation in your app. The appearance of each of these buttons is provided by its text title. To find out which symbol names to use to specify these buttons, see the documentation for [UIBarButtonSystemItem](../../../UIKit/Reference/UIBarButtonItem_Class/Reference/Reference.html#//apple_ref/c/tdef/UIBarButtonSystemItem) in _[UIBarButtonItem Class Reference](../../../UIKit/Reference/UIBarButtonItem_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40007519)_.

  In addition, you can use the system-provided Info button in a toolbar:

<figure class="figure">
	<span class="caption"></span>
<img src="../image/UI Elements/Bars/info_button_2x.png" alt="image: ../Art/info_button_2x.png" width="22" height="22">
</figure>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW52"></a>

### Tab Bar

  A **tab bar** gives people the ability to switch between different subtasks, views, or modes. 

<figure class="figure">
	<span class="caption"></span>
	<img src="../image/UI Elements/Bars/clock_tab_bar_7_2x.png" alt="image: ../Art/clock_tab_bar_7_2x.png" width="320" height="49">
</figure>

  A tab bar is contained in a tab bar controller, which is an object that manages the display of a set of custom views. To learn more about defining a tab bar in your code, see [“Tab Bar Controllers”](../../../WindowsViews/Conceptual/ViewControllerCatalog/Chapters/TabBarControllers.html#//apple_ref/doc/uid/TP40011313-CH3) and [“Tab Bars”](../UIKitUICatalog/UITabBar.html#//apple_ref/doc/uid/TP40012857-UITabBar).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW48"></a>

#### Appearance and Behavior

  A tab bar appears at the bottom edge of the screen and should be accessible from every location in the app. A tab bar is translucent and it displays icons and text in tabs, all of which are equal in width. When users select a tab, the icon receives the appropriate tint color. 

  On iPhone, a tab bar can display no more than five tabs at one time; if the app has more tabs, the tab bar displays four of them and adds the More tab, which reveals the additional tabs in a list. On iPad, a tab bar can display more than five tabs.

  A tab can display a badge—which is a red oval that contains white text and either a number or exclamation point—that communicates app-specific information.

  A tab bar does not change its height when the device changes its orientation.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW49"></a>

#### Guidelines

  Use a tab bar to give users access to different perspectives on the same set of data or different subtasks related to the overall function of your app. When you use a tab bar, follow these guidelines:

  **Don’t use a tab bar to give users controls that act on elements in the current mode or screen.** If you need to provide controls for your users, use a toolbar instead (for usage guidelines, see [Toolbar](#//apple_ref/doc/uid/TP40006556-CH12-SW4)).

  **In general, use a tab bar to organize information at the app level.** A tab bar is well-suited for use in the main app view because it’s a good way to flatten your information hierarchy and provide access to several peer information categories or modes at one time. 

  **Don’t remove a tab when its function is unavailable.** If a tab represents a part of your app that is unavailable in the current context, it’s better to display a disabled tab than to remove the tab altogether. If you remove a tab in some cases but not in others, you make your app’s UI unstable and unpredictable. The best solution is to ensure that all tabs are enabled, but explain why a tab’s content is unavailable. For example, if the user doesn’t have any songs on an iOS device, the Songs tab in the Music app displays a screen that explains how to download songs.

  **Consider badging a tab bar icon to communicate unobtrusively.** You can display a badge on a tab bar icon to indicate that there is new information associated with that view or mode.

  **Use system-provided tab bar icons according to their documented meaning.** For more information, see [Tab Bar Icons](#//apple_ref/doc/uid/TP40006556-CH12-SW34). If you decide to create your own tab bar icons, see [Bar Button Icons](BarIcons.html#//apple_ref/doc/uid/TP40006556-CH21-SW1) for advice on how to design them.

  **If appropriate, customize the appearance of a tab bar.** For example, you can supply a custom tint for the tab bar and its icons, as long as the icons are either system-provided or custom template images. You can also supply a background image for the tab bar (note that it’s often a good idea to supply a resizable background image; to learn more about creating a resizable image, see [Creating Resizable Images](ResizableImages.html#//apple_ref/doc/uid/TP40006556-CH30-SW1)). 

  **On iPad, you might use a tab bar in a split view pane or a popover** if the tabs switch or filter the content within that view. However, it often works better to use a segmented control at the bottom edge of a popover or split view pane, because the appearance of a segmented control coordinates better with the popover or split view appearance. (For more information on using a segmented control, see [Segmented Control](Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW27).)

  **On iPad, avoid crowding the tab bar with too many tabs.** Putting too many tabs in a tab bar can make it physically difficult for people to tap the one they want. Also, with each additional tab you display, you increase the complexity of your app. In general, try to limit the number of tabs in the main view or in the right pane of a split view to about seven. In a popover or in the left pane of a split view, up to about five tabs fit well.

  **On iPad, avoid creating a More tab.** In an iPad app, a screen devoted solely to a list of additional tabs is a poor use of space.

  **On iPad, display the same tabs in each orientation to increase the visual stability of your app.** In portrait, the recommended seven tabs fit well across the width of the screen. In landscape orientation, you should center the same tabs along the width of the screen. This guidance also applies to the usage of a tab bar within a split view pane or a popover. For example, if you use a tab bar in a popover in portrait, it works well to display the same tabs in the left pane of a split view in landscape.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW34"></a>

### Tab Bar Icons

  iOS provides the standard icons described in <span class="x-name-no-link">Table 33-2</span> for use in tab bars.

  To find out which symbol names to use to specify these icons, see the documentation for [UITabBarSystemItem](../../../UIKit/Reference/UITabBarItem_Class/Reference/Reference.html#//apple_ref/c/tdef/UITabBarSystemItem) in _[UITabBarItem Class Reference](../../../UIKit/Reference/UITabBarItem_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006928)_.

<div class="tableholder">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW17"></a>
  <table class="graybox" border="0" cellspacing="0" cellpadding="5">
    <caption class="tablecaption">Table 33-2 Standard icons for use in the tabs of a tab bar</caption>
    <thead>
        <tr>
            <th scope="col" class="TableHeading_TableRow_TableCell">

  Icon

</th>
            <th scope="col" class="TableHeading_TableRow_TableCell">

  Name

</th>
            <th scope="col" class="TableHeading_TableRow_TableCell">

  Meaning

</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarBookmarks_2x.png" width="25" height="22">


</td>
            <td>

  Bookmarks

</td>
            <td>

  Show app-specific bookmarks

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarContacts_2x.png" width="25" height="22">


</td>
            <td>

  Contacts

</td>
            <td>

  Show contacts

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarDownloads_2x.png" width="25" height="22">

</td>
            <td>

  Downloads

</td>
            <td>

  Show downloads

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarFavorites_2x.png" width="25" height="22">

</td>
            <td>

  Favorites

</td>
            <td>

  Show user-determined favorites

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarFeatured_2x.png" width="25" height="22">

</td>
            <td>

  Featured

</td>
            <td>

  Show content featured by the app

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarHistory_2x.png" width="25" height="22">

</td>
            <td>

  History

</td>
            <td>

  Show history of user actions

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarMore_2x.png" width="24" height="4">

</td>
            <td>

  More

</td>
            <td>

  Show additional tab bar items

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarMostRecent_2x.png" width="25" height="22">

</td>
            <td>

  MostRecent

</td>
            <td>

  Show the most recent item

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarMostViewed_2x.png" width="25" height="22">

</td>
            <td>

  MostViewed

</td>
            <td>

  Show items most popular with all users

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarRecents_2x.png" width="25" height="22">

</td>
            <td>

  Recents

</td>
            <td>

  Show the items accessed by the user within an app-defined period

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarSearch_2x.png" width="25" height="22">


</td>
            <td>

  Search

</td>
            <td>

  Enter a search mode

</td>
        </tr>
        <tr>
            <td scope="row">
<img src="../image/UI Elements/Bars/UITabBarTopRated_2x.png" width="25" height="22">


</td>
            <td>

  TopRated

</td>
            <td>

  Show the highest-rated items, as determined by the user

</td>
        </tr>
    </tbody>
  </table>
</div>

  As with all standard buttons and icons, it’s essential to use the tab bar icons in accordance with their documented meanings. In particular, take care to base your usage of an icon on its semantic meaning, not its appearance. This will help your app’s UI make sense even if the icon associated with a specific meaning changes its appearance.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW5"></a>

### Search Bar

  A **search bar** accepts text from users, which can be used as input for a search (shown here with placeholder text).

<figure class="figure">
	<span class="caption"></span>
	<img src="../image/UI Elements/Bars/search_bar_7_2x.png" alt="image: ../Art/search_bar_7_2x.png" width="320" height="43">
</figure>

  To learn how to define a search bar in your code, see [“Search Bars”](../UIKitUICatalog/UISearchBar.html#//apple_ref/doc/uid/TP40012857-UISearchBar).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW6"></a>

#### Appearance and Behavior

  A search bar looks similar to a text field. By default, a search bar displays the search icon on the left side. When the user taps a search bar, a keyboard appears; when the user is finished typing search terms, the input is handled in an app-specific way.

  In addition, a search bar can display a few optional elements, such as:

*   **Placeholder** text. This text might state the function of the control—for example, “Search”—or remind users in what context they are searching—for example, “Google”.

*   The **Bookmarks** button. This button can provide a shortcut to information users want to easily find again. For example, the Bookmarks button in the Maps search mode gives access to bookmarked locations, recent searches, and contacts.

      The Bookmarks button is visible only when there is no user-supplied or nonplaceholder text in the search bar. When the search bar contains such text, the Clear button appears so that users can erase the text.

*   The **Clear** button. Most search bars include a Clear button that lets users to erase the contents of the search bar with one tap.

      When the search bar contains any nonplaceholder text, the Clear button is visible so users can erase the text. If there is no user-supplied or nonplaceholder text in the search bar, the Clear button is hidden.

*   The **results list** icon. This icon indicates the presence of search results. When users tap the results list icon, an app can display the results of their most recent search.

*   A descriptive title, called a **prompt**, that appears above the search bar. For example, a prompt can be a short phrase that provides introductory or app-specific context for the search bar.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW7"></a>

#### Guidelines

  Use a search bar to enable search in your app. Don’t use a text field to enable search because it doesn’t have the standard search-bar appearance that users expect.

  You can customize a search bar by tinting it or specifying a custom background appearance and by providing custom accessory images. In iOS 7, you can put a search bar in a navigation bar (for more information, see [UISearchDisplayController](../../../UIKit/Reference/UISearchDisplayController_Class/Reference/Reference.html#//apple_ref/occ/cl/UISearchDisplayController)).

  If you decide to supply a background image, it can be a good idea to supply a resizable image; to learn more about creating one, see [Creating Resizable Images](ResizableImages.html#//apple_ref/doc/uid/TP40006556-CH30-SW1).

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW8"></a>

### Scope Bar

  A **scope bar**—which is available only in conjunction with a search bar—allows users to define the scope of a search (shown here below a search bar).

<figure class="figure">
	<span class="caption"></span>
	  		<img src="../image/UI Elements/Bars/scope_bar_mail_7_2x.png" alt="image: ../Art/scope_bar_mail_7_2x.png" width="304" height="22">
</figure>

  To learn more about defining a search bar and scope bar in your code, see [“Search Bars”](../UIKitUICatalog/UISearchBar.html#//apple_ref/doc/uid/TP40012857-UISearchBar).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW9"></a>

#### Appearance and Behavior

  When a search bar is present, a scope bar can appear near it. Regardless of orientation, a scope bar displays below a search bar, unless you use a search display controller in your code (for more information on the way this works, see _[UISearchDisplayController Class Reference](../../../UIKit/Reference/UISearchDisplayController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40008225)_). When you use a search display controller, the scope bar is displayed within the search bar to the right of the search field when the device is in landscape orientation and below the search bar when the device is in portrait.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH12-SW10"></a>

#### Guidelines

  It can be useful to display a scope bar when there are clearly defined or typical categories in which users might want to search. For example, users often want to narrow their search to one field in an email message.

  You can customize a scope bar by supplying a background image. In addition, you can define different appearances for the enabled and disabled states of the scope bar buttons and the dividers between them.

</section>

</section>

</article>