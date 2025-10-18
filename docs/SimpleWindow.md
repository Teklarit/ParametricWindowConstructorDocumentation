# Simple Windows and Doors

`PWCSimpleWindow` и `PWCSimpleDoor` - classes for quick construction of simple windows and doors. Filling restrictions: from 1 to 3 rows (vertical filling) with different filling coefficients. Then in each row an arbitrary number of cells with glass or sash (horizontal filling).

> The difference between `PWCSimpleWindow` and `PWCSimpleDoor`: in `PWCSimpleWindow` we configure the filling in the frame, in `PWCSimpleDoor` we configure the filling in the main sash.

![](./img/SimpleConstructor1.png ':size=50%')

![](./img/SimpleConstructor2.jpg ':size=50%')

## `DetailsPanel`:

### `Constructor Live Refresh`

![](./img/ConstructorLiveRefresh0.png ':size=20%')

- `Refresh` - Button. Generate/update geometry.
- `Live Refresh` - Enable/disable automatic geometry rebuilding when infill data changes.

### Filling

![](./img/SimpleConstructor0.png ':size=20%')

- `Main Door Data`: (only for `PWCSimpleDoor`)
	- `Sash Side` - Sash side.
	- `Open Angle Type` - Set the type and angle of opening (used for the current display, for converting in the desired form into a single mesh).
	- `Angle Left Right` - Set the current angle of opening to the side. (0 - 120, degrees).
	- `Angle Up Down` - Set the current angle of opening down. (0 - 10, degrees).
- `Filling`
	-  `Override Materials` - On/off the list of materials that will be applied to the geometry of the structure instead of the base materials.
	- `Width` - The width of the structure.
	- `Height` - The height of the structure.
	- `Rows Count` - The number of rows in the structure. From 1 to 3. (vertical filling).
	- `Row Weight` - Fill factor (The higher the value, the greater the ratio of the cell height to the total height).
	- `Row Filling` - Array with data that will fill the row (horizontal filling).
		- `Filling Type` - Cell type (glass, sash).
		- `Fill Weight` - Cell fill factor in a row.
		- `Glazing Type` - Glazing type (triple glazing, opaque panel).
		- `Add Mosquito Net` - On/off mosquito net.
		- `Sash Side` - Sash side.
		- `Open Angle Type` - Set the type and angle of opening (used for the current display, for converting in the desired form into a single mesh).
		- `Angle Left Right` - Set the current angle of opening to the side. (0 - 120, degrees).
		- `Angle Up Down` - Set the current angle of opening down. (0 - 10, degrees).
		
> Some fields are hidden/shown depending on the type of infill and other related parameters.

### Inside Sill and Outside Sill

Any type of sill can be installed on either side of the window.

- `Inside Sill` - (facing the interior). Axis: `-X`.
- `Outside Sill` - (facing the exterior). Axis: `+X`.

> Some fields are hidden/shown depending on the type of infill and other related parameters.

- `Inside Sill` or `Outside Sill`:
	- `Add Sill` - On/off window sill.
	- `Indoor Outdoor Type` - Construction type (Indoor Sill (Interior) or Outdoor Sill (Exterior)).
	- `Indoor Sill Type` - Type/model of interior sill.
	- `Outdoor Sill Type` - Type/model of exterior sill.
	- `Sill Depth` - Window sill depth (cm). 
	- `Sill Extra Width` - Additional window sill width (cm) (+ or - to the width of the construction).
	- `Sill Origin Offset` - Move the window sill along the local axes: X - forward, Y - right, Z - up. (If `Sill Extra Width` = 20, then `Sill Origin Offset Y` = 10 or -10 (half) to align with the desired side).
	- `Sill Angle` - Outside Sill angle (0-45) (degrees).
