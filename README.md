# Pickaxe

> ...

## Draft

This is the draft specification of a shell game engine that'll be written in Go. I hope to collect my thoughts here until it can layout a clear minimum viably architecture from which I can derive the code necessary to run it. No deadline is given and it'll likely be fruitless, but hopefully I'll pick a few things along the way.

## Motivation

I want to learn about game development and I've always wanted a rogue-like shell MMORPG inspired by the MUDs of yore.

## The Game

Not sure yet but maybe think Ultima Online with graphics of Ultima I-IV.

## The Engine

The engine should be able to produce shell games in general, but be specially able in making online games and RPGs. Although that is the ultimate goal it'll start small. Really small. Let's try writing something on the screen.

### Architecture

The code won't reflect it right away but eventually I want a human friendly object oriented design that is easy to grasp. Bellow I'll list the objects, types, behavior and relationships that comes to mind. I'll refine and refute ideas later down the line.

<dl>
  <dt>Game</dt>
  <dd>The game controller that holds everything together. It should handle the initialization, the game loop, user input, scene management and the wind down of the program.</dd>
  <dt>Entity</dt>
  <dd>An entity is a piece of logic that can have a visual representation. The player is an entity, and so is an item, or an NPC, but so is a timer, a light source, an environmental effect, an interface control, etc.</dd>
  <dt>Tile</dt>
  <dd>A cell in the grid of the game world. Dirt, grass, water, a segment of a road, a wall, a door, etc.</dd>
  <dt>World</dt>
  <dd>The game world is where tiles and entities are laid out on a plane giving them position, direction, speed, etc. in relation to each other, allowing for physical interaction.</dd>
  <dt>Scene</dt>
  <dd>A scene is a configuration of the screen, a series of entities such as cameras and interface controls that are contextually linked, so the game knows what to render. e.g. the main menu, the gameplay, a dialogue, etc.
  <dt>Camera</dt>
  <dd>A slice of game world so it can been seen. Cameras are added to a Scene and more than one can exist at the same time.</dd>
  <dd>...</dd>
</dl>
