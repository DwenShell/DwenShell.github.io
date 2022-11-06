---
layout: single
title:  "Stolp of Varinye"
toc: true
toc_label: "Table of content"
toc_icon: "cogs"
toc_sticky : true

---

# Commençons pas une présentation

Qu'est-ce que Stolp of Varinye ? 

Il s'agit là de l'ébauche d'un projet réaliser en collaboration avec 2 amis pour validé notre années de L2. Bien que celui-ci ne fut pas finis et que l'implémentation de de la compatibilité Android n'ai jamais été pleinement réalisé, il possède néanmoins certaines fonctionnalité techniques intéressante.

Pour résumer l'objectif de départ, l'idée était de réaliser un jeu mobile inspiré de l'oeuvre des **"Escalier de Penrose"** réalisé par M. Escher. Il en vas sans dire que la première difficulté fus de revisité ce concept dans une idée qui n'avais pas encore été exploré : celle de la répétition de manière instancier des escaliers. 

Pour expliquer plus clairement, l'objectif du jeu était de proposer un jeu d'énigme dans un monde formé d'instance du même terrain, tout ce qui arrivait à un terrain, arrivant aux autres instances. 

***

# Travail de programmation

Ce projet fut pour moi un nouveau défis, en parti par l'utilisation de Shader ainsi que des scriptables objects. Travail que je vais détailler plus en détail ci-dessous : 

## Shader et Stencil Buffer

L'utilisation de Stencil Buffer et plus particulièrement des Stencil Buffer fut très pratique dans le cadre de ce projet. En effet, j'avais pour objectif de créer une "loupe" qui permettait en regardant au travers de voir des objet invisible le reste du temps. Pour faire simple, des rayons sont émis par un objet "master" (Buffer Read) qui vont rebondir sur les objets marqués "client" (Buffer Write). Ce rebond permet alors de renvoyer l'image de l'objet et par conséquent de le voir à travers le "master qui lui est équipé d'un material transparent. L'effet final peut donc ressembler à celui ci-dessous : 

![shaderDemo](/assets/images/shaderDemo.gif)

Et ci-dessous ce trouve les code relatif au BufferR et BufferW (pour Read and Write)

BufferR : 

![ShaderBufferR](https://user-images.githubusercontent.com/114059469/200172035-054633b6-d313-40d1-98f3-964a59501c57.png)

BufferW :
 
![ShaderBufferW](https://user-images.githubusercontent.com/114059469/200172040-dd774511-b883-4a2e-a02e-d3a4ab67b6ce.png)

## Scriptable Object 

La deuxième problématique qui était elle aussi lié au fonctionnement du jeu, était l'utilisation de scriptable Object afin d'obtenir un mouvement synchronisé des briques du puzzle, comme le montre l'image ci-dessous : 

![scriptableDemo](/assets/images/scriptableDemo.gif)

La méthode de fonctionnement de cette mécanique est également assez simple puisqu'elle consiste en deux type de bloc, un bloc "Master" et un bloc "Slave". Le bloc Master est déterminer par le joueur, il peut en effet choisir de bouger n'importe quel bloc attaché à l'instance de base du monde. Le bloc Master envoie ensuite chaque mouvement local qu'il effectue comme une donnée au sein du scriptable object. Lorsqu'une donnée est mise à jour dans ce même scriptable object, les blocs "slave" vont alors lire la donnée et appliqué ce mouvement sur eux-même en local. 

# Suite du projet

Ce projet n'auras pas de suite et resteras clos. Il as par ailleurs été décider de rendre open source son code, aussi, je me ferais une joie de vous aider si une partie de celui-ci vous intéresse. 
