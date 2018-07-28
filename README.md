# Pickaxe

> ...

## Draft

This is the draft specification of a shell game engine that'll be written in Go. I hope to collect my thoughts here until it can layout a clear minimum viably architecture from which I can derive the code necessary to run it. No deadline is given and it'll likely be fruitless.

## Motivation

I want a rogue-like shell MMORPG inspired by the MUDs of yore.

## The Game

Not sure yet but maybe think Ultima Online in the terminal.

## The Engine

The engine should be able to produce shell games in general, but be specially able in making online games and RPGs. Although that is the ultimate goal it'll start small. Really small. Let's try writing something on the screen.

### Architecture

The code won't reflect it right away but eventually I want a human friendly object oriented design that is easy to grasp. Bellow I'll list the objects, types, behavior and relationships that comes to mind. I'll refine and refute ideas later down the line.

<dl>
  <dt>Game</dt>
  <dd>The game controller that holds everything together. It should handle the initialization, the game loop, the user input, the scene management and the wind down of the program.</dd>
  <dt>Scene</dt>
  <dd>A scene is a context, a group of entities and behaviors that area contextually linked, like the "main menu", the "intro". the "gameplay", the "pause menu", a "dialogue", etc. Multiple scenes can be active at any given time.</dd>
  <dt>Entity</dt>
  <dd>An entity is a piece of logic that might have a visual representation on the screen. The player is an entity, so is an item, an NPC, but so is a timer, a light source, an environmental effect, or even a fragment of the interface.</dd>
</dl>
