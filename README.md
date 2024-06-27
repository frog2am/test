<div align="center">

<br/>

<img src="logo_color.png" width="520px" />

<br />
<br />

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fdevcheeze%2Fnotiffy&count_bg=%231679AB&title_bg=%23555555&icon=github.svg&icon_color=%23FFFFFF&title=Hits&edge_flat=false)](https://github.com/frog2am/test) [![NPM Downloads](https://img.shields.io/npm/dt/swiper.svg?style=flat&label=NPM Download)]() [![Last Commit](https://img.shields.io/github/last-commit/frog2am/test.svg?style=flat&label=Last Commit)]() [![License](https://img.shields.io/npm/l/idm-ipex-ui.svg?style=flat&label=License)]()
[![NPM](https://nodei.co/npm/swiper.png?downloads=true)](https://www.npmjs.com/package/notiffy)

</div>

<br />

# 👋 Overview

"Notiffy" is a TypeScript-based notification message UI.
<br />
Modern design created using pure CSS makes it accessible for everyone to learn and apply.
<br />
Customization is possible through provided properties and supports vanilla JavaScript as well as TypeScript.
<br/>
Supports all frameworks and platforms that use JavaScript, such as React, Vue.js, and JSP.
<br />
Promises regular debugging and continuous updates.
<br />
Below are the core features provided by default.
<br />

1. <b>Platform Independent</b>
   No extra installations for dependencies.

2. <b>Four Types Available</b>
   Provides "Slip", "Mole", and "Alert" types for various uses besides the "Toast".

3. <b>Varient Events</b>
   Event-based callback triggers can be utilized.

4. <b>Most browsers Supported</b>
   Supports major browsers such as Chrome, Edge, Firefox and Safari.

5. <b>Automatically Responsive Size</b>
   Delivers reactive type CSS automatically for tablet and mobile devices.

6. <b>MIT License</b>
   It is free to use because it follows the MIT license.

<br />
<br />

1. <b>Platform Independent</b>
   No extra installations for dependencies.
   <br />

2. <b>Four Types Available</b>
   Provides "Slip", "Mole", and "Alert" types for various uses besides the "Toast".
   <br />

3. <b>Varient Events</b>
   Event-based callback triggers can be utilized.
   <br />

4. <b>Most browsers Supported</b>
   Supports major browsers such as Chrome, Edge, Firefox and Safari.
   <br />

5. <b>Automatically Responsive Size</b>
   Delivers reactive type CSS automatically for tablet and mobile devices.
   <br />
6. <b>MIT License</b>
   It is free to use because it follows the MIT license.

<br />
<br />

# ⚠️ Usage Cautions

Global CSS may affect DIV, SVG and Path tags.
<br />
TypeScript is optional with minimal dependencies required for module building.
<br />
In case of using Node.js, it is advisable to opt for version 18.12.0 or newer. (if possible)

<br />
<br />

# 📥 Installation

Select one of the following methods to add "Notiffy" to your project.
<br />

- When using NPM.
  <br />

```shell
$ npm install notiffy
```

<br />

- When using YARN.
  <br />

```shell
$ yarn add notiffy
```

<br />

- When grab from CDN. (latest version)
  <br />

```html
<!-- latest version... -->
<script src="https://cdn.jsdelivr.net/npm/notiffy/dist/index.js"></script>

<!-- if wanting specific version... -->
<script src="https://cdn.jsdelivr.net/npm/notiffy@1.0.0/dist/index.js"></script>
```

<br />
<br />

# ⚡ Quick Start

- Declare module imports.
  <br />

```javascript
import { Toast, Slip, Mole, Alert } from 'notiffy';

// if using CommonJS...
const { Toast, Slip, Mole, Alert } = require('notiffy');

// If grab the CDN...
const { Toast, Slip, Mole, Alert } = notiffy;
```

<br />

- When using "Toast" example.
  <br />

```javascript
Toast.warning({ text: 'hello toast.' });
```

<br />
<br />

# 💡 How To Apply

- HTML example using CDN.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="https://cdn.jsdelivr.net/npm/notiffy/dist/index.js"></script>
    <title>Example</title>
  </head>
  <body>
    <button id="button">Toast Popup</button>
  </body>
  <script>
    document.getElementById('button').addEventListener('click', function () {
      const { Toast } = notiffy;
      Toast.warning({ text: 'clicked the button' });
    });
  </script>
</html>
```

<br />

- Functional React example using an imported module. (for reference)

```typescript
import { Toast } from 'notiffy';

export const Example = (): JSX.Element => {
  const onClickButton = (): void => {
    Toast.waring({ text: 'clicked the button' });
  };

  return (
    <div>
      <button onClick={onClickButton}></button>
    </div>
  );
};
```

<br />
<br />

# 🔗 More Infomation

- [Click Here](https://devcheeze.github.io/notiffy/) for document and examples.
- [Click Here](mailto:devcheeze@icloud.com) to send feedback to the creator by email.
