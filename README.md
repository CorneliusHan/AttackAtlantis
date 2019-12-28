# team11

# Attack Atlantus
CPSC 427 team11

# MINIMAL PLAYABILITY GAME SUBMISSION

## Comparison to our proposed development plan

The following is our proposed plan for the past two weeks with comments:
# Week: November 1
* UI: Start screen interface
* Enemy AI:
* Charge and fast dash momentum
* Advanced pathing
* Boss AI
* Able to use generated abilities of characters
* Basic pathing
# Week: November 8 – Playability
* UX tutorial levels, introduction to ability learning and enemies encountered
* Add more levels

# Playable Game Report: AttackAlantus (Week November 1st)
Summary of work completed:
* Game levels: the game now has 10 different levels to play with. The difficulty of the game gets more difficult as the game goes on.
* World refactor: refactor the world in order to add levels
* Main menu improvement: the main menu can now handle mouse events
* Ability improvement: abilities are now activated by left click
* Score system improment: scores are calculated based on enemy types
* DefaultTexture selection transition: added transition for going between levels, going to the main menu, and going to the level selection UI
* DefaultTexture Selection UI: user can select different levels in this page or go back to the main menu using a new UI.
* Victory/Defeat UI: when a level is won, the user can choose to go to the next level, go back to level selection, or retry. When a level is lost, the user can choose to go back to level selection, or retry.
* Improved state machine and decision tree: more states and switching logic.
* Improved animation: death animations for all entities, new sprites for enemies.
* Improved efficiency: cache texture loading rather than loading it every time.
* Sound system: hit sounds, ability sounds, death sounds
* Boss character: add a new boss character. It has new animations, abilities, physics, and AI. It appears in levels 5 and 10.
* DefaultTexture content: different backgrounds, terrians, enemy types, and maybe a boss in each level.



## Installation
Within the team11 directory:
```
mkdir build; cd build;
CMAKE ../ -DCMAKE_BUILD_TYPE=Release
make
./attackAtlantus
```

## Controls
- WASD Keys to move
- Spacebar to attack
- Mouse for ability direction and mouse left click for ability activation
## Story
Deep in the ocean, something horrible has emerged: the forces of Atlantis are waging war upon humanity. Once a lowly beach bum, you are forced to fight through hordes of sea monsters in order to defend your home. The game will have around 5 - 10 stages (levels). In order for the player to clear all stages, the player needs to defeat all minions and boss(es) to pick up the key to unlock the next stage. 
## Core game design elements
## Rendering
The background for the game will be rendered as a stationary top-down 2D plane. We plan to vary the background image when we create different stages. There will be five main types of entities that need to be rendered: 
The player
An enemy
An item/skill
Obstacles
Projectiles
## Assets (geometry, sprites, audio, etc.)
We plan to use sprites for most of our graphical assets. We plan to have simple animations for abilities. For audio, we would like simple, pleasant, battle music, sounds for dealing/taking damage, death sounds, and ability pickup sounds.
## 2D geometry manipulation (transformation, collisions, etc.)
We will have translations for each entity listed in the rendering section. There will be many collision checks, as we need to check for touching enemies, projectiles, and items. Additionally, we would like to implement various space transformations as items.
## Gameplay logic/AI
The core gameplay will be surviving as enemies periodically spawn from specified locations and attempt to attack the player. There will be various items/power-ups spawning in random locations, forcing the player to make strategic decisions regarding whether they should risk trying to go pick up the item, and when they should use the item once it’s picked up. The enemies will have a basic AI, following the player and trying to kill them. Different types of enemies may have different AIs; some will shoot projectiles while others may have erratic movement. After surviving a certain period of time, the player will need to defeat a boss in order to complete the stage.
## Physics
We will have basic projectile physics. We are also likely to rely on physics for certain abilities, for example, a weapon that moves in curves or an ability pushing/pulling enemies in certain directions.


## Reference:
    Sound: Willlewis, Abyssmal, ethanchase7744 and jalastram from freesound.org and gg from https://www.myinstants.com/instant/gg/
           NeoSpica, 89o, Michel88, Christopherderp, rhodesmas, LittleRobotSoundFactory, sheyvan, Robinhood76, UsuarioLeal
    Boomerang: https://opengameart.org/content/boomerang-bullet
    Meteor: https://imgbin.com/png/kz89Xz1Z/computer-icons-meteoroid-png
## License
[MIT](https://choosealicense.com/licenses/mit/)
