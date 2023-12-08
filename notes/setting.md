---
tags: [Game]
title: setting
created: '2023-12-08T16:13:58.966Z'
modified: '2023-12-08T16:15:01.736Z'
---

# Setting

## Locations

### City

### Forest

### House

## Cozy

### Themes

#### Creativity

#### Eating

#### Entry

#### Fellowship

#### Food Preparation

#### Sleeping

| Room               | Theme            | Privacy | Neighbors                |
| ------------------ | ---------------- | ------- | ------------------------ |
| Bedroom            | Sleeping         | High    | Study?                   |
| Dining room        | Eating           | Low     | Kitchen, Living room     |
| Entryway           | Entry            | Low     | Living room              |
| Kitchen            | Food Preparation | Medium  | Dining room, Living room |
| Living room        | Fellowship       | Low     | Dining room, Kitchen     |
| Study / Craft room | Creativity       | Medium  | Kitchen, Bedroom?        |

### With Living Room



``` mermaid
flowchart
	entry(Entryway)
	dining(Dining Room)
	kitchen(Kitchen)
	bedroom(Bedroom)
	living(Living room)
	study(Study)
	hall(Hall)
	
	dining --- living
	kitchen --- dining
	kitchen --- living
	entry --- living
	living --- hall
	dining --- hall
	hall --- study
	hall --- bedroom
	
```

### Without Living Room

``` mermaid
flowchart
	entry(Entryway)
    dining(Dining Room)
	kitchen(Kitchen)
	bedroom(Bedroom)
	study(Study)
	hall(Hall)
	
	kitchen --- dining
	entry --- dining

	kitchen --- hall
	dining --- hall
	hall --- study
	hall --- bedroom
	
