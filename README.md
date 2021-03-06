#  Basic Cross-Platorm Keychain Access for Node.js 

  This module adds methods for basic Keychain access in Node.js **This is in-development and is not feature complete.**
  
  For MAC only support check out the xkeychain npm module (https://github.com/drudge/node-keychain).

## Requirements

 * Mac OS X 10.6+
 * Windows XP or higher
 * Ubuntu Linux (uses GNOME keyring).

## Installation

    npm install xkeychain
    
## Example

```javascript
var keychain = require('keychain');

keychain.setPassword({ account: 'foo', service: 'FooBar', password: 'baz' }, function(err) {
  keychain.getPassword({ account: 'foo', service: 'FooBar' }, function(err, pass) {
    console.log('Password is', pass);
    // Prints: Password is baz
  });
});
```

## Contributors

This module was originally implemented by Nicholas Penree ([drudge](http://github.com/drudge)) as node-keychain. This module focuses on OS X while this one focuses on supporting multiple OSes at once.

The following are the major contributors of `node-xkeychain` (in no specific order).

  * Michael Vooorhaen ([mvhaen](http://github.com/mvhaen))

## License 

(The MIT License)

Copyright (c) 2011 Nicholas Penree &lt;nick@penree.com&gt;

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
