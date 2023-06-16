---
layout: post
title: Devlog of PJDJ Episode I
subtitle: Setting Sail
cover-img: /assets/img/cover/hello_world.png
tags: [GameDev, Journal]
---

## About Development

### Inspiration

I want to create a game about *music*, not the conventional rhythm-based action games commonly referred to as "music games," but a game that truly revolves around music. I can't recall exactly when this idea took root in my mind, but it was probably over a year ago during an **Open DJ Night** event in *fRUITYSPACE*. The hazy imaginations I had at that time started to solidify, and the initial concept of the game began to take shape. Moments of listening to music have always been delightful, at least for me, but it seems I have been struggling to find dedicated opportunities to appreciate music. I realized that in order to regain those wonderful moments, I needed to position myself differently, just like a radio host or a DJ in an electronic club. When I find myself in a similar position, the things I anticipate naturally come to fruition.

So, the goal of this game is to create such a position where players can **share** music. It would be even better if players can take a step further from enjoyment to creation. Of course, I also hope the game can reach a wider audience. The dense array of knobs on a mixing console or the interface of a digital audio workstation can be intimidating. However, leading players into an unfamiliar domain through a smoother and friendlier approach is precisely what video games excel at.

### Previous Attempts

In early 2022, after the idea of creating a *music-playing* game emerged, I did some work. I initially envisioned it as a 3D game, similar to *Passpartout: The Starving Artist*, where players would act as a DJ in a bar, and the customers would vote with their feet, deciding whether to stay longer. However, due to various reasons, the progress of the 3D version halted at the stage of setting up a Unity project and importing some models downloaded from [Sketchfab](https://sketchfab.com/). Eventually, the project files disappeared when I replaced my hard drive.

In June of this year, I started working on the game again. I don't know if I will be able to finish it, where the music will come from, or even if it will sustain me in the future. However, I do know that while working on it, I can alleviate some anxiety and cultivate a greater fondness for this beautiful world. This time, after a relatively serious evaluation of my development abilities, I decided to create a pixel art-style 2D game, perhaps similar to *Papers, Please*. Generating pixel art assets may take more time than learning 3D modeling, but I am more inclined to work on those pixels.

### Technology

The game will be developed using the **Unity** engine, which is almost the only choice for me and also the most suitable one. The game will utilize the URP (Universal Render Pipeline) for rendering. After researching, I found it to be a more appropriate choice, and the official support for this rendering method will likely save me time when dealing with lighting and shadow issues, even though I haven't yet explored its advantages.

Setting up the development workflow for pixel art has proven to be more challenging than I anticipated. The first decision to make was regarding the resolution, and that choice was relatively straightforward since there are plenty of samples to refer to. In the end, I decided to use a native resolution of 640 x 360 pixels, which can still adapt to 16:9 display devices when scaled 1:3. Managing pixel art assets is also relatively easy thanks to Unity's recently provided official **Aseprite** file import tool. This allows me to directly modify .ase format files in the project, just like opening .PSD files, saving me a lot of time.

Almost all of the troubling issues are related to camera control, and I still haven't found suitable solutions for some of these problems (which will likely require solving through programming). These problems mainly arise from my desire to present different content in the upper and lower parts of the screen, with the upper part showing the panoramic view of the game scene and the lower part being the control area. The intuitive approach would be to use different cameras to capture the two separate scenes and then overlay them together. However, due to the inability of PixelPerfectCamera to support screen resizing, this approach had to be abandoned. Then I planned to implement the game's control interface entirely using UI elements. However, after almost completing all the functionality, I realized that although using UI components seemed convenient and quick with many ready-to-use options, it would become quite inconvenient later on. One simple example is that UI components tend to have a fixed presentation, which is not ideal for objects that require frequent movement or rotation. Additionally, many features in URP (Universal Render Pipeline) are designed for game scenes and do not adapt well to UI elements. Therefore, in the end, I returned to using 2D scenes to implement the control part.

![Demo Illustration][illustration]

Next is the choice of PixelPerUnit (PPU). Although this choice does not affect the final visual presentation of the game, it does impact the scale of various values during development. Initially, I should have chosen the PPU based on the size of characters in the game. However, because there are upper and lower sections, I need to decide which side to use as a reference or find a balance between the two. I initially set the PPU to 64 and later adjusted it to 32.

Finally, there is the issue of pixel alignment. I want the final visuals of the game to have a retro style, where elements in the game are aligned on a pixel scale even if they are divided into multiple layers. I have already set the correct positions for all game objects through calculations, and their states appear correctly in the editor window. However, after going through the camera, they appear misaligned in the game window. This greatly affects the presentation effect of a pixel game, and I am still searching for a solution to this problem.

## About Myself

### Positive Feelings

For the first time, I am starting a project as a "solo developer" with a potentially long development cycle, and it's undoubtedly an exciting thing. Although I have made similar attempts before, I was never alone, always relying on others. Development outside of work has always been more like a hobby for me, unrelated to my livelihood, and the success or failure of those attempts didn't have a significant impact on my life. But this time seems different.

I have never been a brave person, unable to withstand the fear of the unknown, and therefore unable to experience the excitement and joy that uncertainty can bring. When making the decision to start this project, it also took a long time for me to prepare mentally. But it seems that starting to do this is easier than I imagined. The motivation to continue on my own is stronger than during the daydreaming phase. Maybe the real problems haven't hit me yet, or perhaps even if they arise, solutions will follow. I'm increasingly reluctant to think about these future problems and find it more practical to focus on solving the current ones.

### Continuous Effort Required

There is still a significant gap between time management and my planned schedule, which is clearly harmful to sustainable development work.

I was mentally prepared for the challenge of dividing work and rest when developing alone at home, but the actual situation is still far from what I expected. I can hardly have a day where I can work diligently for 7-8 hours like I used to in the studio and then have the rest of the time for myself. I believe this is closely related to not setting more specific and detailed work goals at the beginning of each day. To achieve this, it's crucial to have sufficient sleep to maintain a refreshed state in the morning. So the first problem to tackle is probably going to bed on time. Additionally, incorporating rituals to establish a more regular development rhythm can be helpful, such as adding reminders in visible places to stay focused.


[illustration]:/assets/img/images_in_blogs/Devlog_of_PJDJ_Episode_I_01.png