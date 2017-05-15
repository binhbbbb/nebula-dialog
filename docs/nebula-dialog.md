# \<nebula-dialog\>

`<nebula-dialog>` is a web component to display a responsive dialog overlay.

## Import

```html
<link rel="import" href="/bower_components/nebula-loader/nebula-dialog.html"> 
```

## Usage

The following demonstrates common properties and event handlers: 

```html
<nebula-dialog
  id="dialog"
  opened="{{opened}}"
  on-closed="_onClosed"
  on-opened="_onOpened">
  <!-- place content to display here -->
</nebula-dialog>
```

By default, the dialog display is set to `none`. To open the dialog you can set the `opened` property to `true` or `false`. You can also use the `show` method which returns a promise that resolves when the dialog is closed or canceled.

```js
  this.$.dialog.show().then(function(result) {
    console.log('The dialog has been closed', result)
  })
```

## Style

The dialog can be styled using standard CSS properties, and the following variables:

Custom property | Description | Default
:--- | :--- | :---
`--nebula-dialog-backdrop-color` | The background color of the base element. | hsla(0, 0%, 0%, 0.6)
`--nebula-dialog-animation-duration` | The duration of the animation. | 250ms

The element also inherits default values from the following global theme styles. If a global theme variable has not been set, it will use the local default.

Custom property | Description | Default
:--- | :--- | :---
`--nebula-ui-backdrop-color` | The background color of the base element. | hsla(0, 0%, 0%, 0.6)

## API Reference

## Mixins

#### [Nebula.DialogBehavior](nebula-dialog-behavior.md)