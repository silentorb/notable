---
tags: [Game]
title: Marloth world generation
created: '2023-12-08T16:13:58.966Z'
modified: '2023-12-08T16:20:47.048Z'
---

# Marloth world generation

## Generation Requirements

### Comprehensive

#### Rules

* Generation solutions must be easily and practically comprehended by their creator
* There should be no room for surprises
* Generation solutions should not need monkey patches for fringe cases—there should be no fringe cases

#### Motivation

* Incomprehensible world generation solutions result in an effectively infinite amount of fringe cases, bugs, and whack-a-mole fixes

### General to Specific

#### Rules

* Generation solutions should transition from general models to specific models
* Generation solutions should not transition from specific models to general models
* The transitions must be seamless

#### Motivation

* Relying on a single layer of scope results in very limited generation
* When transitioning from general to specific, the system can have tremendous control on both layers, but when transitioning from specific to general, most control of the general is lost and what little remaining control becomes a series of hacks (jiggering specific configuration details so that they indirectly cause the desired general effects)

### No Backing up

#### Rules

* Generation solutions should never try an operation and then undo that operation
* Instead, generation solutions should rely on algorithms and preplanning so that there is never a need to back up

#### Motivation

* Any use of backing up quickly leads to incomprehensible side-effects

### Order to Chaos

* Generation solutions should never attempt to tame chaos
* Any chaos within a generation solution must be controlled
* Chaos can be introduced to ordered data in order to embellish that data as long as the chaos is tightly bounded

#### Motivation

* Chaos begets chaos, never order

### No Cleaning up data

#### Rules

* Intermediate steps of a generation solution should not generate data that requires further mutation before it is acceptable
* Generated data should be immediately useable on point of generation
* Any mutation of data should only be used to enhance and embellish already useable data

#### Motivation

* Data that requires cleanup is inherently chaotic and incomprehensible

### Multi-Model

#### Rules

* Generation solutions should not rely on a one-size-fits-all model for generation data
* Instead, multiple models should be used and translated between
* To some degree, each layer of the generation process ([General to Specific](#general-to-specific)) should use a different model
* High level (general) level data models should support any number of specific sub-models within different sections of the world

#### Motivation

* Using a single model results in very limited world generation
* Any attempt to perform advanced world generation with a single model will snap the model and cause endless failures

### Traversable

#### Rules

* Player characters should be able to walk from any essential world element to any other essential world element

#### Motivation

* Unlike games like Minecraft, this game will not provide players with a means to terraform their way through incongruent terrain

### Simple Traversal

#### Rules

* Traversal should not employ ladders, elevators, or teleporters

#### Motivation

* Ladders and elevators are more complicated to support for AI
* Ladders and elevators increase the amount of potential physical fringe cases and glitches
  * Many 3D games that employ ladders and elevators carefully place them in restricted locations in order to limit these issues
* Teleporters break spatial continuity
* Teleporters bypass the wonder of following winding corridors and arriving at an unexpected place

#### Notes

* An exception may eventually be made for teleporters

### Easy Lookups

#### Rules

* Each model should easily support looking up what world elements exists around any given point in 3D space

#### Motivation

* Without Easy lookups, the generation solution easily gets lost and quickly gets bogged down in trying to reason about the world around a particular point

### Easy Navigation

#### Rules

* Each model should support easy navigation from one world element to the next in any spatial direction

#### Motivation

* Without Easy navigation, the generation solution easily gets lost and quickly gets bogged down in trying to reason about the world around a particular point

### Clear Element Integration

#### Rules

* Each model should support clear and straightforward integration between the various elements of a world
* This includes:
  * A clear sense of space ownership between elements (which section of space is owned by which element)
  * A clear sense of how neighboring elements relate and connect

#### Motivation

* Without Easy navigation, the generation solution easily gets lost and quickly gets bogged down in trying to reason about the world around a particular point

### Strong Verticality

#### Rules

* The generated world should have frequent and dramatic variations in floor height

#### Motivation

* Flat levels are boring

### Room-over-room

#### Rules

* Generation solutions should support traversable rooms-over-rooms

#### Motivation

* While DOOM II continues to demonstrate how much can be accomplished without room-over-room, supporting room-over-room allows for so many more world generation possibilities and is already supported by the underlying game engine

### Minimal right angles

#### Rules

* Generated architecture can contain some right angles but should not depend on them

#### Motivation

* Right angles are boring

### No obvious grid

#### Rules

* To whatever degree that grids are used by the underlying generation methods, the use of those grids should not be obvious to the player

#### Motivation

* Grids weaken any sense of an organic world and kill suspension of disbelief

### Minimal large prefabs

#### Rules

* Use of large prefabs should be minimized

#### Motivation

* At least for me, heavy use of large prefabs is distracting and kills suspension of disbelief

### Complex integration

#### Rules

* The elements of the world should tightly wrap around and integrate with each other

#### Motivation

* Sterile separation of world elements is boring
