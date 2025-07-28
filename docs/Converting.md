# Converting

Fields `DetailsPanel`:

![](./img/ConstructorConverting0.png ':size=20%')

`Constructor Converting`:

- `Merge to One Mesh` - Button. Merge all meshes into one. (`PWCAnimation` works only with separate meshes).
- `Save as StaticMesh` - Button. Save the structure as a StaticMesh asset. (Path: Game/Generated/...)

Message about saving and opening `Content Browser` at the link:

![](./img/SaveAsStaticMesh1.jpg ':size=50%')

> If you need to replace the current object with a saved `StaticMesh` - use the `Replace Selected Actors with` function: Right-click on the active object to open the context menu and select: `Replace Selected Actors with` -> `SM_ObjectName` -> `StaticMesh`. It is important that the desired `StaticMesh` asset is selected in the `ContentBrowser`. Result: `StaticMeshActor` with the installed `StaticMesh` asset and the old name.

![](./img/ReplaceActorsWith0.png ':size=50%')
