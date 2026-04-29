# Music

The music system handles background music with crossfading, pausing, resuming, and track history.

It uses 2 audio players to achieve smooth transitions between tracks but only one music should play at a time.

## Playing Music

- `SoundManager.play_music(resource: AudioStream) -> AudioStreamPlayer`

Stop currently playing music if any and play the given audio stream on the music bus.

- `SoundManager.play_music(resource: AudioStream, position: float = 0.0, volume: float = 1.0, crossfade_duration: float = 0.0, override_bus: String = "") -> AudioStreamPlayer`

You can define the starting time, player volume and crossfade duration if needed.

## Controlling Playback

- `SoundManager.pause_music(resource: AudioStream = null) -> void`

Pause all playing music players or only the first one playing the resource if an audio stream is given.

- `SoundManager.resume_music(resource: AudioStream = null) -> void`

Resume all playing music players or only the first one playing the resource if an audio stream is given.

- `SoundManager.stop_music(fade_out_duration: float = 0.0) -> void`

Stop all playing music players.

## Checking Status

- `SoundManager.is_music_playing(resource: AudioStream = null) -> bool`

Return `true` if a music player is playing.

If a resource is given, only return `true` if a music player is playing the given audio stream.

- `SoundManager.is_music_track_playing(resource_path: String) -> bool`

Return `true` if a music player is playing an audio stream with the given `ressource_path`.

- `SoundManager.get_currently_playing_music() -> Array[AudioStream]`

Get a list of the audio streams being played by music players.

- `SoundManager.get_currently_playing_music_tracks() -> PackedStringArray`

Get a list of the audio streams' ressource path being played by music players.

## Track History

- `SoundManager.get_music_track_history() -> PackedStringArray`

Get a list of the last 50 audio streams' ressource path that were played by music players.

- `SoundManager.get_last_played_music_track() -> String`

Get the last played audio stream's ressource path played by a music player.
