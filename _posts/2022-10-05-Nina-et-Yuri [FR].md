---
layout: single
header:
  teaser : /assets/images/banner_test.png
  overlay_image: /assets/images/banner_test.png
  caption: "Photo credit: [**Echinops**](https://twitter.com/Echinopspsps)"
  actions:
    - label: "More Info"
      url: "https://tom-gatineau.itch.io/nina-et-yuri "
title:  "Nina & Yuri [FR]"
toc: true
toc_label: "Table of content"
toc_icon: "cogs"
toc_sticky : true

---
# Un plateformer né en Game Jam

![Pres Nina Yuri Portefolio](https://user-images.githubusercontent.com/114059469/191930265-32b12a1c-e7ff-4f4b-8aab-13ac1c99aadc.png)


# Une courte présentation

Bienvenue sur le Wiki de Nina&Yuri.

Ce projet a été réalisé dans le cadre de la Emotional Game Jam de 2022. Tout le code de la version actuelle (21/09/22) proviens donc de cette version. Il a été réalisé sur la version 4.27 du moteur Unreal Engine.

Le principe de fonctionnement du jeu est le switch entre deux modes d'affichages, un mode 2D et un mode 3D accompagnés d'une modification des hitbox et des rendus de caméra (perspective vers isométrique).

Le développement du jeu se fait en blueprint sans intégration de code C pour le moment.

EDIT du 29/09/22 : le projet a reçu le tremplin du concours de la Gamecup et va donc être poursuivi dans une version complète du jeu. Par conséquent, tous blueprint visible dans ce wiki seront issues de la version Pre-Alpha V1.3 Name : Finale Game Jam


***
# Mécanique de base
## Changement de caméra

Pour introduire le travail sur le projet, la première problématique c'est poser sur le changement de caméra entre les deux modes d'affichages. 
Ex ci-dessous :

En 2D
![ny_2D](https://user-images.githubusercontent.com/114059469/191619607-fe846042-73ab-4073-b8f1-478cf66c0ede.png)
En 3D
![ny_3D](https://user-images.githubusercontent.com/114059469/191619643-f8f51dac-5199-43ea-98ce-a3b8efb9b7b0.png)

Pour ce faire, le programme vérifie lorsque il y a une rotation si le player rentre dans un angle de 10° correspondant à un angle de vue en 2 dimensions. Lorsque cette condition est vraie, un changement de caméra entre celle attachée au player et celle fixe en vue orthographique est opérée. 

## Changement des Hitbox

Lorsque la condition "Personnage en 2D" est vrai, un changement sur les hitbox des différentes plateformes est opéré, celles-ci vois la valeur Box Extent augmenté de manière drastique afin de permettre au personnage de ce mouvoir dessus même si la plateforme en question n'es pas sur le même plan que le joueur. 

# Animation du player

Le personnage et son animation Frame-by-Frame repose sur l'utilisation d'un Flipbook permettant ainsi de switcher les différentes frames rapidement durant le jeu. 

Voici un exemple du fonctionnement des changements de frames dans le jeu : 


![ezgif-1-343b3dc1e6](https://user-images.githubusercontent.com/114059469/193783795-0cf2ac5d-b971-4870-8f2f-54cfd2a22a12.gif)

Et la traduction au niveau des blueprints :
![ScreeBP](https://user-images.githubusercontent.com/114059469/193783831-9f377285-856c-48c7-805f-4895b39295fd.png)

# Avancée future du projet
## Evolution visuel

Je vais rester succinte sur cette partie, l'une des première évolution qui devrait arriver pour Nina & Yuri est l'arrivée d'une maj visuel. L'idée, bien entendu, serait de conserver la DA tout en faisant évoluer le niveau de polish et le travail sur les textures; l'application d'une trimsheet est par ailleurs en réflexion afin d'allèger la demande en matière de performance. La pertinence également d'une utilisation de displacement map pour passer les props dans des version low poly est également en réflexion par plusieurs membres de l'équipe. 

## Evolution mécanique

Sur ce plan, c'est avant tout une mise à jour du moteur qui est prévue, passant le projet de UE4 vers UE5 afin de profiter de certaines nouveautés offertes par nanite. Un retravail complet de la programmation des différents éléments est aussi en reflexion afin de préparer les futures évolutions du jeu qui ne sont pas encore pleinement envisageables à la vue de l'état actuel du projet (PreAlpha V1.3).

***

Vous pouvez suivre les actualités du projet ici : https://twitter.com/NinaYuriTheGame

La démo est également disponible par là : https://tom-gatineau.itch.io/nina-et-yuri 
![Nina-yurt-logo](https://user-images.githubusercontent.com/114059469/193817889-a0feb3ca-9cdd-4fac-8fdd-f7866550b63f.png)