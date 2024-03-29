---
layout: single
header:
  teaser : /assets/images/banner_test.png
  overlay_image: /assets/images/banner_test.png
  caption: "Photo credit: [**Echinops**](https://twitter.com/Echinopspsps)"
  actions:
    - label: "itch.io"
      url: "https://tom-gatineau.itch.io/nina-et-yuri "
title:  "Nina & Yuri [EN]"
toc: true
toc_label: "Table of content"
toc_icon: "cogs"
toc_sticky : true
gallery:
  - url: https://user-images.githubusercontent.com/114059469/191619607-fe846042-73ab-4073-b8f1-478cf66c0ede.png
    image_path: https://user-images.githubusercontent.com/114059469/191619607-fe846042-73ab-4073-b8f1-478cf66c0ede.png
    alt: "Visuel du jeu en 2D"
    title: "Visuel du jeu en 2D"
  - url: https://user-images.githubusercontent.com/114059469/191619643-f8f51dac-5199-43ea-98ce-a3b8efb9b7b0.png
    image_path: https://user-images.githubusercontent.com/114059469/191619643-f8f51dac-5199-43ea-98ce-a3b8efb9b7b0.png
    alt: "Visuel du jeu en 3D"
    title: "Visuel du jeu en 3D"

---
# A platformer born in Game Jam

![NYPresEN](/assets/images/NYPresEN.png)

Want to see this article in french ? Go here : [French version](https://dwenshell.github.io/Nina-et-Yuri-FR/){: .btn .btn--info} 
{: .notice}

# A short presentation

Welcome to the Nina&Yuri Wiki.

This project was made as part of the Emotional Game Jam 2022. Hasn't been updated. It was made on version 4.27 of the Unreal Engine.
{: .text-justify}

The operating principle of the game is the switch between two display modes, a 2D mode and a 3D mode accompanied by a modification of hitboxes and camera renderings (perspective to isometric).
{: .text-justify}

The development of the game is done in blueprint without integration of C code for the moment.
{: .text-justify}

EDIT of 09/29/22: the project received the springboard from the Gamecup competition and will therefore be continued in a full version of the game. Consequently, all the blueprints visible in this wiki will be from the Pre-Alpha V1 version .3 Name: Finale Game Jam
{: .text-justify}


***
# Basic mechanics
## Change camera

To introduce the work on the project, the first problem I encountered was the change of camera between the two display modes.
{: .text-justify}
Example below:

{% include gallery layout="half" caption="Quelques visuels ingame" %}

To do this, the rotation happens if the enters an angle of 10° corresponding to a viewing angle in 2 dimensions. A change of camera between the one attached to the player and the fixed one in orthographic view is operated.
{: .text-justify}

## Hitbox change

When the "Character in 2D" condition is true, a change on the hitboxes of the different platforms is activated, these see the Box Extent value increased drastically in order to allow the character to move on it even if the platform in question is not on the same plane as the player.
{: .text-justify}

# Player animation

The character and its Frame-by-Frame animation are based on the use of a Flipbook, which allows you to switch between the different images quickly during the game.
{: .text-justify}

Here is an example of how frame changes work in-game:


![ezgif-1-343b3dc1e6](https://user-images.githubusercontent.com/114059469/193783795-0cf2ac5d-b971-4870-8f2f-54cfd2a22a12.gif)

And the translation at the level of the plans:
![ScreeBP](https://user-images.githubusercontent.com/114059469/193783831-9f377285-856c-48c7-805f-4895b39295fd.png)

# Future progress of the project
## Visual evolution

I'll keep this part brief, one of the first changes that should happen for Nina & Yuri is the arrival of a visual update. The idea, of course, would be to keep the AD while polishing the level and working on the textures; the application of a Trimsheet is also under consideration in order to alleviate the demand in terms of performance. The relevance of using the movement card to pass the accessories in the low poly version is also being considered by several members of the team.
{: .text-justify}

## Mechanical Evolution

On this level, it is above all an update of the engine which is planned, passing the project from UE4 to UE5 in order to take advantage of certain new features offered by nanite. A complete rework of the programming of the various elements is also under consideration in order to prepare the future evolutions of the game which are not yet envisaged in view of the current state of the project (PreAlpha V1.3).
{: .text-justify}

***

You can follow the project news here: [Twitter](https://twitter.com/NinaYuriTheGame){: .btn .btn--info}

The demo is also available here: [itch.io](https://tom-gatineau.itch.io/nina-et-yuri){: .btn .btn--info}
![Nina-yurt-logo](https://user-images.githubusercontent.com/114059469/193817889-a0feb3ca-9cdd-4fac-8fdd-f7866550b63f.png)