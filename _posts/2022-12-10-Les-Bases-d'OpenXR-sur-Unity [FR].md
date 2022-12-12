---
layout: single
title:  "[WIP] Les Bases d'OpenXR avec Unity [FR]"
toc: true
toc_label: "Table of content"
toc_icon: "cogs"
toc_sticky : true

---

#Introduction à Open XR

Il convient de commencer ce post par une petite explication de ce qu'est Open XR, comment j'en ais entendu parler et où j'en suis actuellement dans la découverte de ce packages proposer sur Unity par la Unity Team elle-même. 

##Qu'est-ce que c'est, Open XR ?

OpenXR est un standard en Open Source permettant la compatibilité de multiples casque de RV avec une seule et même interface. Ce qui signifie qu'à moins d'avoir des besoins spécifique lié à une fonction d'un type de casque. Tout le code réaliser avec les fonctions d'Open XR seras compatibles sur des casques comme Meta Quest, HoloLens, Pico etc. Ce standard permet donc un vrai gains de temps évitant les multiples versions d'un même produit en fonction du casque utiliser.

J'ai commencé l'utilisation de celui-ci dernièrement pour deux projets réalisé en cours, l'un ne portant pas de nom de se présentant comme une expériences interactif que je vais vous détailler plus bas, et un autre nommé "Red Clamp" qui lui se présente sous la forme d'un rail shooter, projet que je vais également vous détailler plus bas.
##Utilisation d'Open XR

Je ne vais pas vous faire ici une présentation de l'installation détaillés d'Open XR ainsi que de sa mise en place dans la mesure où plusieurs tutoriel très intérrésant l'expliquerons surement bien mieux que moi, je vous invite nottament à suivre la suite de tuto nommé "How to Make a VR Game in Unity 2022" proposé par "Valem Tutorials" et qui m'as personnellement permis d'appliquer Open XR à mes projets. 

#Application au sein de projet
##Expérience VR
Le premier projet sur lequel j'ai utliser Open XR est une expérience intéractive qui se veut réfléxive sur notre place dans le monde. En effet, au sein de celle-ci vous allez vous retrouver plongé dans une usine avec du travail à la chaine à fabriquer des casques de RV à la chaine; le tout avec une musique entétante et une simple action répétitive. Je me permet de vous montrer quelques exemples ci-dessous par le biais de screenshot. 
![vrExpScreen01](/assets/images/vrExpScreen01.png)
![vrExpScreen02](/assets/images/vrExpScreen02.png)
Je vous ajouterais prochainement une vidéo qui permet de vraiment se rendre compte de l'ambiance qui est installer, ambiance assez déstabilisante une fois tout les paramètres réunis. 

##Red Clamp
![redClampLogo02](/assets/images/redClampLogo02.png)
RedClamp est donc en toute logique le deuxième projet sur lequel j'ai commencé à travailler en VR. Ce projet étant toujours en développement, je ne ferais ici qu'une présentation sommaire, il auras en effet le droit à un post à part entière dans le futur puisque certaines mécanique présente au sein de celui-ci mérite d'y porter une certaine attention. 

Pour vous le présenter rapidement, le jeu porte sur l'aventure d'un crabe gangster qui veut se faire respecter dans la nouvelle ville dans laquelle lui et son partenaire arrive. Pour se faire, ils décident de faire un tour en voiture et de simplement annihiler le cartel présent localement pour montrer qui commande à présent.
![redClampLogo01](/assets/images/redClampLogo01.png)

Red Clamp promet donc des combats avec diverses armes et des enemies varier que j'aurais le plaisir de vous décrire dans un post futur. 