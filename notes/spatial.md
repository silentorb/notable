---
tags: [Game]
title: spatial
created: '2023-12-08T16:13:58.966Z'
modified: '2023-12-08T16:15:01.743Z'
---

# Spatial

## Nested state

### Problems

* Nested state has inherent UI/UX problems
* Nested state is problematic in abstract UIs
* Nested state is even more problematic for 2D spatial UIs
* Nested state is even, even more problematic in first person 3D spatial UIs where element distance can vary and player view can be obstructed

### Solution

> Note: This solution is accidentally applied far more than people realize

* Keep actor state simple
* What would normally be nested state is instead represented as separate actors
  * These actors can be treated as loosely-coupled children of the root actor
* Unlike a nested state UI, the secondary actor approach cleanly integrates with the spatial world and other actors, both visually and in simulation interactions

## Physical manifestation of internals

* One idea I have had but not seriously considered is to have different locations in the map represent the internal state of different characters
* It would be like stepping inside their head
* I would allow the player to view state internals in a graphic manner, and interact with those internals

## Translating abstract UI

### Overview

* Similar to how I was able to extract the essence of turn-based combat and translate some of that to real-time combat, maybe I can extract some of the essence of abstract UIs and apply it to a spatial world
* For this exercise I am not interested in analyzing game UIs, which leads to a stilted echo chamber, but instead want to focus on reviewing best practices of productivity apps
  * In particular, focusing less on the narrow field of game UI and instead on the broader and more refined field of information architecture

### CRUD

* UIs largely involve reading and writing data (Creation, Reading, Updating, and Deletion)
* The data can largely be partitioned into individual records
* As with most processing, CRUDs are roughly composed of 90% reading and 10% writing
* CRUDs work best when they are divided into specialized views and don't try to cram too much functionality into a single view
* There is usually much overlap between creation and updating views
* Deletion does not usually need a dedicated view
* That leaves two main types of views, read views and write views
* Sometimes reading and writing are combined into the same view, but that can be messy
* Similar to OS file systems, CRUD read views are split into two types, list views and record views
  * List views are like directories, and record views are like single files
* This list and record structure translates well to relational databases
* A crucial ingredient of cruds is having logical relationships between records, and a smooth flow between related records
  * The user should be able to naturally navigate from one view to related views, based on the relational data schema
* This relates to node graphs: how the elements of a system relate to each other

### Node graphs

* I love node graphs

* The pathing of the world forms a node graph
* One of the issues I have been wrestling with is trying to get the Winding Path algorithm to create a clear sense of nodes and edges
  * Winding Path does not naturally distinguish between nodes and edges
* If the world generation leveraged node graphs more, that would help support the Physical manifestation idea
  * Different world nodes (locations) could be associated with different characters

## Requirements

* Most or all state is visually represented in 3D space
* Most or all state changes are visually represented in 3D space
* At least some of the visuals feel creative, as though the player is creating a work of art by causing certain effects
* Atomic, modal actors

