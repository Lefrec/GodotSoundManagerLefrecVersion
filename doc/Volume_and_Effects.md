# Volume and Effects

You can control the **volume** and **audio effects** of buses throught script thanks to dedicated functions.

Since they are general functions you need to pass a bus index as an argument that you can find using [these functions](./Other_Features.md#accessing-buses).

## Volume Control

Volume should always be set as a linear float value between `0.0` and `1.0`.

- `SoundManager.get_volume(bus_index: int) -> float`

Get the linear volume of the given bus.

- `SoundManager.set_volume(bus_index: int, volume: float) -> void`

Set the linear volume of the given bus to volume.

- `SoundManager.get_mute(bus_index: int) -> bool`

Get the value of mute on the given bus.

- `SoundManager.set_mute(bus_index: int, enabled: bool) -> void`

Set the value of mute to enabled on the given bus.

## Audio Effects

These functions allow you to interact with `AudioEffect` on buses.

- `SoundManager.get_effect(bus_index: int, effect_index: int) -> AudioEffect`

Get the effect on the given bus at the given index.

- `SoundManager.get_effects(bus_index: int) -> Array[AudioEffect]`

Get an array of every effect on the given bus.

- `SoundManager.add_effect(bus_index: int, effect: AudioEffect, index : int = -1) -> void`

Add the effect to the given bus, you can specify the index you want to position the effect at.

- `SoundManager.set_effect(bus_index: int, effect_index: int, enabled: bool) -> void`

Set the effect at the given index on the given bus to enabled.

- `SoundManager.remove_effect(bus_index: int, effect_index: int) -> void`

Remove the effect at the given index on the given bus.

- `SoundManager.clear_effects(bus_index: int) -> void`

Remove every effect on the given bus.
