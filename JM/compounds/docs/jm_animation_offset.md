## `jm_animation_offset`


<br />Builds an array of animation offsets.
<br />Example at the default settings: 
<br />(0,-.1,-.2,-.3,-.4,-.5.......)

## `Inputs`

### `size`
Size of the array of offsets to build.

### `Start`
Start number to begin the offset.
<br />Negative numbers can be thought of as a frame offset.
<br /> -10  would be a 10 frame offset with the clamp min set to 0.

### `Step`
The size of the increment to build.

### `Clamp min`
Every number below this number will be clamped to this input.

### `Clamp max`
Every number above this number will be clamped to this input.

### `Frame`
connect the time nodes frame output here. This is used to add to the offset over time.

### `Time multiply`
At the default clamp setting, numbers between 0 - 1 will control the speed of the animation.
