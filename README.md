# msa-edition
MySimpleApp component to perform WYSIWYG edition.

## CLIENT API

The following code is available by importing the corresponding web component:
```html
<!-- Example -->
<link rel="import" href="../msa-edition/msa-edition-mover.html"></link>
```

### Function: MsaEdition.makeMovable
From: `msa-edition-mover.html`

Make a DOM element movable by user.

![Example](/doc/mover.png)

```javascript
// Example
MsaEdition.makeResizable("#move_me") // div is now movable
MsaEdition.makeResizable("#move_me", false) // div is not movable anymore
```

* __MsaEdition.makeMovable__: `Function(target [, movable])`
  * __*target__: `DOM Element` or `String`
    * if `DOM Element` : target that is made movable.
    * if `String` : CSS selector query from which the targets are deduced.
  * __movable__: `Boolean`, determines if the target is movable or not (default: true).

### Function: MsaEdition.makeResizable
From: `msa-edition-resizer.html`

Make a DOM element resizable by user.

![Example](/doc/resizer.png)

```javascript
// Example
MsaEdition.makeResizable("#resize_me") // div is now resizable
MsaEdition.makeResizable("#resize_me", false) // div is not resizable anymore
```

* __MsaEdition.makeMovable__: `Function(target [, resizable, args])`
  * __*target__: `DOM Element` or `String`
    * if `DOM Element` : target that is made resizable.
    * if `String` : CSS selector query from which the targets are deduced.
  * __resizable__: `Boolean`, determines if the target is resizable or not (default: true).
  * __args__: `Object`
    * __updateTargetPosition__: `Boolean`, set target position to relative. This hack allows to reduce some buggy behaviour with resizer handles positioning (default: true).

### Function: MsaEdition.popupFlexItemMenuFor
From: `msa-edition-flex-item-menu.html`

Popup a menu to manage a DOM Element position and size, in flex positioning context.

![Example](/doc/flex-item-menu-popup.png)

```
// Example
MsaEdition.popupFlexItemMenuFor("#my_div")
```

* __MsaEdition.popupFlexItemMenuFor__: `Function(target)`
  * __*target__: `DOM Element` or `String`
    * if `DOM Element` : target that is managed by popup.
    * if `String` : CSS selector query from which the target is deduced.
