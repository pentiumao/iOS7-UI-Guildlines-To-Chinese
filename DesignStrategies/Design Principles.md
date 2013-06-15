## Design Principles

>	**Important**  
>	This is a preliminary document for an API or technology in development. Although this document has been reviewed for technical accuracy, it is not final. This Apple confidential information is for use only by registered members of the applicable Apple Developer program. Apple is supplying this confidential information to help you plan for the adoption of the technologies and programming interfaces described herein. This information is subject to change, and software implemented according to this document should be tested with final operating system software and final documentation. Newer versions of this document may be provided with future seeds of the API or technology.

### Aesthetic Integrity

  Aesthetic integrity doesn’t measure the beauty of an app’s artwork or characterize its style; rather, it represents how well an app’s appearance and behavior integrates with its function to send a coherent message. 

<img src="../image/DesignStrategies/Design Principles/aesthetic_2x.png" alt="image: ../Art/aesthetic_2x.png" width="638" height="332">

  People care about whether an app delivers the functionality it promises, but they’re also affected by the app’s appearance and behavior in strong—sometimes subliminal—ways. For example, an app that helps people perform a serious task can put the focus on the task by keeping decorative elements subtle and unobtrusive and by using standard controls and predictable behaviors. This app sends a clear, unified message about its purpose and its identity that helps people trust it. But if the app sends mixed signals by presenting the task in a UI that’s intrusive, frivolous, or arbitrary, people might question the app’s reliability or trustworthiness.

  On the other hand, in an app that encourages an immersive task—such as a game—users expect a captivating appearance that promises fun and excitement and encourages discovery. People don’t expect to accomplish a serious or productive task in a game, but they expect the game’s appearance and behavior to integrate with its purpose. 

### Consistency

  Consistency lets people transfer their knowledge and skills from one part of an app’s UI to another and from one app to another app. A consistent app isn’t a slavish copy of other apps and it isn’t stylistically stagnant; rather, it pays attention to the standards and paradigms people are comfortable with.

<img src="../image/DesignStrategies/Design Principles/consistency_2x.png" alt="image: ../Art/consistency_2x.png" width="500" height="199">


  To determine whether an iOS app follows the principle of consistency, think about these questions:

*   Is the app consistent with iOS standards? Does it use system-provided controls, views, and icons correctly? Does it incorporate device features in a reliable way?

*   Is the app consistent within itself? Does text use uniform terminology and style? Do the same icons always mean the same thing? Can people predict what will happen when they perform the same action in different places? Do custom UI elements look and behave the same throughout the app?

*   Within reason, is the app consistent with its earlier versions? Have the terms and meanings remained the same? Are the fundamental concepts and primary functionality essentially unchanged?

### Direct Manipulation

  When people directly manipulate onscreen objects instead of using separate controls to manipulate them, they're more engaged with their task and it’s easier for them to understand the results of their actions.
  
<img src="../image/DesignStrategies/Design Principles/manipulation_2x.png" alt="image: ../Art/manipulation_2x.png" width="557" height="271">

  Using the Multi-Touch interface, people can pinch to directly expand or contract an image or content area. And in a game, players move and interact directly with onscreen objects—for example, a game might display a combination lock that users can spin to open.

  In an iOS app, people experience direct manipulation when they:

*   Rotate or otherwise move the device to affect onscreen objects

*   Use gestures to manipulate onscreen objects

*   Can see that their actions have immediate, visible results

### Feedback

  Feedback acknowledges people’s actions, shows them the results, and updates them on the progress of their task. 
  
<img src="../image/DesignStrategies/Design Principles/feedback_2x.png" alt="image: ../Art/feedback_2x.png" width="465" height="304">

  The built-in iOS apps provide perceptible feedback in response to every user action. List items and controls highlight briefly when people tap them and—during operations that last more than a few seconds—a control shows elapsing progress. 

  Subtle animation can give people meaningful feedback that helps clarify the results of their actions. For example, lists can animate the addition of a new row to help people track the change visually. 

  Sound can also give people useful feedback, but it shouldn’t be the only feedback mechanism because people can’t always hear their devices.

### Metaphors

  When virtual objects and actions in an app are metaphors for familiar experiences—whether these experiences are rooted in the real world or the digital world—users quickly grasp how to use the app.

  It’s best when an app uses a metaphor to suggest a usage or experience without letting the metaphor enforce the limitations of the object or action on which it’s based.

  iOS apps have great scope for metaphors because people physically interact with the screen. Metaphors in iOS include:

*   Moving layered views to expose content beneath them

*   Dragging, flicking, or swiping objects in a game

*   Tapping switches, sliding sliders, and spinning pickers

*   Flicking through pages of a book or magazine

### User Control

  People—not apps—should initiate and control actions. An app can suggest a course of action or warn about dangerous consequences, but it’s usually a mistake for the app to take decision-making away from the user. The best apps find the correct balance between giving people the capabilities they need while helping them avoid unwanted outcomes. 

<img src="../image/DesignStrategies/Design Principles/user_control_2x.png" alt="image: ../Art/user_control_2x.png" width="322" height="241">

  Users feel more in control of an app when behaviors and controls are familiar and predictable. And when actions are simple and straightforward, users can easily understand and remember them. 

  People expect to have ample opportunity to cancel an operation before it begins, and they expect to get a chance to confirm their intention to perform a potentially destructive action. Finally, people expect to be able to gracefully stop an operation that’s underway.

[Integrating with iOS](Integration.html#//apple_ref/doc/uid/TP40006556-CH61-SW1)

[From Concept to Product](Process.html#//apple_ref/doc/uid/TP40006556-CH6-SW1)

Copyright © 2013 Apple Inc. All rights reserved. Apple Confidential Information. 
[Terms of Use](http://www.apple.com/legal/terms/site.html)   |  [Privacy Policy](http://www.apple.com/legal/privacy/)  |   [Updated: 2013-06-13](RevisionHistory.html#//apple_ref/doc/uid/TP40006556-CH99-SW1)