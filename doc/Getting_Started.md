# Getting Started

## Installation

- Copy the `addons/sound_manager` directory from this repository into your project's `res://addons/` directory.
- Enable **SoundManager - Lefrec version** in **Project** → **Project Settings**.
- Access the `SoundManager` singleton anywhere in your project.

## Overview

This Sound Manager provides a simple way to handle audio in your Godot projects. It manages different types of audio through separate buses :

- [**Sound effects**](./Sound_Effects_and_UI_Sounds.md)
- [**UI sounds**](./Sound_Effects_and_UI_Sounds.md)
- [**Ambient sounds**](./Ambient_Sounds.md)
- [**Music**](./Music.md)

Different types of sound have slightly different logic and set of features.

## Basic Usage

Get a reference to an `AudioStream` throught `preload()`, `@export`, etc.

```cs
var boom = preload("res://sounds/boom.wav")
var click = preload("res://sounds/click.wav")
var wind = preload("res://sounds/wind.wav")
var song = preload("res://sounds/song.wav")
```

### Playing sounds

```cs
SoundManager.play_sound_effect(boom)
SoundManager.play_ui_sound(click)
SoundManager.play_ambient_sound(wind)
SoundManager.play_music(song)
```

### Stopping sounds

```cs
SoundManager.stop_sound_effect(boom)
SoundManager.stop_ui_sound(click)
SoundManager.stop_all_ambient_sound()
SoundManager.stop_music()
```

Check the dedicated page for each audio type to see what are their specific features.

## Controlling buses

You can adjust **volume** and add **effects** to buses through script thanks to dedicated functions.

[more about volume and effects](./Volume_and_Effects.md)

You can also change the default bus of each sound type if you want or override the bus used for a single audio stream.

[more about changing and overriding buses](./Other_Features.md)
