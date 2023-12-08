---
tags: [Game]
title: interaction
created: '2023-12-08T16:13:58.966Z'
modified: '2023-12-08T16:15:01.701Z'
---

# Interaction

## Traditional RPG interactions

* Traditional RPG environment interaction involves:
  * The player activating an interaction command with a preconfigured interactable element in the game world
  * Any interaction more elaborate than opening a door or pulling a lever involves a modal UI view

## Problems

> Note: some of these problems only apply to complex interactions, but simple interactions don't scale well and need the option of falling back on complex interactions.  Very few RPGs have been created that only allow simple interactions.  (Even the lightweight Diablo series still features dialog windows and shop screens.)

* Is non-composable, either in terms of input (commands) or output (effects)
  * A single interaction command either does a single completely different thing for each interactable item, or branches into multiple options through a UI dialog
  * This is a brittle design and has been stretched to the snapping point by most advanced RPG
* Is incompatible with the spatial simulation
  * Any integration between the two systems requires bridging and adapters
* Only supports PC-to-NPC (or non-player actor)
  * In general, RPG environment interactions are rarely player-to-player or NPC-to-NPC
  * This limitation has been tripping up any attempts to make Marloth more of a simulation that has a life apart from the player
* Has no observable effect
  * This overlaps with being abstract
  * If two other characters were to engage in dialog, the player could watch but normally would not be able see any meaningful information about what is happening
  * Some games will have audio or floating text for dialog not involving the player, but that approach is brittle and doesn't scale well
    * Usually this is only used during scripted events or for ambience
    * Even then, I've only ever seen that for dialog, nothing else
      * For example, I've never seen a float UI for an NCP browsing the wares of a shopkeeper
* Only supports two actors
  * Some games will have scripted dialog between more than two characters
    * That is uncommon

## Solution options

### Simple Spatial

Limit the game mechanics to what works with simple spatial UI

* This is the safest route
* I've gone this direction several times and I can make it work, especially if I stick more to combat than I would prefer

### Innovative Spatial

Invent a surreal system of representing complex abstract associations in spatial reality

* I've invested some designing toward this, but haven't full explored it yet
* So far, it seems possible but also shows signs of being over-ambitious like most things I pursue

### Traditional RPG

Just go with the standard RPG/Immersive Sim approach and see if I can make it slightly better

### Distinct phases

Have different game phases (minigames)

* This is the Sid Meier's approach to game design

* Some roguelikes are divided into three phases:

  * Management
  * Exploration

  * Combat

## Solution Resolution

### Reduction

* I've tried implementing the traditional RPG direction several times, disliking and steering away from it
* I just don't really like having separate phases
  * In practice this usually ends up being multiple thin games instead of a single dense game, especially when developed by a small team
  * I've never been a big fan of the the mini-game design approach

### Action items

* For now, I'll take a stab at further designing an innovative spatial system
* If that proves impractical, I'll fall back to Simple spatial
