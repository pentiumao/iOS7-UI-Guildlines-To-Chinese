<article class="chapter">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW1"></a>
  <a name="//apple_ref/doc/uid/TP40006556-CH13"></a>

## Content Views

    <section id="mini_toc">
	<div id="mini_toc_button">

On This Page

  </div>

*   [
	  				Activity
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW122)

*   [
	  				Activity View Controller
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW121)

*   [
	  				Collection View
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW127)

*   [
	  				Container View Controller
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW111)

*   [
	  				Image View
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW137)

*   [
	  				Map View
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW134)

*   [
	  				Page View Controller
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW141)

*   [
	  				Scroll View
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW138)

*   [
	  				Table View
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW3)

*   [
	  				Text View
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW16)

*   [
	  				Web View
	  			](#//apple_ref/doc/uid/TP40006556-CH13-SW4)
</section>

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW122"></a>

### Activity

  An **activity** represents a system-provided or custom service—accessible via an activity view controller—that can act on some specified content.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/activity_2x.png](Art/activity_2x.png)
</figure>

  To learn more about defining an activity in your code, see _[UIActivity Class Reference](../../../UIKit/Reference/UIActivity_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40011974)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW123"></a>

### Appearance and Behavior

  An **activity** is a customizable object that represents a service that an app can perform while users are in the app. When users tap the Share button, a set of activities is presented by an activity view controller (to learn how incorporate an activity view controller into your app, see [Activity View Controller](#//apple_ref/doc/uid/TP40006556-CH13-SW121)).

  Each activity is represented by an icon and a title that appears below the icon. System-provided activities can use either of two icon styles: a style that looks like an app icon or a style that looks similar to a bar button icon. A third-party activity is always represented by an icon that uses the second style. You can see both icon styles in the activity view controller shown below.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/activity_view_7_2x.png](Art/activity_view_7_2x.png)
</figure>

  Users initiate a service by tapping its activity icon in the activity view controller. In response, the activity either performs the service immediately or—if the service is complicated—it can request more information before performing the service.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW124"></a>

### Guidelines

  Use an activity to give users access to a custom service that your app can perform. Note that iOS provides several built-in services, such as Print, Twitter, Message, and AirPlay. You don’t need to create a custom activity that performs a built-in service.

  **Create a streamlined template image that represents your service.**A template image is an image that iOS uses as a mask to create the final image that users see. To create a template image that looks good in the final icon, follow these guidelines:

*   Use black or white with appropriate alpha transparency.

*   Don’t include a drop shadow.

*   Use anti-aliasing.

  An activity template image should be centered in an area that measures about 70 x 70 pixels (high resolution).

  **Craft an activity title that succinctly describes your service.** The title is displayed below the activity’s icon in the activity view controller. A short title is best, because it looks better onscreen and it’s easier to localize. If your title is too long, iOS first shrinks the text and then—if the title is still too long—truncates it. In general, it’s a good idea to avoid including your company or product name in the activity title.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW121"></a>

### Activity View Controller

  An **activity view controller** presents a transient view that lists system-provided and custom services that can act on some specified content.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/activity_view_controller_2x.png](Art/activity_view_controller_2x.png)
</figure>

  To learn more about defining an activity view controller in your code, see _[UIActivityViewController Class Reference](../../../UIKit/Reference/UIActivityViewController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40011976)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW125"></a>

### Appearance and Behavior

  An activity view controller displays a configurable list of services that the user can perform on the specified content. Users tap the Share button to reveal the contents of an activity view controller.

  An activity view controller works with a set of activities, each of which represents a specific service. To learn how to design an activity to provide a custom service, see [Activity](#//apple_ref/doc/uid/TP40006556-CH13-SW122).

  On iPhone and iPod touch, an activity view controller appears in an action sheet; on iPad, it appears in a popover.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW126"></a>

### Guidelines

  Use an activity view controller to give people a list of services they can perform on content that is specified in some way. The services can be system-provided—such as Copy, Twitter, and Print—or custom. A common way to use an activity view controller is to allow users to post content they’ve selected to a social media account.

  **Don’t create a custom button that reveals an activity view controller.** People are accustomed to accessing system-provided services when they tap the Share button. You want to take advantage of this learned behavior and avoid confusing users by providing an alternate way to do the same thing.

  **Ensure that the listed services are appropriate in the current context.** You can change the services listed in an activity view controller by specifying system-provided services to exclude and by identifying custom services to include. For example, if you wanted to prevent users from printing an image, you would exclude the Print activity from the activity view controller.

<div class="note">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW128"></a>
  <aside class="aside">

Note

You can’t change the order in which the system-provided services are listed in an activity view controller. Also, all system-provided services appear before any custom services.

  </aside>
</div>

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW127"></a>

### Collection View

  A **collection view** manages an ordered collection of items and presents them in a customizable layout.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/collection_view_7_2x.png](Art/collection_view_7_2x.png)
