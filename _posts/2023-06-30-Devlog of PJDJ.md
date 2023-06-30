---
layout: post
title: Devlog of PJDJ Episode II
subtitle: Long Night
cover-img: /assets/img/cover/hello_world.png
tags: [GameDev, Journal]
---

## About Development

### Environmental Art

The main visuals of the game consist of the upper half, which depicts a scene similar to a DJ booth where visitors gather, and the lower half, which represents the control interface. For the artistic style of the lower section, I aim to achieve a pixel art style similar to "Please, Don't Touch Anything." The corresponding upper scene should also maintain a consistent style.

I drew inspiration for the visual style of the first scene from the underground jazz bars I often visit. Its spatial layout is suitable for a narrow area. When choosing the perspective for the scene, I spent a considerable amount of time on reference and deliberation. Initially, I thought about using a perspective similar to *TMNT: Shredder's Revenge* to present the scene. On one hand, this game's pixel art style is more realistic and closer to the style of the control interface. On the other hand, the game's assets can be found on SpriteResource, making it convenient for reference. However, during the art experimentation process, I realized that creating assets in this style would be time-consuming and challenging. I briefly considered a 2D side-scrolling style without depth, similar to backgrounds in 2D platformer games, but I found that this style wasn't suitable for depicting crowded scenes. Therefore, I abandoned that idea and returned to the original style.

### Characters

Designing the characters for the game is an interesting task. My concept is to depict anthropomorphic animal characters, drawing inspiration from the Japanese anime *Odd Taxi* and the text-based adventure game *Night in the Woods*. This kind of setting creates a greater distance from reality and allows for more imaginative possibilities for the characters. Undoubtedly, the game will require a significant number of characters, and some animation will be necessary. Creating all the content manually is impractical, so I need to find a way to generate characters programmatically and reuse animations.

Through the process of drawing, I have accumulated some experience. In the initial design phase, it might be more suitable to work on a single layer rather than dividing different positions into separate layers. Layered drawing may be more suitable to consider once the overall style is determined, especially for pixel art.

### Dialogue System

The open-source dialogue system [Yarn Spinner](https://docs.yarnspinner.dev/) provides great convenience. Using it, I can easily edit dialogues and organize the game's flow in the future. It allows me to independently write scripts directly in a text document, without relying too heavily on in-game functionality.

![Demo Illustration][illustration]

### Title Page and Others

Developing these components can be seen as a trap because, compared to the game's progression, they are relatively less important. However, at the same time, I have a desire to design them as comprehensively as possible in one go, so they can be utilized effectively in the future. But clearly, this would require a significant amount of time, which could be better spent on more crucial matters.


## About Personal Reflection

### Positive Experiences

During the first half of this work cycle, I have been in a great development state. I thoroughly enjoy the process and have gained more confidence for the upcoming development tasks. Moreover, I have been able to strike a better balance between my personal life and work, which has helped me feel more at ease. While I am aware that I need to focus more and increase my efficiency, seeing the game gradually taking shape brings me a sense of fulfillment.

### Areas for Improvement

To complete the game or even just its demo, I need to have more confidence in myself. I am fully aware of this, but it's challenging to achieve, especially when working on tasks that are not my strong suit. Confidence can easily be shattered, and it significantly affects my development state. However, I have yet to reach the point where I am not influenced by such emotions.

Additionally, it seems that I have spent too much time on researching and studying outstanding works. While learning from successful examples is helpful, I have devoted an excessive amount of time to it. In the next work cycle, I should allocate more time to independently completing the development rather than attempting to find the optimal solution. Minimizing exposure to successful cases can also be beneficial for building confidence. I should lower my expectations and not constantly strive for the highest quality of an independent game on the first attempt. Good things often require more time, effort, and a better development state. Expecting outstanding results in a short period ultimately leads to self-doubt and erodes confidence in completing the game. For me, setting longer cycles to allow for a more relaxed development process may be a better choice. I believe that as development progresses, I will gain a clearer understanding of my own development abilities.


[illustration]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_II_01.png