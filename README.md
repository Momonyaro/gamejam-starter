# What's the big idea?!
Well, if you want to participate in a game jam, but are maybe sighing at all the time you might have to spend making regular old boilerplate. This is one of _a thousand_ solutions to that problem.

The repo isn't that important in of itself, instead just take the starter_kit folder and place it inside your godot project folder.

## Some features provided
* [AUTOLOAD] Saving/Loading (supports multiple save slots)
* [AUTOLOAD] Scene Transitions (a simple fade-to-black is provided but simple to mod)
* [AUTOLOAD] Level Management (allows you to define scenes for main menu, levels, game over and a win-screen)
* [AUTOLOAD] SFX player (supports both global sounds for UI and also positional audio for 2D)
* ObjectPooler component allows for simple pooling of scenes that are commonly spawned like bullets.
* CameraShake2D component that uses offsets to provide easy to "juice" functions to make gameplay more explosive.
* A basic main menu, start game button (that uses the level-management) and level select.

## How to set up
Drop the starter_kit folder into your project and you're most of the way there.
Four autoloads need to also be added if you don't use the repo project.godot file:
  * Levels - res://starter_kit/level_utils/levels_autoload.gd
  * Save - res://starter_kit/save_utils/save_autoload.gd
  * SFX - res://starter_kit/audio_utils/sfx_autoload.tscn
  * Transition - res://starter_kit/scene_utils/transition_autoload.tscn

In order to use the SFX and Levels autoloads you also need to create two resources.
You can either create these and place them in the project root:
  * res://sfx_library.tres - AudioLibraryResource for the SFX autoload to keep track of available sound effects
  * res//game_layout.tres - GameLayoutResource for the Levels autoload to know the scene structure in-game

Another alternative is to define project settings that allow you to place these resources elsewhere in the project:
  * "application/resources/game_layout" should be a string pointing to the file path
  * "application/resources/sfx_library" should be a string pointing to the file path

## So it's NOT plug-and-play?
Nope, not right now. It kind of is if you instead just use the entire starter-kit repo as a jumping off point. We already have everything set up for testing so why not make use of it?
Other than that, no, you will need to set some stuff up but most of the regular components like CameraShake2D will work even if you choose to delete most other systems.
Cause yes, if there is extra functionality that you don't need. Delete it and then just fix the rare issues that might occur.
