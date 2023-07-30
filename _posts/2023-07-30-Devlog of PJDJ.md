---
layout: post
title: Devlog of PJDJ Episode IV
subtitle: Heavy Rain
cover-img: /assets/img/cover/hello_world.png
tags: [GameDev, Journal]
---

## About Development

### Mixer

Finally, the basic functionality of the mixer has been implemented, and two turntables can now work together on the desktop. The part that controls the volume of an individual channel (Channel Fader) in the mixer is achieved through the Mixer module in the engine. As for the function to switch between two channels (Cross Fader), two curves are defined to map the balance between the two channels. This allows for more flexible mixing options, and it's relatively easy to make modifications.

The most challenging part of development was implementing the audio visualization feature. This was mainly due to Unity engine's audio Mixer module not providing a readily applicable interface. However, a less direct approach was eventually found to achieve the desired effect.

But having only these functionalities doesn't mean the mixer development is complete. At the very least, there's a need to add knobs for controlling the volume of the three frequency ranges (high, mid, low equalizer) to consider the mixer as having basic functionality.

![Mixer][mixer]

### Scratching Feature

The scratching feature is perhaps one of the most iconic characteristics of a DJ's profession. With this feature, the turntable's functionality is finally relatively complete. However, the current version still has a significant issue to address: the sound effect when scratching and rotating the record on the turntable is not as ideal as expected. It's unclear whether this is related to the music used for the record, but this sound effect is crucial. The next step is undoubtedly to optimize it properly.

![Scratching][scratching]

### Record Handling Interaction

The main goal was to adjust the design to allow for picking up and putting back records to fit both turntables, while also supporting different record sizes. This seemingly minor change took a considerable amount of time, and there is still room for significant improvements. It is almost certain that the record pack's part will be modified to be displayed in a hand-held card form. After this change, the position on the table where the selected records are placed will also be adjusted accordingly.

![Records Bag][records bag]

### Record Collection

Preparing a complete set and selecting the music to play is one of the most crucial tasks for a DJ. This process is very similar to building a deck in a card game. Therefore, I designed the record collection module and playlist-building module based on the framework of a card game. There are still many areas in the collection module that need improvement, such as classification and sorting functions. However, these are not the most urgent features for now, and it would be more appropriate to focus on developing more critical modules first.

![Record Collection][record collection]


## About Myself

### Positive Feelings

I felt really good on the first day of developing the mixer module. The functionality was implemented quickly, and even when facing a few challenges, I remained relatively calm in seeking solutions. This was undoubtedly due to being well-prepared and well-rested. I should try to create similar conditions for the rest of the development process.

### Room for Improvement

I noticed that when spending a long time fixing bugs or adjusting designs instead of creating new features, I tend to get a bit impatient. This is an area that needs improvement. The main reason behind this impatience is probably not having a proper understanding of my development capabilities, making it difficult to accurately estimate the required time.

Additionally, the core gameplay part of the game still hasn't been developed this week. Although the implemented features are closely related to gameplay, they seem to be more about adding depth to the game. Such elements should be pushed forward once the core loop of the game is operational; otherwise, it may lead to wasted efforts.

### Inspiration

Once I started the development process, I hardly picked up any books. During this development cycle, I managed to read some things during a trip, although it's challenging to say how directly helpful they will be for development. However, they did provide me with a lot of inspiration and ideas for both life and development. Perhaps, on regular evenings, I should go out for a walk, bask in the sun, or enjoy the breeze. It might be much more helpful than sitting in front of the screen all the time.

[mixer]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_IV_01.gif
[scratching]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_IV_02.gif
[records bag]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_IV_03.gif
[record collection]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_IV_04.gif