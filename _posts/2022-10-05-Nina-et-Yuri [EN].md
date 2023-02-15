---
layout: single
header:
  teaser : /assets/images/banner_test.png
  overlay_image: /assets/images/banner_test.png
  caption: "Photo credit: [**Echinops**](https://twitter.com/Echinopspsps)"
  actions:
    - label: "More Info"
      url: "https://tom-gatineau.itch.io/nina-et-yuri "
title:  "Nina & Yuri [EN]"
toc: true
toc_label: "Table of content"
toc_icon: "cogs"
toc_sticky : true

---
# A platformer born in Game Jam

![NYPresEN](/assets/images/NYPresEN.png)


# A short presentation

Welcome to the Nina&Yuri Wiki.

This project was made as part of the Emotional Game Jam 2022. Hasn't been updated. It was made on version 4.27 of the Unreal Engine.

The operating principle of the game is the switch between two display modes, a 2D mode and a 3D mode accompanied by a modification of hitboxes and camera renderings (perspective to isometric).

The development of the game is done in blueprint without integration of C code for the moment.

EDIT of 09/29/22: the project received the springboard from the Gamecup competition and will therefore be continued in a full version of the game. Consequently, all the blueprints visible in this wiki will be from the Pre-Alpha V1 version .3 Name: Finale Game Jam


***
# Basic mechanics
## Change camera

To introduce the work on the project, the first problem I encountered was the change of camera between the two display modes.
Example below:

In 2D
![ny_2D](https://user-images.githubusercontent.com/114059469/191619607-fe846042-73ab-4073-b8f1-478cf66c0ede.png)
In 3D
![ny_3D](https://user-images.githubusercontent.com/114059469/191619643-f8f51dac-5199-43ea-98ce-a3b8efb9b7b0.png)

To do this, the rotation happens if the enters an angle of 10° corresponding to a viewing angle in 2 dimensions. A change of camera between the one attached to the player and the fixed one in orthographic view is operated.

## Hitbox change

When the "Character in 2D" condition is true, a change on the hitboxes of the different platforms is activated, these see the Box Extent value increased drastically in order to allow the character to move on it even if the platform in question is not on the same plane as the player.

# Player animation

The character and its Frame-by-Frame animation are based on the use of a Flipbook, which allows you to switch between the different images quickly during the game.

Here is an example of how frame changes work in-game:


![ezgif-1-343b3dc1e6](https://user-images.githubusercontent.com/114059469/193783795-0cf2ac5d-b971-4870-8f2f-54cfd2a22a12.gif)

And the translation at the level of the plans:
![ScreeBP](https://user-images.githubusercontent.com/114059469/193783831-9f377285-856c-48c7-805f-4895b39295fd.png)

# Future progress of the project
## Visual evolution

I'll keep this part brief, one of the first changes that should happen for Nina & Yuri is the arrival of a visual update. The idea, of course, would be to keep the AD while polishing the level and working on the textures; the application of a Trimsheet is also under consideration in order to alleviate the demand in terms of performance. The relevance of using the movement card to pass the accessories in the low poly version is also being considered by several members of the team.

## Mechanical Evolution

On this level, it is above all an update of the engine which is planned, passing the project from UE4 to UE5 in order to take advantage of certain new features offered by nanite. A complete rework of the programming of the various elements is also under consideration in order to prepare the future evolutions of the game which are not yet envisaged in view of the current state of the project (PreAlpha V1.3).

***

You can follow the project news here: https://twitter.com/NinaYuriTheGame

The demo is also available here: https://tom-gatineau.itch.io/nina-et-yuri 
![Nina-yurt-logo](https://user-images.githubusercontent.com/114059469/193817889-a0feb3ca-9cdd-4fac-8fdd-f7866550b63f.png)