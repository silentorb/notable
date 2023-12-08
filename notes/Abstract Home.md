---
tags: [Game]
title: Abstract Home 2
created: '2023-12-08T16:13:58.950Z'
modified: '2023-12-08T16:16:24.681Z'
---

# Abstract Home 2

I'm not going this direction right now but am keeping this article for reference.

The idea here is to remove the spatial home interior and represent it through a GUI instead

* It would still have a 3D home interior background, but the player would no longer navigate it in first person
* The entirety of the home experience would become turn-based (with a few minor race conditions in multiplayer)

## Motivation

* Turn-based is more relaxing than real-time, and the home section of the game is all about being relaxing
* Most of what I've been wanting the player to do in the home lends itself better to a GUI than interacting with a spatial environment
* This approach is easier to develop and will allow me to more quickly add home gameplay features
* It might sound trivial, but a significant part of the cozy tone I'm trying to create requires the player to be sitting down, and sitting down doesn't work well in a first person game
  * Similarly, a significant part of the desired tone is for the player to be drinking tea and eating snacks while performing their other activities, things that are likewise awkward in first person mode but can be more easily nestled into a GUI

## Disadvantages

* This game's design has always had a gap between the home and outside, but this abstract home approach really solidifies that gap and removes most possibility of creating any overlap in the future
  * For example, I've toyed around with the idea of having secret passages within the home
* While for the most part the abstraction lends itself to cozy, there still is something cozy about walking through a cozy 3D room in real time, and that would be missed
* It's possible that this abstraction could feel a little cheap to players, especially in comparison to the more tangible outside world
* It's less immersive
* There's an aspect of menu's with context artwork where I sometimes feel like they are a tease and leave me subtly dissatisfied

## Notes

* This is similar to how some other games work
  * Some real time RPGs switch to a more abstract, turn-based mode when the player enters a shop or tavern
  * While Minecraft doesn't stop the clock when the player is home, players normally spend most of their home time working with GUIs
* In the future if it ever looks like I can effectively replace enough of this functionality with a spatial real-time interior, I'll do it
* The alternative would be more like Minecraft, where the home interior would still have both a spatial layout and different GUI screens while interacting with each furnishing
