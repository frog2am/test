<div align="center">

<br/>

<img src="logo.png" width="560px" />

<br />
<br />

[![Latest Version](https://img.shields.io/npm/v/notiffy.svg?style=social&label=Latest Version)]() [![Bundle Size](https://img.shields.io/bundlephobia/min/notiffy.svg?style=social&label=Bundle Size)]() [![GitHub Issues](https://img.shields.io/github/issues/devcheeze/notiffy.svg?style=social&label=GitHub Issues)]() [![Supported Node](https://img.shields.io/node/v/notiffy.svg?style=social&label=Supported Node.js)]()

</div>

<br />

## Synopsis

indicatoring module is a spinner for response waiting.
<br />
it is simple, easy to use, and customizable through set some arguments.
<br />
circular indicators can be added or removed at want locations.
<br />
also, it has various uses beyond waiting for data responses.
<br />
provides both package installation and a CDN.
<br />

```html
<!-- latest version -->
<script src="https://cdn.jsdelivr.net/npm/indicatoring/dist/index.js"></script>

<!-- X.X.X version -->
<script src="https://cdn.jsdelivr.net/npm/indicatoring@1.0.0/dist/index.js"></script>
```

<br/>
<br/>

## Preview

![Preivew](preview.gif)

<br/>
<br/>

## Cautions

use Indicatoring.open() to begin and Indicatoring.close() to finish.
<br />
to prevent flickering, the Indicator does not run if Indicatoring.close() is called within 300 milliseconds of Indicatoring.open().
<br />
if the limit arguments is used, Indicatoring.close() can be omitted.

<br />
<br />

## Examples

available in all JavaScript libraries and frameworks

<details>
<summary>
Common (Importing Module)
</summary>

```javascript
import Indicatoring from 'indicatoring';
// or
const Indicatoring = require('indicatoring');
```

</details>

<details>
<summary>
Vanilla JS
</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <script src="http://132.226.23.243:9900/indicatoring/dist/index.js"></script>
  </head>
  <body>
    <div>
      <button onclick="handleRequest()">Click here</button>
    </div>
  </body>
  <script>
    async function handleRequest() {
      Indicatoring.open(); // run while waiting for a response
      fetch('https://api.github.com/users/devcheeze')
        .then((response) => {
          // process response data...
        })
        .catch((error) => {
          // process response error...
        })
        .finally(() => {
          Indicatoring.close(); // required if no limit arguments.
        });
    }
  </script>
</html>
```

</details>

<details>
<summary>
React
</summary>

```javascript
import React from 'react';
import Indicatoring from 'indicatoring';

class App extends React.Component {
  handleRequest = async () => {
    Indicatoring.open(); // run while waiting for a response
    fetch('https://api.github.com/repos/devcheeze/indicatoring')
      .then((response) => {
        // process response data...
      })
      .catch((error) => {
        // process response error...
      })
      .finally(() => {
        Indicatoring.close(); // required if no limit.
      });
  };

  render() {
    return (
      <div>
        <button onClick={this.handleRequest}>Click here</button>
      </div>
    );
  }
}

export default App;
```

</details>

<details>
<summary>
Vue.js
</summary>

```javascript
<template>
  <div>
    <button @click="handleRequest">Click here</button>
  </div>
</template>

<script>
export default {
  methods: {
    async handleRequest() {
      Indicatoring.open(); // run while waiting for a response
      fetch('https://api.github.com/repos/devcheeze/indicatoring')
        .then((response) => {
          // process response data...
        })
        .catch((error) => {
          // process response error...
        })
        .finally(() => {
          Indicatoring.close(); // required if no limit.
        });
    },
  },
};
</script>

<style></style>
```

</details>

<details>
<summary>
Angular
</summary>

```javascript
import { Component } from '@angular/core';
import Indicatoring from 'indicatoring';

@Component({
  selector: 'app-root',
  template: `
    <div>
      <button (click)="handleRequest()">Click here</button>
    </div>
  `,
})
export class AppComponent {
  handleRequest() {
    Indicatoring.open(); // run while waiting for a response
    fetch('https://api.github.com/repos/devcheeze/indicatoring')
      .then((response) => {
        // process response data...
      })
      .catch((error) => {
        // process response error...
      })
      .finally(() => {
        Indicatoring.close(); // required if no limit.
      });
  }
}
```

</details>

<br />
<br />

## Arguments

| Argument | Object Name | Key Name | Type                           | Default Value        |
| -------- | ----------- | -------- | ------------------------------ | -------------------- |
| limit    | -           | -        | Number                         | 0                    |
| config   | background  | color    | String                         | "rgba(0, 0, 0, 0.6)" |
|          |             | blur     | Boolean                        | false                |
|          | circle      | color    | "large" or "medium" or "small" | "medium"             |
|          |             | size     | String                         | "#ffffff"            |

all arguments are optional and apply arguments as shown below.
<br />
arguments will continue to be added.

```javascript
Indicatoring.open(
  4000, // indicating duration of 4 seconds.
  {
    background: {
      color: 'rgba(20, 20, 20, 0.4)', // change background color.
      blur: true, // background blur or not
    },
    circle: {
      color: '#f1f2f3', // circular icon color
      size: 'large', // circular icon size
    },
  }
);
```

<br/>
<br/>

## ETC

- [Github Repository](https://devcheeze.github.io/indicatoring)
- [NPM Repository](https://www.npmjs.com/package/indicatoring)
- [YARN Repository](https://yarnpkg.com/package?name=indicatoring)

- [Creator Github Repository](https://github.com/devcheeze)
- [Send Feedback Email To Creator](mailto:devcheeze@icloud.com)
