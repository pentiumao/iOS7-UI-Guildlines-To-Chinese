<article class="chapter">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW1"></a>
  <a name="//apple_ref/doc/uid/TP40006556-CH14"></a>

## Temporary Views

   <section id="mini_toc">
	<div id="mini_toc_button">

On This Page

  </div>

*   [
	  				Alert
	  			](#//apple_ref/doc/uid/TP40006556-CH14-SW2)

*   [
	  				Action Sheet
	  			](#//apple_ref/doc/uid/TP40006556-CH14-SW36)

*   [
	  				Modal View
	  			](#//apple_ref/doc/uid/TP40006556-CH14-SW3)
</section>

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW2"></a>

### Alert

  An **alert** gives people important information that affects their use of the app or the device.

<figure class="figure">
<img src="../image/UI Elements/Temporary Views/alert_2x.png" alt="image: ../Art/alert_2x.png" width="320" height="309">
</figure>

  To learn about using an alert in your code, see _[UIAlertView Class Reference](../../../UIKit/Reference/UIAlertView_Class/UIAlertView/UIAlertView.html#//apple_ref/doc/uid/TP40006802)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW73"></a>

#### Appearance and Behavior

  An alert pops up in the middle of the app screen and floats above its views. The unattached appearance of an alert emphasizes the fact that its arrival is due to some change in the app or the device, not necessarily as the result of the user’s most recent action. Users must dismiss the alert before they can continue using the currently running app.

  An alert always contains at least one button, which users tap to dismiss the alert. By default, an alert displays a title and might also display a message that provides additional information. An alert can contain one or two text fields, one of which can be a secure text-input field. The background appearance of an alert is system-defined and can’t be changed.

<div class="note">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW55"></a>
  <aside class="aside">

Note

A local or push notification might use an alert to communicate with users, although this is rare. To learn more about local and push notifications, see <!-- a logicalPath='' href='' data-id=''-->Notification Center<!-- /a -->.

  </aside>
</div>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW74"></a>

#### Guidelines

  The infrequency with which alerts appear helps users take them seriously. Be sure to minimize the number of alerts your app displays and ensure that each one offers critical information and useful choices. 

  **Avoid creating unnecessary alerts.** In general, alerts are unnecessary if they:

*   Merely increase the visibility of some information, especially information that’s related to the standard functioning of your app.

      Instead, design an eye-catching way to display the information that harmonizes with your app’s style.

*   Update users on tasks that are progressing normally.

      Instead, consider using a progress view or an activity indicator to provide progress-related feedback to users (these methods of feedback are described in [Progress View](Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW7) and [Activity Indicator](Controls.html#//apple_ref/doc/uid/TP40006556-CH15-SW2)).

*   Ask for confirmation of user-initiated actions.

      To get confirmation for an action the user initiated—even a potentially risky action such as deleting a contact—you should use an action sheet (described in [Action Sheet](#//apple_ref/doc/uid/TP40006556-CH14-SW36)).

*   Inform users of errors or problems about which they can do nothing.

      Although it might be necessary to use an alert to tell users about a critical problem they can’t fix, it’s better to integrate such information into the UI, if possible. For example, instead of telling users every time a server connection fails, display the time of the last successful connection.

  You can specify the text of the required title and optional message, the number of buttons, and the button contents in an alert. You can’t customize the width or the background appearance of the alert view itself, or the alignment of the text (it’s center-aligned). 

  As you read the alert-text design guidelines, it’s useful to know the following definitions:

*   **Title-style capitalization** means that every word is capitalized, except articles, coordinating conjunctions, and prepositions of four or fewer letters when they aren’t the first word.

*   **Sentence-style capitalization** means that the first word is capitalized, and the rest of the words are lowercase unless they are proper nouns or proper adjectives.

  **Succinctly describe the situation and explain what people can do about it.** Ideally, the text you write gives people enough context to understand why the alert has appeared and to decide which button to tap.

  **Keep the title short enough to display on a single line, if possible.** A long alert title is difficult for people to read quickly, and it might get truncated or force the alert message to scroll.

<figure class="figure">
<img src="../image/UI Elements/Temporary Views/alert_title_only_2x.png" alt="image: ../Art/alert_title_only_2x.png" width="320" height="188">
</figure>

  **Avoid single-word titles that don’t provide any useful information**, such as “Error” or “Warning.”

  **When possible, use a sentence fragment.** A short, informative statement is often easier to understand than a complete sentence.

  **Don’t hesitate to be negative.** People understand that most alerts tell them about problems or warn them about dangerous situations. It’s better to be negative and direct than it is to be positive but oblique.

  **As much as possible, avoid using “you,” “your,” “me,” and “my”.** Sometimes, text that identifies people directly can be ambiguous and can even be interpreted as an insult.

  **Use capitalization and punctuation appropriately.** Specifically:

*   Use title-style capitalization and no ending punctuation when the title is a sentence fragment or it consists of a single sentence that is not a question.

*   If the title consists of a single sentence that is a question, use sentence-style capitalization and an ending question mark. In general, consider using a question for an alert title if it allows you to avoid adding a message.

*   If the title consists of two or more sentences, use sentence-style capitalization and appropriate ending punctuation for each sentence. A two-sentence alert title should seldom be necessary, although you might consider it if it allows you to avoid adding a message.

  **If you provide an optional alert message, create a short, complete sentence.** Use sentence-style capitalization and appropriate ending punctuation.

<figure class="figure">
<img src="../image/UI Elements/Temporary Views/alert_title_with_msg_2x.png" alt="image: ../Art/alert_title_with_msg_2x.png" width="320" height="223">
</figure>

  **Avoid creating an alert message that is too long.** If possible, keep the message short enough to display on one or two lines. If the message is too long it will scroll, which is not a good user experience.

  **Avoid lengthening your alert text with descriptions of which button to tap,** such as “Tap View to see the information.” Ideally, the combination of unambiguous alert text and logical button labels gives people enough information to understand the situation and their choices. However, if you must provide detailed guidance, follow these guidelines:

*   Be sure to use the word “tap” (not “touch” or “click” or “choose”) to describe the selection action.

*   Don’t enclose a button title in quotation marks, but do preserve its capitalization.

  **Be sure to test the appearance of your alert in both orientations.** Because the height of an alert is constrained in landscape, it might look different from the way it looks in portrait. It’s recommended that you optimize the length of the alert text so that it looks good and avoids scrolling in both orientations.

  **Generally, use a two-button alert.** A two-button alert is often the most useful, because it’s easiest for people to choose between two alternatives. A single button alert is rarely helpful because it informs without giving people any control over the situation. An alert that contains three or more buttons is significantly more complex than a two-button alert and should be avoided if possible. In fact, if you find that you need to offer people more than two choices, you should consider using an action sheet instead (to learn how to use an action sheet, see [Action Sheet](#//apple_ref/doc/uid/TP40006556-CH14-SW36)).

  **Give alert buttons short, logical titles.** The best titles consist of one or two words that make sense in the context of the alert text. Follow these guidelines as you create titles for alert buttons:

*   As with all button titles, use title-style capitalization and no ending punctuation.

*   Use verbs and verb phrases, such as “Cancel,” “Allow,” “Reply,” or “Ignore” that relate directly to the alert text.

*   Use “OK” for a simple acceptance option if there is no better alternative. Avoid using “Yes” or “No.”

*   Avoid “you,” “your,” “me,” and “my” as much as possible. Button titles that use these words are often both ambiguous and patronizing.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW36"></a>

### Action Sheet

  An **action sheet** displays a set of choices related to a task the user initiates (shown below on iPhone). 

<figure class="figure">
<img src="../image/UI Elements/Temporary Views/action_sheet_iphone_2x.png" alt="image: ../Art/action_sheet_iphone_2x.png" width="320" height="315">
</figure>

  To learn how to define an action sheet in your code, see [“Action Sheets”](../UIKitUICatalog/UIActionSheet.html#//apple_ref/doc/uid/TP40012857-UIActionSheet).

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW75"></a>

#### Appearance and Behavior

  On iPhone, an action sheet always emerges from the bottom of the screen. While an action sheet is visible, iOS dims all other onscreen content.

  An action sheet always contains at least two buttons that allow users to choose how to complete their task. When users tap a button, the action sheet disappears. An action sheet doesn’t include a title or explanatory text, because it appears in immediate response to a user action. 

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW76"></a>

#### Guidelines

  Use an action sheet to:

*   Provide alternate ways to complete a task. An action sheet lets you to provide a range of choices that make sense in the context of the current task, without giving these choices a permanent place in the UI.

*   Get confirmation before completing a potentially dangerous task. An action sheet prompts users to think about the potentially dangerous effects of the step they’re about to take and gives them some alternatives. This type of communication is particularly important on iOS devices because sometimes users tap controls without meaning to.

  **On iPhone, include a Cancel button** so that users can easily and safely abandon the task. Place the Cancel button at the bottom of the action sheet to encourage users to read through all the alternatives before making a choice.

  **On both devices, use the red button color if a potentially destructive action can be performed.** Display a red button at the top of the action sheet, because the closer to the top of the action sheet a button is, the more eye-catching it is. And on iPhone, the farther a destructive button is from the bottom of an action sheet, the less likely users are to tap it when they’re aiming for the Home button. 

<figure class="figure">
<img src="../image/UI Elements/Temporary Views/action_sheet_red_button_2x.png" alt="image: ../Art/action_sheet_red_button_2x.png" width="320" height="113">
</figure>

  **Avoid making users scroll through an action sheet.** If you include too many buttons in an action sheet, users must scroll to see all actions. This is a disconcerting experience for users, because they must spend extra time considering each choice. Also, it can be very difficult for users to scroll without inadvertently tapping a button.

</section>

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW3"></a>

### Modal View

  A **modal view**—that is, a view presented modally—provides self-contained functionality in the context of the current task or workflow.

<figure class="figure">
<img src="../image/UI Elements/Temporary Views/modal_view_mail_compose_2x.png" alt="image: ../Art/modal_view_mail_compose_2x.png" width="320" height="548">
</figure>

  To learn more about defining a modal view in your code, see _[UIViewController Class Reference](../../../UIKit/Reference/UIViewController_Class/Reference/Reference.html#//apple_ref/doc/uid/TP40006926)_.

  <section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW77"></a>

#### Appearance and Behavior

  A modal view occupies the entire screen, which strengthens the user’s perception of entering a separate, transient mode in which they can accomplish something. On iPad, a modal view might also occupy the entire area of a parent view, such as a popover.

  A modal view can display text if appropriate, and contains the controls necessary to perform the task. A modal view generally displays a button that completes the task and dismisses the view, and a Cancel button users can tap to abandon the task.

</section>
<section class="section">
  <a name="//apple_ref/doc/uid/TP40006556-CH14-SW78"></a>

#### Guidelines

  Use a modal view when you need to offer the ability to accomplish a self-contained task related to your app’s primary function. A modal view is especially appropriate for a multistep subtask that requires UI elements that don’t belong in the main app UI all the time. 

  **On iPhone, coordinate the overall look of a modal view with the appearance of your app.** For example, a modal view often includes a navigation bar that contains a title and buttons that cancel or complete the modal view’s task. When this is the case, the navigation bar should use the same appearance as the navigation bar in the app.

  **On all devices, display a title that identifies the task, if appropriate.** You might also display text in other areas of the view that more fully describes the task or provides some guidance. 

  **On both devices, choose an appropriate transition style for revealing the modal view.** Use a style that coordinates with your app and enhances the user’s awareness of the temporary context shift that the modal view represents. To do this, you can specify one of the following transition styles:

*   **Vertical.** The modal view slides up from the bottom edge of the screen and slides back down when dismissed. (This is the default transition style.)

*   **Flip.** The current view flips horizontally from right to left to reveal the modal view. Visually, the modal view looks as if it is the back of the current view. When the modal view is dismissed, it flips horizontally from left to right, revealing the previous view.

  If you decide to vary the transition styles of the modal views in your app, avoid doing so merely for the sake of variety. Users are quick to notice such differences and will assume that they mean something. For this reason, it’s best to establish a logical, consistent pattern that users can easily detect and remember, and avoid changing transition styles without a good reason.

</section>

</section>
</article>