</figure>

  To learn more about defining a collection view in your code, see _[Collection View Programming Guide for iOS](../../../WindowsViews/Conceptual/CollectionViewPGforIOS/Introduction/Introduction.html#//apple_ref/doc/uid/TP40012334)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW129"></a>

### Appearance and Behavior

  A collection view is a customizable scrolling view that displays a set of items your app provides. People use gestures to interact with the items in a collection view and they can modify the collection by inserting, moving, and deleting items. 

  A collection view works with several other objects in your code to define the overall layout and appearance of items. Chief among these objects is the layout object—that is, a standard or custom subclass of `[UICollectionViewLayout](../../../UIKit/Reference/UICollectionViewLayout_class/Reference/Reference.html#//apple_ref/occ/cl/UICollectionViewLayout)`—which specifies the placement and visual attributes of the individual items in the collection. For convenience, UIKit provides the `[UICollectionViewFlowLayout](../../../UIKit/Reference/UICollectionViewFlowLayout_class/Reference/Reference.html#//apple_ref/occ/cl/UICollectionViewFlowLayout)` object, which defines an adjustable linear ordering that can display a grid of items.

  Within a collection view, optional supplementary views can visually distinguish subsets of items. A collection view also supports optional decoration views that can provide custom background and other appearances.

  When users insert, move, or delete items, a collection view animates the action by default. Collection views also support the addition of gesture recognizers to perform custom actions; by default, a collection view recognizes the tap and touch-and-hold gestures to handle item selection and editing, respectively.

  In iOS 7, collection views support custom animated transitions between layouts. To learn more, see _[UICollectionViewTransitionLayout Class Reference](../../../UIKit/Reference/UICollectionViewTransitionLayout_class/Reference/Reference.html#//apple_ref/doc/uid/TP40013096)_.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW130"></a>

### Guidelines

  Use a collection view to give users a way to view and manipulate a set of items that don’t need to be displayed in a list. Because a collection view doesn’t enforce a strictly linear layout, it’s particularly well suited to display items that differ in size.

  A collection view supports extensive customization, so it’s essential to avoid getting distracted by the ability to create radical new designs. You want a collection view to enhance the user’s task; you don’t want a collection view to become the focus of the user experience. The following guidelines can help you create collection views that people appreciate.

  **Don’t use a collection view when a table view is a better choice.** In some cases, it’s easier for people to view and understand information when it’s presented in a list. For example, it can be simpler and more efficient for people to view and interact with textual information when it’s in a scrolling list.

  **Make it easy for people to select an item.** If it’s hard for users to tap an item in your collection view, they’re less likely to enjoy using your app. As with all UI objects that users might want to tap, ensure that the minimum target area for each item in a collection view is 44 x 44 points. If you’re using a collection view in an iPhone app, it’s especially important to make items easy to tap.

  **Use caution if you make dynamic layout changes.** A collection view allows you to change the layout of items while users are viewing and interacting with them. If you decide to dynamically adjust a collection view’s layout, be sure that the change makes sense and is easy for users to track. Changing a collection view’s layout without an obvious motivation can give people the impression that your app is unpredictable and hard to use. And, if the current focus or context is lost during a dynamic layout change, users are likely to feel that they’re no longer in control of your app.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW111"></a>

### Container View Controller

  A **container view controller** manages and presents its set of child views—or view controllers—in a custom way. Examples of system-defined container view controllers are tab bar view controller and navigation view controller (you can learn more about these components in [Tab Bar](Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW52) and [Navigation Bar](Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW3)).

  To learn more about defining a custom container view controller in your code, see _[UIViewController Class Reference](../../../UIKit/Reference/UIViewController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006926)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW114"></a>

### Appearance and Behavior

  As you might expect, a custom container view controller doesn’t have any predefined appearance or behavior. When you subclass `UIViewController` to create a custom container view controller object, you decide how many child view controllers it contains and how they should be presented.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW115"></a>

### Guidelines

  Use a container view controller to present content through which users navigate in a custom way. 

  **Ask yourself whether a custom container view controller is really necessary.** Users are comfortable with the appearance and behavior of standard container view controllers, such as split view and tab bar view. You need to be sure that the potential advantages of your custom container view outweigh the fact that users won’t recognize it or instantly know how it works.

  **Make sure that your custom container view controller works in both orientations.** You need to design a container view controller that gives users a consistent experience in both portrait and landscape.

  **In general, avoid flashy view transitions.** When you use storyboards to design a custom view controller, it’s easy to define custom animations for the transitions between content views. But in most cases, flamboyant view transitions distract people from their purpose and often decrease the aesthetic appeal of your app.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW137"></a>

### Image View

  An **image view** displays one image or an animated series of images.

  To learn more about defining an image view in your code, see [“Image Views”](../UIKitUICatalog/UIImageView.html#//apple_ref/doc/uid/TP40012857-UIImageView).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW147"></a>

### Appearance and Behavior

  An image view doesn’t have any predefined appearance and it doesn’t enable user interaction by default. An image view examines properties of both the image and its parent view to determine whether the image should be stretched, scaled, sized to fit, or pinned to a specific location. 

  In iOS 7, an image view that contains a template image applies the current tint color to the image.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW148"></a>

### Guidelines

  **As much as possible, ensure that all images in an image view have the same size and use the same scale.** If your images have different sizes, the image view will adjust them separately; if your images use different scale factors, they may render incorrectly.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW134"></a>

### Map View

  A **map view** presents geographical data and supports most of the functionality provided by the built-in Maps app (shown below in Photos).

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/map_view_photos_7_2x.png](Art/map_view_photos_7_2x.png)
</figure>

  To learn more about defining a map view in your code, see _[Map Kit Framework Reference](../../../MapKit/Reference/MapKit_Framework_Reference/_index.html#//apple_ref/doc/uid/TP40008210)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW135"></a>

### Appearance and Behavior

  A map view displays a geographical area using standard map data, satellite imagery, or a combination of both. A map view can also display annotations—which mark single points—and overlays, which delineate paths or two-dimensional areas. 

  Users can zoom and pan a map view—unless you disallow these actions—and you can zoom and pan the map programmatically.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW136"></a>

### Guidelines

  Use a map view to give users an interactive view of a geographical area. If you’re developing a routing app, use a map view to display the user’s route (for more information about creating a routing app, see [Routing](Routing.html#//apple_ref/doc/uid/TP40006556-CH32-SW1)).

  **In general, let users interact with the map.**  People are accustomed to interacting with the built-in Maps app, and they expect to be able to interact with your map in similar ways.

  **Use the standard pin colors in a consistent way.** A map pin shows the location of a point of interest in your map. People are familiar with the pin colors in the built-in Maps app, so it’s best to avoid redefining the meaning of these colors in your app. When you use the standard pin colors, be sure to use them in the following ways:

*   Red—a destination point

*   Green—a starting point

*   Purple—a user-specified point

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW141"></a>

### Page View Controller

  A **page view controller** manages multipage content using either a scrolling or page-curl transition style (the page-curl style as it appears in iOS 7 Simulator is shown below).

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/page_view_controller_2x.png](Art/page_view_controller_2x.png)
</figure>

  To learn more about defining a page view controller in your code, see [“Page View Controllers”](../../../WindowsViews/Conceptual/ViewControllerCatalog/Chapters/PageViewControllers.html#//apple_ref/doc/uid/TP40011313-CH4).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW142"></a>

### Appearance and Behavior

  A scroll-style page view controller has no default appearance. A page-curl-style page view controller can add the appearance of the inside of a book spine between pairs of pages and—while the user is turning a page—it displays a page-curl appearance.

  A page view controller animates the transition from one page to another, according to the specified transition style. If the specified style is scroll, the current page scrolls to the next page; if the specified style is page-curl, the current page appears to turn like a page in a book or a notepad.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW143"></a>

### Guidelines

  Use a page view controller to present content that users access in a linear fashion—such as the text of a story—or content that naturally breaks into chunks—such as a calendar.

  A page view controller lets users move from one page to the next or previous page; it doesn’t give users a way to jump among nonadjoining pages. If you want to use a page view controller to present content that users might access in a nonlinear fashion—such as a dictionary or the table of contents in a book—you must implement a custom way to let users move to different areas of the content.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW138"></a>

### Scroll View

  A **scroll view** helps people see content that is larger than the scroll view’s boundaries (the image shown below is both taller and wider than the scroll view that contains it).

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/scroll_view.png](Art/scroll_view.png)
</figure>

  To learn more about defining a scroll view in your code, see [“Scroll Views”](../UIKitUICatalog/UIScrollView.html#//apple_ref/doc/uid/TP40012857-UIScrollView).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW139"></a>

### Appearance and Behavior

  When a scroll view first appears—or when users interact with it—vertical or horizontal scroll indicators flash briefly to show users that there is more content they can reveal. Other than the transient scroll indicators, a scroll view has no predefined appearance.

  A scroll view responds to the speed and direction of gestures to reveal content in a way that feels natural to people. When users drag content in a scroll view, the content follows the touch; when users flick content, the scroll view reveals the content quickly and stops scrolling when the user touches the screen or when the end of the content is reached. A scroll view can also operate in paging mode, in which each drag or flick gesture reveals one app-defined page of content. 

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW140"></a>

### Guidelines

  You can use a scroll view to give people access to large views—or to large numbers of views—in a constrained space. Because people are accustomed to using scroll views throughout iOS, make sure the scroll views in your app behave as people expect.

  **Support zoom behavior appropriately.** If it makes sense in your app, you can let users pinch or double-tap to zoom into and out of a scroll view. When you enable zoom, you should also set maximum and minimum scale values that make sense in the context of the user’s task. For example, letting users zoom in on text until one character fills the screen is unlikely to make it easier for them to read the content.

  **Consider using a page control with a paging-mode scroll view.** When you want to display content that’s been divided into pages, screenfuls, or other chunks, it’s a good idea to give users a way to tell how many chunks are available and which one they’re currently viewing. A page control displays dots that give people this information and—because page controls are used in Safari, Stocks, Weather, and other built-in apps—people already understand how to use them. 

  When you combine a page control with a paging-mode scroll view, it’s a good idea to disable the scroll indicator that’s on the same axis as the page control. People then have one unambiguous way to page through the content. For more information about using a page control in your app, see [Web View](#//apple_ref/doc/uid/TP40006556-CH13-SW4).

  **In general, display only one scroll view at a time.** People often make large swipe gestures when they scroll, so it can be difficult for them to avoid interacting with a neighboring scroll view on the same screen. If you decide to put two scroll views on one screen, consider allowing them to scroll in different directions so that one gesture is less likely to scroll both views. For example, Stocks in portrait orientation on iPhone displays stock quotes in a vertically scrolling view above company-specific information in a horizontally scrolling view.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW3"></a>

### Table View

  A **table view** presents data in a single-column list of multiple rows. 

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/plain_table_2x.png](Art/plain_table_2x.png)
</figure>

  To learn more about defining a table view in your code, see _[Table View Programming Guide for iOS](../TableView_iPhone/AboutTableViewsiPhone/AboutTableViewsiPhone.html#//apple_ref/doc/uid/TP40007451)_ and [“Table Views”](../UIKitUICatalog/UITableView.html#//apple_ref/doc/uid/TP40012857-UITableView).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW64"></a>

### Appearance and Behavior

  A table view displays data in rows that can be divided by section or separated into groups. Users flick or drag to scroll through rows or groups of rows. Users tap a table row to select it and use table view controls to add or remove rows, select multiple rows, see more information about a row item, or reveal another table view. A table row highlights briefly when the user taps a selectable item.

  If a row selection results in navigation to a new screen, the selected row highlights briefly as the new screen slides into place. When the user navigates back to the previous screen, the originally selected row again highlights briefly to remind the user of their earlier selection (it doesn’t remain highlighted).

  iOS defines two styles of table views.

  **Plain** tables display rows that can be separated into labeled sections. An optional index can appear vertically along the right edge of the view. A header can appear before the first item in a section and a footer can appear after the last item. 

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/simple_list_2x.png](Art/simple_list_2x.png)
</figure>

  **Grouped** tables display groups of rows. A grouped table view always contains at least one group of list items—one list item per row—and each group always contains at least one item. A group can be preceded by a header and followed by a footer. A grouped table view doesn’t include an index.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/group_table_singles_2x.png](Art/group_table_singles_2x.png)
</figure>

  iOS includes some **table-view elements** that can extend the functionality of table views. Unless noted otherwise, these elements are suitable for use with table views only.

<div class="tableholder">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW2"></a>
  <table class="graybox" border="0" cellspacing="0" cellpadding="5">
    <caption class="tablecaption">**Table 34-1**Table-view elements</caption>
    <thead>
        <tr>
            <th scope="col" class="TableHeading_TableRow_TableCell">

  Table-view element

</th>
            <th scope="col" class="TableHeading_TableRow_TableCell">

  Name

</th>
            <th scope="col" class="TableHeading_TableRow_TableCell">

  Description

</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td scope="row">

  ![image: ../Art/check_7_2x.png](Art/check_7_2x.png)

</td>
            <td>

  Checkmark

</td>
            <td>

  Indicates that the row is selected

</td>
        </tr>
        <tr>
            <td scope="row">

  ![image: ../Art/disclosure_indicator_7_2x.png](Art/disclosure_indicator_7_2x.png)

</td>
            <td>

  Disclosure indicator

</td>
            <td>

  Displays another table associated with the row

</td>
        </tr>
        <tr>
            <td scope="row">

  ![image: ../Art/detail_disclosure_7_2x.png](Art/detail_disclosure_7_2x.png)

</td>
            <td>

  Detail Disclosure button

</td>
            <td>

  Displays additional details about the row in a new view (for information on how to use this element outside of a table, see <!-- a logicalPath='//apple_ref/doc/uid/TP40006556-CH13-SW19' href='' data-id='//apple_ref/doc/uid/TP40006556-CH13-SW19'-->Detail Disclosure Button<!-- /a -->)

</td>
        </tr>
        <tr>
            <td scope="row">

  ![image: ../Art/UITableGrabber@2x_2x.png](Art/UITableGrabber@2x_2x.png)

</td>
            <td>

  Row reorder

</td>
            <td>

  Indicates that the row can be dragged to another location in the table

</td>
        </tr>
        <tr>
            <td scope="row">

  ![image: ../Art/row_insert_7_2x.png](Art/row_insert_7_2x.png)

</td>
            <td>

  Row insert

</td>
            <td>

  Adds a new row to the table

</td>
        </tr>
        <tr>
            <td scope="row">

  ![image: ../Art/delete_control_7_2x.png](Art/delete_control_7_2x.png)

</td>
            <td>

  Delete button control 

</td>
            <td>

  In an editing context, reveals and hides the Delete button for a row

</td>
        </tr>
        <tr>
            <td scope="row">

  ![image: ../Art/delete_button_7_2x.png](Art/delete_button_7_2x.png)

</td>
            <td>

  Delete button

</td>
            <td>

  Deletes the row

</td>
        </tr>
    </tbody>
  </table>
</div>

  In addition to the table-specific elements listed in <span class="x-name-no-link">“Table-view elements”</span>, iOS defines the refresh control, which gives users the ability to refresh a table’s contents. To learn more about using a refresh control with a table in your app, see [Refresh Control](Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW131).

  iOS defines four table-cell styles that implement the most common layouts for table rows in both plain and grouped tables. Each cell style is best suited to display a different type of information.

<div class="note">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW66"></a>
  <aside class="aside">

Note

Programmatically, these styles are applied to a table view’s cell, which is an object that tells the table how to draw its rows.

  </aside>
</div>

  **Default** (`[UITableViewCellStyleDefault](../../../UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleDefault)`). The default cell style includes an optional image in the left end of the row, followed by a left-aligned title.

  The default style is good for displaying a list of items that don’t need to be differentiated by supplementary information.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/default_cell_plain_2x.png](Art/default_cell_plain_2x.png)
</figure>

  **Subtitle** (`[UITableViewCellStyleSubtitle](../../../UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleSubtitle)`). The subtitle style includes an optional image in the left end of the row, followed by a left-aligned title on one line and a left-aligned subtitle on the line below.

  The left-alignment of the text labels makes the list easy to scan. This table-cell style works well when list items look similar, because users can use the additional information in the detail text labels to help distinguish items named in the text labels.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/subtitle_cell_plain_2x.png](Art/subtitle_cell_plain_2x.png)
</figure>

  **Value 1** (`[UITableViewCellStyleValue1](../../../UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleValue1)`). The value 1 style displays a left-aligned title on the same line with a right-aligned subtitle in a lighter font.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/value1_cell_plain_2x.png](Art/value1_cell_plain_2x.png)
</figure>

  **Value 2** (`[UITableViewCellStyleValue2](../../../UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/c/econst/UITableViewCellStyleValue2)`). The value 2 style displays a right-aligned title in a blue font, followed on the same line by a left-aligned subtitle in a black font. Images don’t fit well in this style.

  In the value 2 layout, the crisp, vertical margin between the text and the detail text helps users focus on the first words of the detail text label. 

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/value2_cell_plain_2x.png](Art/value2_cell_plain_2x.png)
</figure><div class="note">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW67"></a>
  <aside class="aside">

