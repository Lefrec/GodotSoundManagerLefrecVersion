# Ambient Sounds

Ambient sounds are background environmental audio that can fade in and out smoothly. They're designed for things like wind, rain, crowd noise, or other atmospheric effects.

Pass an argument as `fade_in_duration` or `fade_out_duration` to define how long the fade transition should take in seconds.

- `SoundManager.play_ambient_sound(resource: AudioStream, fade_in_duration: float = 0.0, override_bus: String = "") -> AudioStreamPlayer`

Play the given audio stream on the ambient sounds bus.

Return the `AudioStreamPlayer` that will play the sound so you can access it easily to change its volume, pitch, etc.

- `SoundManager.stop_ambient_sound(resource: AudioStream, fade_out_duration: float = 0.0) -> void`

Stop any ambient sounds player that is currently playing the given audio stream.

- `SoundManager.stop_all_ambient_sounds(fade_out_duration: float = 0.0) -> void`

Stop any ambient sounds player that is currently playing.


## Notes

- Ambient sounds won't play again if they're already playing
- Multiple ambient sounds can play simultaneously
- Fading uses smooth transitions for natural sound changes
- Ambient sounds use a pool of 2 players by default
