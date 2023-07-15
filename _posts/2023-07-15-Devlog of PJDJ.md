---
layout: post
title: Devlog of PJDJ Episode III
subtitle: Mark Time
cover-img: /assets/img/cover/hello_world.png
tags: [GameDev, Journal]
---

## About Development

### Development Tools

This part of the development work doesn't introduce any new game features, but implementing them is necessary. These development tools are expected to save more development time in the future.

The tools include the Command Pattern and Transition Management. The core requirement for implementing them is to enable visual development within the editor, instead of hard-coding some logic in scripts. This allows for flexible addition and modification of functionalities while keeping the scripts clean and stable.

The **Command Pattern** is a design pattern that encapsulates operations as commands and manages them uniformly. Its most common use is for "Undo" functionality. In the current game development, *Yarn Spinner* already has an expandable Command system built-in, but it can only be used within Yarn scripts. Therefore, a command system that can be flexibly used within the editor is still needed.

**Transition Management** involves encapsulating various types of ease-in-out animations into transitions with two states. The animation functionality can be achieved using the *DoTween* plugin, requiring additional encapsulation to conveniently control Tran In and Tran Out.

### Cutscenes

A simple animation and text playback system, similar to a PowerPoint presentation, is used to display cutscene content. The text content can also be managed using Yarn scripts. This straightforward format should be sufficient for creating all cutscene animations.

![Cutscenes][cutscenes]

### Turntable Features

The turntable is likely the most crucial part of the gameplay. Previously, some less important modules of the turntable were developed, but this time the focus is on implementing the features for reading and playing records. The complete process—from taking a record from the record sleeve, placing it on the turntable platter, placing the needle on the record, and playing music based on the needle's position—is now operational.

During development, I also cleaned and organized the scripts related to the turntable. This script refactoring proved to be a valuable experience and should be helpful for developing new features in the future.

![Turntable][turntable]

### Records Bag Features

Presenting records bag within the game is a challenging and interesting design problem. The available screen space in the game is limited, and the turntable and mixer already occupy most of it. So the question is how to display the records bag. One approach is to use a UI to bring up the records bag, select a record, and then hide it. Another approach involves controlling camera movement to slide and reveal the area for placing the records bag. Currently, the implemented method is the first one, as it is relatively simpler to implement. However, it does come with some challenges since I have to manage the record cover through UI space while the record exists within the game scene. This might cause some difficulties and the interaction method might feel a bit weird. But for now, this system is functional.

![Records Bag][records bag]

### Scene Loading

Implementing the scene loading functionality took more time than anticipated, but the final result is quite satisfying. The implementation approach involves synchronously loading the target scene from a dedicated "loading" scene. A [tutorial](https://gamedevbeginner.com/how-to-load-a-new-scene-in-unity-with-a-loading-screen/) found online provides a clear explanation of how to load scenes and serves as a good reference.

I'm particularly pleased with the final presentation of the loading scene. It has a simple yet fitting design that aligns well with the game's theme.

![Loading Scene][loading]

### Title Page and Others

Developing these components can be seen as a trap because, compared to the game's progression, they are relatively less important. However, at the same time, I have a desire to design them as comprehensively as possible in one go, so they can be utilized effectively in the future. But clearly, this would require a significant amount of time, which could be better spent on more crucial matters.


## About Personal Reflection

### Positive Experience

On the final day of this development cycle, I felt really good about working on the jukebox functionality. I could fully focus on the task at hand without constantly switching between different tasks due to feelings of apprehension. In summary, there are several reasons why I had this positive experience: Firstly, these functionalities are the most crucial ones in the game, so mentally it felt less burdensome to dedicate time to the most important tasks. Secondly, compared to art-related design work and system development, implementing specific functionalities is an area where I am relatively skilled, so it felt more effortless. Lastly, I could sense the accumulation of experience throughout this process, which gives me more confidence for future development.

### Areas for Improvement

Despite encountering some pitfalls in the previous development cycle, I still fell into them this time. During the first half of this development cycle, almost all of my time was spent on developing non-core game functionalities. Focusing on the most essential parts may not be as easy as imagined because it means inevitably facing numerous design challenges and unexpected surprises. On the other hand, the development of peripheral functionalities is relatively straightforward and has readily available references. Therefore, it may require some practical methods to achieve this goal.

In addition, the habit of writing down the issues that need improvement and the goals for the current development cycle on a whiteboard was not maintained this time, which led to confusion when selecting daily work objectives. It must be said that placing ideas in a prominent location will have a subtle influence over time, so in the next development cycle, it is necessary to restore this habit.

### Insights

Focus has an astonishing impact on the efficiency and quality of completing work. At the same time, taking breaks is equally important to ensure a focused state of mind. When it's difficult to enter a state of concentration, it may indicate the need for rest. In such cases, instead of multitasking with relatively easier tasks, it's better to take a proper break.

Receiving feedback from others can be extremely helpful during development, and the sooner, the better. Therefore, setting a goal for the next phase could be to release a playable version for real players to interact with. This can help me gain a clearer understanding of which aspects need to be prioritized.

[cutscenes]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_III_01.gif
[turntable]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_III_02.gif
[records bag]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_III_03.gif
[loading]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_III_04.gif