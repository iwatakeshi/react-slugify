# react-slugify


[![Build Status](https://img.shields.io/circleci/project/github/martpie/react-slugify.svg)](https://circleci.com/gh/martpie/react-slugify)
[![Dependencies](https://david-dm.org/martpie/react-slugify.svg)](https://github.com/martpie/react-slugify)

Slugify a React node

## Usage

###  `slugify(node[, options])`

- `node` String, Number, Fragment, Array of nodes
- `options` Object (optional)
  - `delimiter` String (default is `'-'`)
  - `prefix` String (default is `''`)

## Examples

```tsx
import slugify from 'react-slugify';

slugify('something I want to test');
// -> "something-i-want-to-test"

slugify(<span>Yes it works like that too</span>);
// -> "yes-it-works-like-that-too"

slugify(
  <>
    <span>and</span>
    <span>with</span>
    <span>fragments or arrays</span>
  </>
);
// -> "and-with-fragments-or-arrays"

slugify(
  <h3>Crème brulée receipe</h3>,
  { delimiter: '_' }
);
// -> creme_brulee_receipe

slugify(
  <h3>Crème brulée receipe</h3>,
  { prefix: 'user-content' }
);
// -> user-content-creme-brulee-receipe


slugify(
  <h3>Crème brulée receipe</h3>,
  { delimiter: '_', prefix: 'user-content' }
);
// -> user-content_creme_brulee_receipe
```
