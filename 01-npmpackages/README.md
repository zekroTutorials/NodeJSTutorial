# `#01` - NodeJS Installation

> Die Vorgangsweise ist bei Linux und Windows gleich.

---

## Packages erstellen

Zuerst sollte man sich einen Ordner anlegen mit folgender Struktur:

```
MyPackage
    |-- src
         |-- index.js
    |-- test
         |-- test.js
```

Danach kann man mit folgendem Command automatisch die `package.json` erstellen, welche das Package beschreibt:
```
$ npm init
```

Im folgenden Dialog wird man durch die wichtigsten Keys der `package.json` geführt:

```
This utility will walk you through creating a package.json file.
It only covers the most common items, and tries to guess sensible defaults.

See `npm help json` for definitive documentation on these fields
and exactly what they do.

Use `npm install <pkg>` afterwards to install a package and
save it as a dependency in the package.json file.

Press ^C at any time to quit.
package name: (examplepackage) 
version: (1.0.0) 0.1.0
description: This is an example package
entry point: (index.js) src/index.js
test command: node test/test.js
git repository: https://github.com/zekroTutorials/NodeJSTutorial
keywords: test, justatest
author: zekro <contact@zekro.de>
license: (ISC) MIT
About to write to /home/ringo/Desktop/git/NodeJSTutorial/01-npmpackages/examplepackage/package.json:

{
  "name": "examplepackage",
  "version": "0.1.0",
  "description": "This is an example package",
  "main": "src/index.js",
  "scripts": {
    "test": "node test/test.js"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/zekroTutorials/NodeJSTutorial.git"
  },
  "keywords": [
    "test",
    "justatest"
  ],
  "author": "zekro <contact@zekro.de>",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/zekroTutorials/NodeJSTutorial/issues"
  },
  "homepage": "https://github.com/zekroTutorials/NodeJSTutorial#readme"
}


Is this ok? (yes) 
```

Zudem sollten die beiden Keys `dependencies` und `dev-dependencies` hinzugefügt werden, falls das Package auf anderen Packages basieren soll. Weitere Informationen dazu im Videotutorial.

```json
{
  ...
  "dependencies": { 
  },
  "dev-dependencies": { 
  }
}
```

---

## Code

Nun fügen wir etwas Code zu unserem Test-Package hinzu:

> src/index.js
```js
console.log("Testpackage loaded!");
```

> test/test.js
```js
require('../src/index.js');
```

Danach kann man das Package mit folgendem Command testen:
```
$ npm test
> examplepackage@0.1.0 test /home/ringo/Desktop/git/NodeJSTutorial/01-npmpackages/examplepackage
> node test/test.js

Testpackage loaded!
```

---

© 2018 - present  
Ringo Hoffmann (zekro Development)  
zekro.de | contact[at]zekro.de
