# Конвертация

Поля `DetailsPanel`:

![](../img/ConstructorConverting0.png ':size=20%')

`Constructor Converting`:

- `Merge to One Mesh` - Кнопка. Обьединить все меши в один. (`PWCAnimation` работает только с отдельными мешами).
- `Save as StaticMesh` - Кнопка. Сохранение конструкции как StaticMesh ассет. (Путь: Game/Generated/...)

Сообщение о сохранении и открытие `Content Browser` по ссылке:

![](../img/SaveAsStaticMesh1.jpg ':size=50%')

> Если требуется заменить текущий обьект на сохранённый `StaticMesh` - воспользоваться функцией `Replace Selected Actors with`: На активном обьекте правым кликом вызывается контекстное меню и выбирается: `Replace Selected Actors with` -> `SM_ObjectName` -> `StaticMesh`. Важно, чтоб в `ContentBrowser` был выбран нужный `StaticMesh` ассет. Результат: `StaticMeshActor` с установленным `StaticMesh` ассетом и старым именем.

![](../img/ReplaceActorsWith0.png ':size=50%')
