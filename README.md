[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/arsnebula/nebula-dialog)
[![Polymer Version](https://img.shields.io/badge/polymer-v2-blue.svg)](https://www.polymer-project.org)
[![Sauce Labs Build Status](https://img.shields.io/badge/saucelabs-passing-red.svg)](https://saucelabs.com/beta/builds/4bfb5db522544eb1b9550cb35eed6e3e)
[![Gitter Chat](https://badges.gitter.im/org.png)](https://gitter.im/arsnebula/webcomponents)
[![Become a Patreon](https://img.shields.io/badge/patreon-support_us-orange.svg)](https://www.patreon.com/arsnebula)

# \<nebula-dialog\>

A web component to display modal dialogs.

* Fixed position full-screen overlay with a backdrop and centered layout
* Built-in animation
* Declare a dialog in markup, or use the included behavior/stylesheet to build your own
* Easily styled with style attributes or with CSS variables and mixins

> Warning: This element requires browser support for [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise). To ensure support by all browsers, use a promise polyfill such as [PolymerLabs Promise Polyfill](https://github.com/PolymerLabs/promise-polyfill).

## Installation

```sh
$ bower install -S arsnebula/nebula-dialog
```

## Getting Started

Import the package.

```html
<link rel="import" href="/bower_components/nebula-loader/nebula-dialog.html"> 
```

To define a custom dialog with markup, use the `nebula-dialog` element.

```html
<nebula-dialog
  opened="{{opened}}"
  result="{{result}}"
  on-opened="_onOpened"
  on-closed="_onClosed">
</nebula-dialog>
```

To create a custom dialog element, use the `nebula-dialog-behavior` and `nebula-dialog-styles` building blocks.

```html
<dom-module id="my-dialog">
  <template>
    <style include="nebula-dialog-styles"></style>
    <slot></slot>
  </template >
  <script>
    class MyDialog extends Nebula.DialogBehavior(Polymer.Element) {
      static get is() { return 'my-dialog' }
    }
    customElements.define(MyDialog.is, MyDialog)
  </script>
</dom-module>
```

*For more information, see the API documentation.*

## Contributing

We welcome and appreciate feedback from the community. Here are a few ways that you can show your appreciation for this package:

* Give us a **Star on GitHub** from either [webcomponents.org](https://www.webcomponents.org/element/arsnebula/nebula-element-mixin) or directly on [GitHub](https://github.com/arsnebula/nebula-element-mixin).

* Submit a feature request, or a defect report on the [Issues List](https://www.webcomponents.org/element/arsnebula/nebula-element-mixin/issues).

* Become a [Patreon](https://www.patreon.com/arsnebula). It takes a lot of time and effort to develop, document, test and support the elements in our [Nebula Essentials](https://www.webcomponents.org/collection/arsnebula/nebula-essentials) collection. Your financial contribution will help ensure that our entire collection continues to grow and improve.

If you are a developer, and are interested in making a code contribution, consider opening an issue first to describe the change, and discuss with the core repository maintainers. Once you are ready, prepare a pull request:

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Change Log

See [CHANGELOG](/CHANGELOG.md)

## License

See [LICENSE](/LICENSE.md)