Note

All four standard table-cell styles also allow the addition of a table-view element, such as the checkmark or the disclosure indicator. Adding these elements decreases the width of the cell available for the title and subtitle.

  </aside>
</div>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW68"></a>

### Guidelines

  Use a table view to display large or small amounts of information cleanly and efficiently. For example, you can use a table view to:

  **Provide a list of options from which users can select.** You can use the checkmark to show users the currently selected options in the list.

  **Display hierarchical information.** The plain table style is well-suited to display a hierarchy of information. Each list item can lead to a different subset of information displayed in another list. Users follow a path through the hierarchy by selecting one item in each successive list. The disclosure indicator tells users that tapping anywhere in the row reveals the subset of information in a new list.

  **Display conceptually grouped information.** Both table view styles allow you to provide context by supplying header and footer views between sections of information.

  In iOS 6.0 and later, you can use a header-footer view—that is, an instance of `UITableViewHeaderFooterView`—to display text or a custom view in a header or footer. To learn how to use a header-footer view in your code, see _[UITableViewHeaderFooterView Class Reference](../../../UIKit/Reference/UITableViewHeaderFooterView_class/Reference/Reference.html#//apple_ref/doc/uid/TP40012241)_.

  **Display an index to facilitate lookup.** The plain style supports an index view that helps users quickly find what they need. The index consists of a column of entries—usually letters in an alphabet—that floats on the right edge of the screen.

  If you include an index, avoid using table-view elements that display on the right edge of the table—such as the disclosure indicator—because these elements interfere with the index.

  Follow these guidelines when you use table views:

  **Always provide feedback when users select a list item.** Users expect a table row to highlight briefly when they tap a selectable item in it. After tapping, users expect a new view to appear or the row to display a checkmark to indicate that the item has been selected or enabled. 

  **If table content is extensive or complex, avoid waiting until all the data is available before displaying anything.** Instead, fill the onscreen rows with textual data immediately and display more complex data—such as images—as they become available. This technique gives users useful information right away and increases the perceived responsiveness of your app. 

  **Consider displaying “stale” data while waiting for new data to arrive.** Although this technique isn’t recommended for apps that handle frequently changing data, it can help more static apps give users something useful right away. Before you decide to do this, gauge how often the data changes and how much users depend on seeing fresh data quickly.

  **If the data is slow-loading or complex, tell users that processing is continuing.** If a table contains only complex data, it might be difficult to display anything useful right away. In these rare cases, it's important to avoid displaying empty rows, because this can imply that your app has stalled. Instead, the table should display a spinning activity indicator along with an informative label, such as “Loading...”, centered in the screen. Doing this reassures users that processing is continuing.

  **If appropriate, use a custom title for the Delete button.** If it helps users to better understand the way your app works, you can create a title to replace the system-provided Delete title.

  **As much as possible, use succinct text labels to avoid truncation.** Truncated words and phrases can be difficult for users to scan and understand. Text truncation is automatic in all table-cell styles, but it can present more or less of a problem, depending on which cell style you use and on where truncation occurs.

  **If you want to lay out your table rows in a nonstandard way**, it’s better to create a custom table-cell style than to significantly alter a standard one. To learn how to create your own cells, see [“Customizing Cells”](../TableView_iPhone/TableViewCells/TableViewCells.html#//apple_ref/doc/uid/TP40007451-CH7-SW18) in _[Table View Programming Guide for iOS](../TableView_iPhone/AboutTableViewsiPhone/AboutTableViewsiPhone.html#//apple_ref/doc/uid/TP40007451)_.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW16"></a>

### Text View

  A **text view** accepts and displays multiple lines of text.

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/text_view_2x.png](Art/text_view_2x.png)
</figure>

  To learn more about defining a text view in your code, see [“Text Views”](../UIKitUICatalog/UITextView.html#//apple_ref/doc/uid/TP40012857-UITextView).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW69"></a>

### Appearance and Behavior

  A text view is a rectangle of any height. A text view supports scrolling when the content is too large to fit inside its bounds. 

  If the text view supports user editing, a keyboard appears when the user taps inside the text view. The keyboard’s input method and layout are determined by the user’s language settings.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW70"></a>

### Guidelines

  You have control over the font, color, and alignment of the text in a text view. The default font is the system font and the default color is black. The default for the alignment property is left (you can change it to center or right). 

  **Always make sure the text is easy to read.** Although you can use attributed strings to combine multiple fonts, colors, and alignments in creative ways, it’s essential to maintain the readability of the text. It’s a good idea to support Dynamic Type and use the `[UIFont](../../../UIKit/Reference/UIFont_Class/Reference/Reference.html#//apple_ref/occ/cl/UIFont)` method `preferredFontForTextStyle` to get the text for display in a text view.

  **Specify different keyboard types to accommodate different types of content you expect users to enter.** For example, you might want to make it easy for users to enter a URL, a PIN, or a phone number. Note, however, that you have no control over the keyboard’s input method and layout, which are determined by the user’s language settings. iOS provides several different keyboard types, each designed to facilitate a different type of input. To learn about the keyboard types that are available, see the documentation for `[UIKeyboardType](../../../UIKit/Reference/UITextInputTraits_Protocol/Reference/UITextInputTraits.html#//apple_ref/c/tdef/UIKeyboardType)`. To learn more about managing the keyboard in your app, read <!-- a href="" target="_self" -->“Managing the Keyboard”<!-- /a --> in _[iOS App Programming Guide](../../../iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072)_.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW4"></a>

### Web View

  A **web view** is a region that can display rich HTML content (shown here between the navigation bar and toolbar in Mail on iPhone).

<figure class="figure">

	  		<span class="caption"></span>
	  		![image: ../Art/web_view_2x.png](Art/web_view_2x.png)
</figure>

  To learn more about defining a web view in your code, see [“Web Views”](../UIKitUICatalog/UIWebView.html#//apple_ref/doc/uid/TP40012857-UIWebView).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW71"></a>

### Appearance and Behavior

  In addition to displaying web content, a web view performs some automatic processing on web content, such as converting a phone number to a phone link.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH13-SW72"></a>

### Guidelines

  If you have a webpage or web app, you might decide to use a web view to implement a simple iOS app that provides a wrapper for your webpage or web app. If you plan to use a web view to access web content that you control, be sure to read _[Safari Web Content Guide](../../../AppleApplications/Reference/SafariWebContent/Introduction/Introduction.html#//apple_ref/doc/uid/TP40002051)_.

  **Avoid using a web view to create an app that looks and behaves like a mini web browser.** People expect to use Safari on iOS to browse web content, so replicating this broad functionality within your app is not recommended.

</section>

</section>

 	<section id="next_previous" class="">

[Bars](Bars.html#//apple_ref/doc/uid/TP40006556-CH12-SW1)

[Controls](Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW1)

Copyright © 2013 Apple Inc. All rights reserved. Apple Confidential Information. 
[Terms of Use](http://www.apple.com/legal/terms/site.html)   |  [Privacy Policy](http://www.apple.com/legal/privacy/)  |   [Updated: 2013-06-13](RevisionHistory.html#//apple_ref/doc/uid/TP40006556-CH99-SW1)

  </section>
</article>