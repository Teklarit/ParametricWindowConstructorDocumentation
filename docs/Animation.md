# Animation

!> Animation is only available on geometry that is not merged into 1 mesh!

`PWCAnimationComponent` - component that allows you to activate 4 basic type animations of the doors.

To use, add the `PWCAnimationComponent` component to the `SimpleWindowConstructor` or `SimpleDoorConstructor` actor. Example for an object at the level: In the active actor panel, `Details` -> `Add` -> `PWCAnimation`.

![](./img/AddAnimationComponent1.png ':size=40%')

It is possible to change the animation time for the handle `Handle Animation Time` and the door opening `Hinge Animation Time`.

![](./img/AddAnimationComponent2.png ':size=30%')

Calling the animation is available through the Blueprint function `RunAnimation` in `PWCAnimationComponent`.

!> The function is called on the user side where it is needed. In the Sequencer, or PlayerController.

![](./img/AddAnimationComponent3.png ':size=30%')

Parameters:
- `NewOpenAction` - Opening or closing animation (`Open`, `Close`).
- `NewOpenAxis` - Opening animation to the side or from the top (`RightLeft`, `UpDown`).
- `Reset` - Ignore current/last animation, show full animation.
 
> If the "Open from top" animation is called, and the current animation is "Open from side", the closing animation is automatically turned on, and then the opening animation in the desired direction.
