<article class="chapter">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW1"></a>
  <a name="//apple_ref/doc/uid/TP40006556-CH15"></a>

## Controls

<section id="mini_toc">
	<div id="mini_toc_button">

On This Page

  </div>

*   [
	  				Activity Indicator
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW2)

*   [
	  				Date Picker
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW3)

*   [
	  				Contact Add Button
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW144)

*   [
	  				Detail Disclosure Button
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW4)

*   [
	  				Info Button
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW5)

*   [
	  				Label
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW22)

*   [
	  				Network Activity Indicator
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW44)

*   [
	  				Page Control
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW6)

*   [
	  				Picker
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW23)

*   [
	  				Progress View
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW7)

*   [
	  				Refresh Control
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW131)

*   [
	  				Rounded Rectangle Button
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW8)

*   [
	  				Segmented Control
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW27)

*   [
	  				Slider
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW57)

*   [
	  				Stepper
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW116)

*   [
	  				Switch
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW14)

*   [
	  				System Button
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW10)

*   [
	  				Text Field
	  			](#//apple_ref/doc/uid/TP40006556-CH15-SW9)
</section>

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW2"></a>

### Activity Indicator

  An **activity indicator** shows that a task or process is progressing.

<figure class="figure">
<span class="caption"></span>
<img src="../image/UI Elements/Controls/activity_indicator_2x.png" width="20" height="20">
</figure>

  To learn how to define an activity indicator in your code, see _[UIActivityIndicatorView Class Reference](../../../UIKit/Reference/UIActivityIndicatorView_Class/Reference/UIActivityIndicatorView.html#//apple_ref/doc/uid/TP40006830)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW79"></a>

#### Appearance and Behavior

  An activity indicator spins while a task is progressing and disappears when the task completes. Users don’t interact with an activity indicator. 

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW80"></a>

#### Guidelines

  Use an activity indicator in a toolbar or a main view to show that processing is occurring, without suggesting when it will finish. 

  **Don’t display a stationary activity indicator,** because users associate this with a stalled process. 

  **Use an activity indicator when it’s more important to reassure users that their task or process has not stalled** than it is to suggest when processing will finish.

  **If appropriate, customize the size and color of an activity indicator** to coordinate with the background of the view in which it appears.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW3"></a>

### Date Picker

  A **date picker** displays components of date and time, such as hours, minutes, days, and years. 

<figure class="figure">
<span class="caption"></span>
<img src="../image/UI Elements/Controls/date_picker_7_2x.png" alt="image: ../Art/date_picker_7_2x.png" width="320" height="176">
</figure>

  To learn how to define a date picker in your code, see [“Date Pickers”](../UIKitUICatalog/UIDatePicker.html#//apple_ref/doc/uid/TP40012857-UIDatePicker).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW81"></a>

#### Appearance and Behavior

  A date picker can have up to four independent wheels, each of which displays values in a single category, such as month or hour. Users flick or drag to spin each wheel until it displays the desired value horizontally in the middle of the picker. The final value comprises the values displayed in each wheel.

  The overall size of a date picker is fixed at the same size as the iPhone keyboard.

  A date picker has four modes, each of which displays a different number of wheels that contain a set of different values.

*   **Date and time.** The date and time mode—which is the default mode—displays wheels for the calendar date, hour, and minute values, plus an optional wheel for the AM/PM designation.

*   **Time.** The time mode displays wheels for the hour and minute values, plus an optional wheel for the AM/PM designation.

*   **Date.** The date mode displays wheels for the month, day, and year values.

*   **Countdown timer.** The countdown timer mode displays wheels for the hour and minute. You can specify the total duration of a countdown, up to a maximum of 23 hours and 59 minutes.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW82"></a>

#### Guidelines

  Use a date picker to let users pick—instead of type—a date or time value that consists of multiple parts, such as the day, month, and year. A date picker is easy to use because the values in each part have a relatively small range and users already know what the values are.

  **As much as possible, display a date picker inline with the content.** It’s best when users can avoid navigating to a different view to use a date picker.

  **If it makes sense in your app, change the interval in the minutes wheel.** By default, a minutes wheel displays 60 values (0 to 59). If you need to display a coarser granularity of choices, you can set a minutes wheel to display a larger minute interval, as long as the interval divides evenly into 60. For example, you might want to display the quarter-hour intervals 0, 15, 30, and 45.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW144"></a>

### Contact Add Button

  A **Contact Add button** lets the user add an existing contact to a text field or other text-based view.

<figure class="figure">
<img src="../image/UI Elements/Controls/contact_add_7_2x.png" alt="image: ../Art/contact_add_7_2x.png" width="36" height="36">
</figure>

  To learn how to define a Contact Add button in your code, see [“Buttons”](../UIKitUICatalog/UIButton.html#//apple_ref/doc/uid/TP40012857-UIButton).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW145"></a>

#### Appearance and Behavior

  When users tap a Contact Add button, a list of their contacts is revealed. When users choose a contact from the list, the list closes and the contact is added to the view that contains the Contact Add button.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW146"></a>

#### Guidelines

  Use a Contact Add button to give users an easy way to access a contact without using the keyboard. For example, users can tap the Contact Add button in the To field of the Mail compose view instead of typing a recipient’s name.

  Because the Contact Add button functions as an alternative to typing contact information, it’s not appropriate to use the button in a view that doesn’t accept keyboard input. 

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW4"></a>

### Detail Disclosure Button

  A **Detail Disclosure button** reveals additional details or functionality related to an item (shown here inside a map annotation view).

<figure class="figure">
<img src="../image/UI Elements/Controls/detail_disclosure_7_2x.png" alt="image: ../Art/detail_disclosure_7_2x.png" width="22" height="22">
</figure>

  To learn how to define a Detail Disclosure button in your code, see _[UITableViewCell Class Reference](../../../UIKit/Reference/UITableViewCell_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006938)_ and [“Buttons”](../UIKitUICatalog/UIButton.html#//apple_ref/doc/uid/TP40012857-UIButton).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW83"></a>

#### Appearance and Behavior

  Users tap a Detail Disclosure button to reveal additional information or functionality related to a specific item. The additional details or functionality are revealed in a separate view. 

  When a Detail Disclosure button appears in a table row, tapping elsewhere in the row doesn’t activate the Detail Disclosure button; instead, it selects the row item or results in app-defined behavior.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW84"></a>

#### Guidelines

  Typically, you use a Detail Disclosure button in a table view to give users a way to see more details or functionality related to a list item. However, you can also use this element in other types of views to provide a way to reveal more information or functionality related to an item in that view.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW5"></a>

### Info Button

  An **Info button** reveals configuration details about an app, sometimes on the back of the current view. 

<figure class="figure">
<img src="../image/UI Elements/Controls/info_button_2x.png" alt="image: ../Art/info_button.jpg" width="22" height="22">
</figure>

  To learn more about defining an Info button in your code, see [“Buttons”](../UIKitUICatalog/UIButton.html#//apple_ref/doc/uid/TP40012857-UIButton).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW85"></a>

#### Appearance and Behavior

  iOS includes two styles of Info button: a dark-colored button that looks good on light content and a light-colored button that looks good on dark content.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW86"></a>

#### Guidelines

  Use an Info button to reveal configuration details or options about an app. You can use the style of Info button that coordinates best with the UI of your app.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW22"></a>

### Label

  A **label** displays static text.

<figure class="figure">
<img src="../image/UI Elements/Controls/labels_7_2x.png" width="257" height="70">
</figure>

  To learn more about defining labels in your code, see _[UILabel Class Reference](../../../UIKit/Reference/UILabel_Class/Reference/UILabel.html#//apple_ref/doc/uid/TP40006797)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW87"></a>

#### Appearance and Behavior

  A label displays any amount of static text. Users don’t interact with labels except—potentially—to copy the text.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW88"></a>

#### Guidelines

  Use a label to name or describe parts of your UI or to provide short messages to the user. A label is best suited to display a relatively small amount of text.

  **Take care to make your labels legible.** It’s best to support Dynamic Type and use the [UIFont](../../../UIKit/Reference/UIFont_Class/Reference/Reference.html#//apple_ref/occ/cl/UIFont) method `preferredFontForTextStyle` to get the text for display in a label. If you choose to use custom fonts, don’t sacrifice clarity for fancy lettering or showy colors.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW44"></a>

### Network Activity Indicator

  A **network activity indicator** appears in the status bar and shows that network activity is occurring.

<figure class="figure">
<img src="../image/UI Elements/Controls/network_activity_indicator_7_2x.png" alt="image: ../Art/network_activity_indicator_7_2x.png" width="17" height="17">
</figure>

  In your code,  use the `UIApplication` method [networkActivityIndicatorVisible](../../../UIKit/Reference/UIApplication_Class/Reference/Reference.html#//apple_ref/occ/instm/UIApplication/isNetworkActivityIndicatorVisible) to control the indicator’s visibility.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW89"></a>

#### Appearance and Behavior

  The network activity indicator spins in the status bar while network activity proceeds and it disappears when network activity stops. Users don’t interact with the network activity indicator.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW90"></a>

#### Guidelines

  Display the network activity indicator to provide feedback when your app accesses the network for more than a couple of seconds. If the operation finishes sooner than that, you don’t have to show the network activity indicator, because the indicator would be likely to disappear before users notice its presence.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW6"></a>

### Page Control

  A **page control** indicates how many views are open and which one is currently visible (shown here in Weather). 

<figure class="figure">
<img src="../image/UI Elements/Controls/page_control_weather_7_2x.png" alt="image: ../Art/page_control_weather_7_2x.png" width="62" height="22">
</figure>

  To learn more about defining a page control in your code, see [“Page Controls”](../UIKitUICatalog/UIPageControl.html#//apple_ref/doc/uid/TP40012857-UIPageControl).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW91"></a>

#### Appearance and Behavior

  A page control displays an indicator dot for each currently open peer view in an app. From left to right, the dots represent the order in which the views were opened (the leftmost dot represents the first view). By default, the dot that represents the currently visible view is opaque and the dots that represent all other views are translucent. Users tap to the left or the right of the current dot to see the previous or next open view.

  The dots of a page control don’t shrink or squeeze together as more appear. A screen in portrait orientation can accommodate approximately 20 dots; if you try to display more dots than will fit in the screen, they will be clipped. 

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW92"></a>

#### Guidelines

  Use a page control when each view in your app is a peer of every other view. Don’t use a page control if your app displays information in a hierarchy of views, because a page control doesn’t help users retrace their steps through a specific path.

  **Vertically center a page control between the bottom edge of an open view and the bottom edge of the screen,** where it’s always visible without getting in users’ way. Avoid trying to display too many dots for the current screen orientation.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW23"></a>

### Picker

  A **picker** displays a set of values from which a user picks one.

<figure class="figure">
<img src="../image/UI Elements/Controls/picker_7_2x.png" alt="image: ../Art/picker_7_2x.png" width="320" height="215">
</figure>

  To learn more about defining a picker in your code, see _[UIPickerView Class Reference](../../../UIKit/Reference/UIPickerView_Class/Reference/UIPickerView.html#//apple_ref/doc/uid/TP40006842)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW93"></a>

#### Appearance and Behavior

  A picker is a generic version of the date picker. As with a date picker, users spin the wheel (or wheels) of a picker until the value they want appears. The overall size of a picker, including its background, is fixed at the same size as the keyboard on iPhone. (For more information about the date picker, see <!-- a logicalPath='//apple_ref/doc/uid/TP40006556-CH13-SW43' href='' data-id='//apple_ref/doc/uid/TP40006556-CH13-SW43'-->Date Picker<!-- /a -->.)

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW94"></a>

#### Guidelines

  Use a picker to make it easy for people to choose from a set of values. It’s often best to use a picker when people are familiar with the entire set of values. This is because many of the values are hidden when the wheel is stationary. If you need to provide a large set of choices that aren’t well known to your users, a picker might not be the appropriate control.

  **As much as possible, display a picker inline with the content.** It’s best when users can avoid navigating to a different view to use a picker.

  **Consider using a table view, instead of a picker, if you need to display a very large number of values.** This is because the greater height of a table view makes scrolling faster.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW7"></a>

### Progress View

  A **progress view** shows the progress of a task or process that has a known duration (shown here in the Mail toolbar). 

<figure class="figure">
<img src="../image/UI Elements/Controls/progress_view_7_2x.png" alt="image: ../Art/progress_view_7_2x.png" width="320" height="38">
</figure>

  To learn more about defining a progress view in your code, see _[UIProgressView Class Reference](../../../UIKit/Reference/UIProgressView_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006782)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW95"></a>

#### Appearance and Behavior

  iOS provides two styles of progress view. The appearance of each style is very similar, except for height.

*   The **default** style has a weight that makes it suitable for use in an app’s main content area.

*   The **bar** style is thinner than the default style, which makes it well-suited for use in a toolbar.

  As the task or process proceeds, the track of the progress view is filled from left to right. At any given time, the proportion of filled to unfilled area in the progress view gives people an indication of how soon the task or process will finish. Users don’t interact with a progress view.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW96"></a>

#### Guidelines

  Use a progress view to give feedback on a task that has a well-defined duration, especially when it’s important to show approximately how long the task will take. When you display a progress view, you tell the user that their task is being performed and you give them enough information to decide if they want to wait until the task is complete or cancel it.

  **If appropriate, customize the appearance of a progress view** to coordinate with the style of your app. You can specify a custom tint or image for both the track and the fill of a progress view. 

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW131"></a>

### Refresh Control

  A **refresh control** performs a user-initiated content refresh—typically in a table (shown here above the mailbox list).

<figure class="figure">
<img src="../image/UI Elements/Controls/refresh_control_7_2x.png" alt="image: ../Art/refresh_control_7_2x.png" width="320" height="205">
</figure>

  To learn more about defining a refresh control in your code, see _[UIRefreshControl Class Reference](../../../UIKit/Reference/UIRefreshControl_class/Reference/Reference.html#//apple_ref/doc/uid/TP40012250)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW132"></a>

#### Appearance and Behavior

  By default, a refresh control is hidden until the user initiates a refresh action by dragging down from the top edge of a table. The refresh control looks similar to an activity indicator.

  A refresh control can also display a title and use a custom tint.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW133"></a>

#### Guidelines

  Use a refresh control to give users a consistent way to tell a table or other view to update its contents immediately, without waiting for the next automatic update. The following guidelines can help you ensure that your refresh control enhances the user’s experience.

  **Don’t stop performing automatic content updates just because you provide a refresh control.** Even though users appreciate being able to request that an update be performed _now_, they still appreciate content that refreshes itself automatically. And if you rely on users to initiate all refreshes, users who are unaware of the refresh control are likely to wonder why your app displays stale data. In general, you want to give users the option to refresh contents immediately; you don’t want to make users responsible for every update.

  **Supply a short title only if it adds value.** In particular, don’t use the title to describe how to use the refresh control.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW8"></a>

### Rounded Rectangle Button

  The rounded rectangle button has been deprecated in iOS 7. Instead, use the system button—that is, a [UIButton](../../../UIKit/Reference/UIButton_Class/UIButton/UIButton.html#//apple_ref/occ/cl/UIButton) of type `UIButtonTypeSystem`. For guidelines, see [System Button](#//apple_ref/doc/uid/TP40006556-CH15-SW10).

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW27"></a>

### Segmented Control

  A **segmented control** is a linear set of segments, each of which functions as a button that can display a different view.

<figure class="figure">
<img src="../image/UI Elements/Controls/segmented_control_2x.png" alt="image: ../Art/segmented_control.jpg" width="320" height="48">
</figure>

  To learn more about defining a segmented control in your code, see [“Segmented Controls”](../UIKitUICatalog/UISegmentedControl.html#//apple_ref/doc/uid/TP40012857-UISegmentedControl).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW103"></a>

#### Appearance and Behavior

  The length of a segmented control is determined by the number of its segments; the height of a segmented control is fixed. The width of each segment is proportional, based on the total number of segments. When users tap a segment, the segment displays a selected appearance.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW104"></a>

#### Guidelines

  Use a segmented control to offer closely related, but mutually exclusive choices. 

  **Make sure that each segment is easy to tap.** To maintain a comfortable hit region of 44 x 44 points for each segment, you need to limit the number of segments. On iPhone, a segmented control should have five or fewer segments. 

  **As much as possible, maintain consistency in the size of each segment’s contents.** Because all segments in a segmented control have equal width, it doesn’t look good if the content fills some segments, but not others.

  **Avoid mixing text and images in a single segmented control.** A segmented control can contain text or images. An individual segment can contain either text or an image, but not both. In general, it’s best to avoid putting text in some segments and images in other segments of a single segmented control.

  **If appropriate, customize the appearance of a segmented control.** For example, you can supply a custom background tint or image. If you supply a background image, you can also specify a different background image to use for a segment’s selected appearance and a custom appearance for the dividers between segments. (In some cases, it can be a good idea to supply a resizable background image; to learn more about creating one, see [Creating Resizable Images](ResizableImages.html#//apple_ref/doc/uid/TP40006556-CH30-SW1).)

  If you customize the background appearance of a segmented control, you should make sure that the automatic centering of the control’s text or image content still looks good. If necessary, you can use the bar metrics APIs to adjust the positioning of the content inside the segmented control (to learn more about specifying bar metrics, see the appearance-customization APIs described in [UISegmentedControl](../../../UIKit/Reference/UISegmentedControl_Class/Reference/UISegmentedControl.html#//apple_ref/doc/uid/TP40006807-CH3)).

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW57"></a>

### Slider

  A **slider** allows users to make adjustments to a value or process throughout a range of allowed values (shown here with custom images on the left and the right). 

<figure class="figure">
<img src="../image/UI Elements/Controls/slider_2x.png" alt="image: ../Art/slider.png" width="290" height="35">
</figure>

  To learn more about defining a slider in your code, see [“Sliders”](../UIKitUICatalog/UISlider.html#//apple_ref/doc/uid/TP40012857-UISlider).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW105"></a>

#### Appearance and Behavior

  A slider consists of a horizontal track and a thumb (a circular control that the user can slide) and can include optional images that convey the meaning of the right and left values. When people drag the thumb along the slider, the value or process is updated continuously and is displayed in the track. 

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW106"></a>

#### Guidelines

  Use a slider to give users fine-grained control over values they can choose or the operation of the current process.

  **If appropriate, customize the appearance of a slider.** For example, you can do any of the following:

*   Set the width of a slider to fit in with the UI of your app.

*   Define the appearance of the thumb, so that users can see at a glance whether the slider is active.

*   Supply images to appear at both ends of the slider to help users understand what the slider does.

      Typically, these custom images correspond to the minimum and maximum values of the value range that the slider controls. A slider that controls image size, for example, could display a very small image at the minimum end and a very large image at the maximum end.

*   Define a different appearance for the track, depending on which side of the thumb it is on and which state the control is in.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW116"></a>

### Stepper

  A **stepper** increases or decreases a value by a constant amount.

<figure class="figure">
<img src="../image/UI Elements/Controls/stepper_2x.png" alt="image: ../Art/stepper.jpg" width="94" height="29">
</figure>

  To learn more about defining a stepper in your code, see [“Steppers”](../UIKitUICatalog/UIStepper.html#//apple_ref/doc/uid/TP40012857-UIStepper).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW117"></a>

#### Appearance and Behavior

  A stepper is a two-segment control in which one segment displays a plus symbol and the other segment displays a minus symbol. Users tap a segment to increase or decrease a value. A stepper doesn’t display the value that the user changes.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW118"></a>

#### Guidelines

  In general, use a stepper when users might need to make small adjustments to a value. For example, it makes sense to use a stepper to set the number of copies in the Printer Options action sheet, because users rarely change this value by very much. On the other hand, it wouldn’t make sense to use a stepper to help users choose a page range, because those values can vary a lot.

  **Make it obvious which value the stepper affects.** A stepper doesn’t display any values, so you need to make sure that users know which value they’re changing when they use a stepper.

  **If appropriate, customize the appearance of a stepper** to coordinate with the style of your app. You can specify a custom tint for the control or you can supply custom images for the background and divider and for the increment and decrement symbols.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW14"></a>

### Switch

  A **switch** presents two mutually exclusive choices or states (used in table views only).

<figure class="figure">
<img src="../image/UI Elements/Controls/switch_on_2x.png" alt="image: ../Art/switch_on.jpg" width="57" height="36">
</figure><figure class="figure">
<img src="../image/UI Elements/Controls/switch_off_2x.png" alt="image: ../Art/switch_off.jpg" width="54" height="34">
</figure>

  To learn more about defining a switch in your code, see [“Switches”](../UIKitUICatalog/UISwitch.html#//apple_ref/doc/uid/TP40012857-UISwitch).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW107"></a>

#### Appearance and Behavior

  A switch displays the value that is currently in effect; users slide the control to select the other value. Users can also tap the control to switch between choices.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW108"></a>

#### Guidelines

  Use a switch in a table row to give users two simple, diametrically opposed choices that determine the state of something, such as yes/no or on/off.

  You can use a switch control to change the state of other UI elements in the view. Depending on the choice users make, new list items might appear or disappear, or list items might become active or inactive.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW10"></a>

### System Button

  A system button performs an app-specific action.

<figure class="figure">
<img src="../image/UI Elements/Controls/system_button_2x.png" alt="image: ../Art/system_button_2x.png" width="43" height="11">
</figure>

  If you need to display a button that includes a bezel, use a button of type `UIButtonTypeCustom` and supply a custom background image.

  To learn more about defining a system button in your code, see [“Buttons”](../UIKitUICatalog/UIButton.html#//apple_ref/doc/uid/TP40012857-UIButton).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW97"></a>

#### Appearance and Behavior

  iOS 7 system buttons don’t include a bezel or a background appearance. A system button can contain an icon or a text title, and it can specify a tint color or receive its parent’s color.

<div class="note">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW13"></a>
  <aside class="aside">

Note

In iOS 7, `UIButtonTypeRoundedRect` has been redefined as `UIButtonTypeSystem`. An app that uses a rounded rectangle button in iOS 6 automatically gets the system button appearance when it links against iOS 7.

  </aside>
</div>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW98"></a>

#### Guidelines

  Use a system button to initiate an action. When you supply a title for a system button, follow this approach:

*   Use title-style capitalization—that is, capitalize every word except articles, coordinating conjunctions, and prepositions of four or fewer letters

*   Avoid creating a title that is too long. Overly long text gets truncated, which can make it difficult for users to understand it.

  You can specify the title or image to display in a system button, and you can tell the button to highlight when it’s tapped and specify how the title or image should look when the button highlights. You can also supply a tint for the button’s content.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW9"></a>

### Text Field

  A **text field** accepts a single line of user input (shown here with a purpose description and placeholder text). 

<figure class="figure">
<img src="../image/UI Elements/Controls/text_field_2x.png" alt="image: ../Art/text_field_2x.png" width="288" height="72">
</figure>

  To learn more about defining a text field and customizing it to display images and buttons, see [“Text Fields”](../UIKitUICatalog/UITextField.html#//apple_ref/doc/uid/TP40012857-UITextField).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW109"></a>

#### Appearance and Behavior

  A text field is a fixed-height field with rounded corners. When users tap a text field a keyboard appears; when users dismiss the keyboard, the text field handles the input in an app-specific way.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH15-SW110"></a>

#### Guidelines

  Use a text field to get a small amount of information from the user. Before you decide to use a text field, consider whether there are other controls that might make inputting the information easier, such as a picker or a list. 

  **Customize a text field if it helps users understand how they should use it.** For example, you can display custom images in the left or right sides of the text field, or add a system-provided button, such as the Bookmarks button. In general, you should use the left end of a text field to indicate its purpose and the right end to indicate the presence of additional features, such as bookmarks.

  **Display the Clear button in the right end of a text field when appropriate.** When this element is present, tapping it clears the contents of the text field, regardless of any other image you might display over it.

  **Display a hint in the text field if it helps users understand its purpose,** such as “Name” or “Address.” A text field can display such placeholder text when there is no other text in the field.

  **Specify a keyboard type that’s appropriate for the type of content you expect users to enter.** For example, you might want to make it easy for users to enter a URL, a PIN, or a phone number. iOS provides several different keyboard types, each designed to facilitate a different type of input. To learn about the keyboard types that are available, see the documentation for [UIKeyboardType](../../../UIKit/Reference/UITextInputTraits_Protocol/Reference/UITextInputTraits.html#//apple_ref/c/tdef/UIKeyboardType). To learn more about managing the keyboard in your app, read <!-- a href="" target="_self" -->“Managing the Keyboard”<!-- /a --> in _[iOS App Programming Guide](../../../iPhone/Conceptual/iPhoneOSProgrammingGuide/Introduction/Introduction.html#//apple_ref/doc/uid/TP40007072)_. Note that you have no control over the keyboard’s input method and layout, because these attributes are determined by the user’s language settings.

</section>

</section>

</article>