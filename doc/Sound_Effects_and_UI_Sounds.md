# Sound Effects and UI Sounds

**Sound effects** and **UI sounds** are short audio clips that can play simultaneously. The Sound Manager maintains a pool of 8 audio players for each by default.

They work the same way under the hood but they are separated into two categories and each have their own bus as **sound effects** usually represent diegetic sounds and **UI sounds** extra diegetic sounds so it can be useful to treat them separately.

## Playing sounds

- `SoundManager.play_sound_effect(ressource : AudioStream, override_bus: String = "") -> AudioStreamPlayer`

Play the given audio stream on the sound effects bus.

- `SoundManager.play_ui_sound(resource: AudioStream, override_bus: String = "")`

Play the given audio stream on the UI sounds bus.

These functions return the `AudioStreamPlayer` that will play the sound so you can access it easily to change its volume, pitch, etc.

## Stopping sounds

- `SoundManager.stop_sound_effect(resource: AudioStream) -> void`

Stop any sound effect player that is currently playing the given audio stream.

- `SoundManager.stop_ui_sound(resource: AudioStream) -> void`

Stop any ui sound player that is currently playing the given audio stream.

## Notes

- Sound effects and UI sounds automatically stop when finished playing
- The pool reuses players to avoid creating too many nodes
- If all players are busy, new sounds will create a new temporary player
