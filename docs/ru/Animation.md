# Анимация

!> Анимация доступна только на не объединённой в 1 меш геометрии!

`PWCAnimationComponent` - компонента, которая позволяет активировать 4 основные анимации створок.

Для использования следует добавить к актору `SimpleWindowConstructor` или `SimpleDoorConstructor` - компоненту `PWCAnimationComponent`. Пример для обьекта на уровне: В панели активного актора `Details` -> `Add` -> `PWCAnimation`.

![](../img/AddAnimationComponent1.png ':size=40%')

Доступно изменение времени анимации для ручки `Handle Animation Time` и открыванеии створки `Hinge Animation Time`.

![](../img/AddAnimationComponent2.png ':size=30%')

Вызов анимации доступен через Blueprint функцию `RunAnimation` в `PWCAnimationComponent`.

!> Вызов функции осуществляется на стороне пользователя там, где ему необходимо. В Sequencer, или PlayerController.

![](../img/AddAnimationComponent3.png ':size=30%')

Параметры:
 - `NewOpenAction` - Анимация открытия или закрытия (`Open`, `Close`).
 - `NewOpenAxis` - Анимация открыть в сторону или сверху (`RightLeft`, `UpDown`).
 - `Reset` - Не учитывать текущую/последнюю анимацию, показать полную анимацию.
 
> Если происходит вызов анимации "Открыть сверху", а текущая анимация "Открыть сбоку" - автоматически включается анимация закрытия и после - открытия в нужном направлении.
