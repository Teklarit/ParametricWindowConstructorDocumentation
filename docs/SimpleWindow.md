# Simple Windows and Doors

## Base classes

- `PWCSimpleWindowConstructor` - a class for quickly generating windows with infills. Infill: 1 to 3 rows (vertical). A row can be filled with any number of elements (glass or sash) (horizontal).
- `PWCSimpleDoorConstructor` - a class for quickly generating doors with infills. Unlike `PWCSimpleWindowConstructor`, the infill starts at the sash.
- `PWCThreeCorneredWindowConstructor` - a triangle window. No infill, adjustable width, height, and vertex position.

Searching and placing objects at the level:

![](./img/SimpleConstructor1.png ':size=50%')

![](./img/SimpleConstructor2.jpg ':size=50%')

## `DetailsPanel`:

### `Constructor Live Refresh`

![](./img/ConstructorLiveRefresh0.png ':size=20%')

- `Refresh` - Button. Generate/update geometry.
- `Live Refresh` - Enable/disable automatic geometry rebuilding when infill data changes.

### `Object Settings`

- `Geometry Quality` - `HIGHT`/`LOW` - geometry detalization (profile and other elements).
- `Glass Planes Generation Type` - `All Planes` - generate all planes for glass, `First And Last Only` - generate only the first and last planes for glass.
- `Handle Type` - Select a handle model.
-  `Override Materials` - On/Off the list of materials that will be applied to the geometry of the structure instead of the base materials.

### `Filling`

![](./img/SimpleConstructor0.png ':size=20%')

- `Main Door Data`: (only for `PWCSimpleDoor`)
	- `Sash Side` - Sash side.
	- `Open Angle Type` - Set the type and angle of opening (used for the current display, for converting in the desired form into a single mesh).
	- `Angle Left Right` - Set the current angle of opening to the side. (0 - 120, degrees).
	- `Angle Up Down` - Set the current angle of opening down. (0 - 10, degrees).
- `Filling`
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

### `Inside Sill and Outside Sill`

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
