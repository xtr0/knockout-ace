# knockout-ace

Knockout bindings for the ACE embeddable code editor (using brace)

[![NPM version](https://badge.fury.io/js/knockout-ace.png)](http://badge.fury.io/js/knockout-ace)

## Installation

    npm install knockout-ace

N.B. This module peer depends on `brace` and `knockout`.  It will fail to install if you are not using the same version of knockout and brace as this module.  You will need to require in whichever themes and modes you want from brace (see [brace documentation](https://github.com/thlorenz/brace))

## Example

To use, simply use the `ace` data binding:

```html
<div data-bind="ace: sourceText, aceOptions: { mode: 'sql', theme: 'textmate' }"></div>
```

```javascript
var ko = require('knockout');
require('knockout-ace');
require('brace/theme/textmate');
require('brace/mode/sql');

ko.applyBindings({
  sourceText: 'SELECT * FROM aceModes'
});
```

## License

  MIT