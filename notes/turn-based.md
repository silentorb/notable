---
tags: [Game]
title: turn-based
created: '2023-12-08T16:13:58.966Z'
modified: '2023-12-08T16:15:01.768Z'
---

# Turn Based

## Overview

* For many years I have played around with the idea of the Marloth game revolving around a cycle where the player interacts with the world, returns home to sleep, the world is updated, and then the player steps out into the updated world and sees what has changed
  * In essence, the player and the world are taking turns
  * Some effects of the player and the world are still immediate
    * What are or aren't is still fuzzy to me
* I'm not sure why I've never fully run with this direction
  * I can't recall ever thinking it was a *bad* idea
  * Possibly I've had a subconscious aversion because this would work best as a foundational feature and I've been hesitant to build on a foundation I've never seen before
    * Not that that's every stopped me with other personal projects...
    * I guess Dark Souls does do this to a lesser degree, and is probably one of the subconscious inspirations for the idea
* The main purpose of this document is to define the idea and help weigh whether to seriously pursue it

## Advantages

Here are the advantages to this turn-based approach:

1. It provides an inexpensive way to integrate diverse and complex narrative logic
2. It relies heavily on implication (and I love implication)
3. It lends itself well to strategy (something that is normally hard to inject into most video games, especially real-time games)
4. It lends itself well to the cozy-horror style I'm trying to establish, where the dangerous world is real-time and the turn-based aspect takes place when you are home
5. It lends itself well to spatial reality—potentially a lot can be communicated through discreet changes in spatial reality
6. This is related to many of the earlier points but is worth specifying—this approach is possibly the most effective solution I've ever seen for marrying turn-based and real-time gameplay

## Disadvantages

Here are the disadvantages to this turn-based approach:

1. There is ambiguity between its deferred effects and immediate effects
2. It is very game defining—if I run with this feature it will be a primary feature
3. It has little precedent and will require extra trial and error
4. It is a little awkward with multiplayer (though still possible—all of the players will need to sleep at the same time)

