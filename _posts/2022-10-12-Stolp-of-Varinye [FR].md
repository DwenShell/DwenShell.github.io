---
layout: single
header:
  teaser : /assets/images/banner_stolp.png
title:  "Stolp of Varinye [FR]"
toc: true
toc_label: "Table of content"
toc_icon: "cogs"
toc_sticky : true

---

# Commençons par une présentation

Qu'est-ce que Stolp of Varinye ? 

Il s'agit de l'ébauche d'un projet réalisé en collaboration avec 2 amis pour valider notre année de L2. Bien que celui-ci ne fut pas fini et que l'implémentation de la compatibilité Android n'a jamais été pleinement réalisée, il possède néanmoins certaines fonctionnalités techniques intéressantes.

Pour résumer l'objectif de départ, l'idée était de réaliser un jeu mobile inspiré de l'oeuvre des **"Escalier de Penrose"** réalisée par M. Escher. Il en va sans dire que la première difficulté a été de revisiter ce concept dans une idée qui n'avait pas encore été exploré : celle de la répétition de manière instancière des escaliers. 

Pour expliquer plus clairement, l'objectif du jeu était de proposer un jeu d'énigme dans un monde formées d'instances du même terrain, tout ce qui arrivait à un terrain, arrivant aux autres instances. 

***

# Travail de programmation

Ce projet a été pour moi un nouveau défi, en parti par l'utilisation de Shaders ainsi que des Scriptables Objects. Utilisation que je vais détailler plus en détail ci-dessous : 

## Shader et Stencil Buffer

L'utilisation de Shaders et plus particulièrement des Stencil Buffer fut très pratique dans le cadre de ce projet. En effet, j'avais pour objectif de créer une "loupe" qui permettait de regarder au travers et de voir des objets invisibles le reste du temps. Pour faire simple, des rayons sont émis par un objet "master" (Buffer Read) qui vont rebondir sur les objets marqués "client" (Buffer Write). Ce rebond permet alors de renvoyer l'image de l'objet, et par conséquent, de le voir à travers le master qui lui est équipé d'un "material" transparent. L'effet final peut donc ressembler à celui ci-dessous : 

![shaderDemo](/assets/images/shaderDemo.gif)

Et ci-dessous se trouve les codes relatifs au BufferR et BufferW (pour Read and Write)

BufferR : 

![ShaderBufferR](https://user-images.githubusercontent.com/114059469/200172035-054633b6-d313-40d1-98f3-964a59501c57.png)

BufferW :
 
![ShaderBufferW](https://user-images.githubusercontent.com/114059469/200172040-dd774511-b883-4a2e-a02e-d3a4ab67b6ce.png)

## Scriptable Object 

La deuxième problématique qui était aussi liée au fonctionnement du jeu, était l'utilisation de Scriptable Object afin d'obtenir un mouvement synchronisé des briques du puzzle, comme le montre l'image ci-dessous : 

![scriptableDemo](/assets/images/scriptableDemo.gif)

La méthode de fonctionnement de cette mécanique est également assez simple puisqu'elle consiste en deux types de blocs; un bloc "Master" et un bloc "Slave". Le bloc Master est déterminé par le joueur. Il peut en effet choisir de bouger n'importe quel bloc attaché à l'instance de base du monde. Le bloc Master envoie ensuite chaque mouvement local qu'il effectue comme une donnée au sein du scriptable object. Lorsqu'une donnée est mise à jour dans ce même scriptable object, les blocs "slave" vont alors lire la donnée et appliquer ce mouvement sur eux-même en local. 

# Suite du projet

Ce projet n'aura pas de suite et restera clos. Il a par ailleurs été décidé de rendre open source son code, aussi, je me ferais une joie de vous aider si une partie de celui-ci vous intéresse.