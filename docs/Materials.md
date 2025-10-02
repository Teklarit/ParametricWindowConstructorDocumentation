# Materials

After conversion, UV values ​​are recalculated (box projection, size - 100 cm).

Some basic materials are available in the plugin (for the profile: `M_PWC_Plastic_SimpleWhite`, `M_PWC_Plastic_Graphite`, `M_PWC_Wood_Walnut`).

## Assigning custom materials

To assign custom materials to geometry, enable the OverrideMaterialsData option:

![](./img/OverrideMaterialsData.png ':size=40%')

Next, a list of material slots will be available:

![](./img/MaterialsSlots.png ':size=40%')

## Pattern direction by profile

An example of a pattern by profile can be found in the `M_PWC_Wood_Walnut` material.

The control is implemented using ColorData information in geometry attributes (red channel). Usage in the material:

![](./img/UVSwap.png ':size=40%')
