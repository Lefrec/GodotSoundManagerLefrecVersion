# Other Features

## Accessing Buses

You can get every audio type dedicated bus index with these functions :

```cs
SoundManager.get_master_index()
SoundManager.get_sound_effects_index()
SoundManager.get_ui_sounds_index()
SoundManager.get_ambient_sounds_index()
SoundManager.get_music_index()
```

## Custom Buses

You can also change which buses the different audio types use if you want :

```cs
SoundManager.set_sound_effects_bus("SFX")
SoundManager.set_ui_sounds_bus("UI")
SoundManager.set_ambient_sound_bus("Ambient")
SoundManager.set_music_bus("Track")
```

Additionaly, you may have noticed that every play function have an `override_bus : String` argument. Passing an audio bus name here will make the player play the audio on the given bus instead of its default one.

## Process Modes

The Sound Manager sets different process modes for reliability:

- **Sound Effects**: `PROCESS_MODE_PAUSABLE` - pauses with game
- **UI Sounds**: `PROCESS_MODE_ALWAYS` - always plays
- **Ambient Sounds**: `PROCESS_MODE_ALWAYS` - always plays
- **Music**: `PROCESS_MODE_ALWAYS` - always plays

You can change those directly in `sound_manager.gd`'s `_init()`.

Functions to change process mode throught script may appear in the future.
