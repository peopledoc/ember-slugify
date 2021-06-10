# ember-slugify

[![CircleCI](https://circleci.com/gh/peopledoc/ember-slugify.svg?style=shield&circle-token=106b80d7153b94e6ee96541d1647d8e3984862cd)](https://circleci.com/gh/peopledoc/ember-slugify)

Library to slugify your strings within Ember.

This library uses:

- [speakingurl](https://pid.github.io/speakingurl/)
- [simple-pinyin](https://github.com/xuqingkuang/simple-pinyin)


## Compatibility

* Ember.js v3.16 or above
* Ember CLI v2.13 or above
* Node.js v12 or above

## Installation

```
ember install ember-slugify
```

## Usage

### In a `js` file

```js
import slugify, { removeDiacritics } from 'ember-slugify';

let slug = slugify('你好你怎么样 monsieur'); // ni-hao-ni-zen-me-yang-monsieur

let options = { separator: '#' }); // options for speakingurl
let slug = slugify('你好你怎么样 monsieur', options); // ni#hao#ni#zen#me#yang#monsieur

let noDiacritics = removeDiacritics('Théâtre'); // Theatre
let slug = slugify('Théâtre'); // theatre
```

### In a template

```hbs
await render(hbs`{{slugify '你好你怎么样 monsieur'}}`)
await render(hbs`{{remove-diacritics 'Théâtre'}}`)
```

The separator option is not available on `slugify` helper.

## Contributing

See the [Contributing](CONTRIBUTING.md) guide for details.

## License

This project is licensed under the [MIT License](LICENSE.md).
