# `jm_strands_on_strands`
Create Strand on strands.

This compound needs.

The "Rebel Pack" compounds:
https://area.autodesk.com/learn/assets

MJCG Compounds:
https://mjcg.gumroad.com/

## `Inputs`

### `Enable`
Turn on/off.

### `Enable end points`
Creates orientated points at the end of each strand, which can be used to instance objects on.

### `Enable out points`
Outputs the points used to create the strands. These points can be used to instance objects rather than create strands. The points inherit rotation, colour, and the length setting becomes point_size.


### `In strands`
Connect input strands here.

## `Creation`

### `Strand count`
Number of strands to create.

### `Segments`
Number of segments per strand.

### `Strand length cutoff`
Input strands shorter the this length will not have strands applied to them.

### `Count based on ratio`
Turn on/off count based on ratio.

### `Length ratio`
Length ratio defines the distance between each new strand, if the input strand is shorter than this distance no strands will be created. If the input strand is longer than the length ratio, its length will be divided by the length ratio and the number of output strands will be based on the result.

### `Start strands`
Position along the input strand where the strands will start.

### `Random start port`
Connect an array or field of scalar values to randomise the start position on a per strand basis.

### `End strands`
Position along the input strand where the strands will end.

### `Random end port`
Connect an array or field of scalar values to randomise the end position on a per strand basis.


### `Remove first`
Removes the first strand.

### `Remove last`
Removes the last strand.

### `Stepped`
Alternates the strands on opposite sides of the input strand.

### `Un flip`
Strands are generated along one side of the input strand.

### `Randomise`
Randomise the strands positions along the input strand based on the distance between each strand.

## `Orientation`
These settings expose MJCG's "update_strands_orientations" compound. Please see the info on this node for more information.

## `Length`

### `Overall Strand length`
Fcurve to give the out strands an overall shape.

### `Random length`
Turn on random length settings. The random lengths generated are multiplied onto the overall length.

### `Random length mask`
Fcurve to mask the random length.

### `Random length min`
The minimum random length value to be multiplied.

### `Random length min`
The maximum random length value to be multiplied.

### `Random length seed`
The seed to use for randomization. 

### `Length randomise port`
Connect an array or field of scalar values to randomise the length on a per strand basis. This can be used to grow the output strands.

## `Rotation`

### `Rotation degrees`
The amount of degrees to rotate the output strand around the input strand.

### `Random rotation port`
Connect an array or field of scalar values to randomise the rotation on a per strand basis.

### `Rotate mask`
Fcurve to mask the rotation.

### `Rotate up degrees`
The amount of degrees to rotate the output strand up or down the length of input strand.

### `Random rotate up port`
Connect an array or field of scalar values to randomise the up rotation on a per strand basis.

### `Rotate up mask`
Fcurve to mask the up rotation.

## `Colour`

### `Colour type`

<span style="color:#ffb80f">***Inherit from strand***</span>
<br />Inherit the colour from the input strand.
<br /><span style="color:#ffb80f">***Random overall colour***</span>
<br />Random colour per input strand.
<br /><span style="color:#ffb80f">***Random colour***</span>
<br />Random colour per output strand.
<br /><span style="color:#ffb80f">***Random colour pairs***</span>
<br />Random colour per pair of output strands. 

### `Random colour min`
The minimum random colour value.

### `Random colour min`
The maximum random colour value.

### `Random colour seed`
The seed to use for randomization. 

### `Overall matte`
Fcurve to generate a overall matte ramp for the output strands based on the length of the input strand.This matte can be used in the shader using a aiUserDataColor node with the attribute set to "overall_matte"

### `Strand matte`
Fcurve to generate a  matte ramp for each of the output strands. This matte can be used in the shader using a aiUserDataColor node with the attribute set to "strand_matte"

## `Distort strands`

### `Distort strands`
Turn on/off.

### `First frame only`
If a field is connected it will be sampled only on the first frame. This will stop the strands swimming through the field if moved.
<span style="color:#ff5a00">Do not use if animating on the strands, as it will break the compound.</span>


### `Vector distortion port`
Connect an array or field of vector values to distort the strands on a per strand basis.

### `Distortion mask`
Fcurve to mask the distortion.

## `End points`

### `Set point size to one`
Sets point_size to one. Turn off to have the point_size equal the strand length.


### `Point size multiplier`
Fcurve to multiply the point_size if "set point size to one" is turned off.

### `orientation_axis`
The end points are orientated to point in the direction of the end of the strand. This can be modified using this vector.

## `Inherit properties`
Each point on the output strands will inherit the properties from the construction points.


## `Output`

### `Out Strands`
point position, point normal, point count

### `Orientated end points`
Outputs orientated points at the end of each strand, which can be used to instance objects on.

### `Out points`
Outputs the points used to create the strands. These points can be used to instance objects rather than create strands. The points inherit rotation, colour, and the length setting becomes point_size.




