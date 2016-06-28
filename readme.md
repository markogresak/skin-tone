# skin-tone [![Build Status](https://travis-ci.org/sindresorhus/skin-tone.svg?branch=master)](https://travis-ci.org/sindresorhus/skin-tone)

> Change the skin tone of an emoji 👌👌🏻👌🏼👌🏽👌🏾👌🏿

The [Fitzpatrick scale](https://en.wikipedia.org/wiki/Fitzpatrick_scale#Unicode) is used to specify skin tones for emoji characters which represent humans.


## Install

```
$ npm install --save skin-tone
```


## Usage

```js
const skinTone = require('skin-tone');

skinTone('👍', skinTone.BROWN); // or skinTone('👍', 4);
//=> '👍🏾'

skinTone('👍', skinTone.WHITE); // or skinTone('👍', 1);
//=> '👍🏻'

// can also remove skin tone
skinTone('👍🏾', skinTone.NONE); // or skinTone('👍🏾', 0);
//=> '👍'

// just passes it through when not supported
skinTone('🦄', skinTone.DARK_BROWN); // or skinTone('🦄', 5);
//=> '🦄'
```


## API

### Skin tone color name constants

- `skinTone.NONE = 0`
- `skinTone.WHITE = 1`
- `skinTone.CREAM_WHITE = 2`
- `skinTone.LIGHT_BROWN = 3`
- `skinTone.BROWN = 4`
- `skinTone.DARK_BROWN = 5`

### skinTone(emoji, type)

#### emoji

Type: `string`

Emoji to modify.

#### type

Type: `number`<br>
Values:

- `skinTone.NONE` / `0`: None
- `skinTone.WHITE` / `1`: 🏻 White        *(Fitzpatrick Type-1–2)*
- `skinTone.CREAM_WHITE` / `2`: 🏼 Cream white  *(Fitzpatrick Type-3)*
- `skinTone.LIGHT_BROWN` / `3`: 🏽 Light brown  *(Fitzpatrick Type-4)*
- `skinTone.BROWN` / `4`: 🏾 Brown        *(Fitzpatrick Type-5)*
- `skinTone.DARK_BROWN` / `5`: 🏿 Dark brown   *(Fitzpatrick Type-6)*


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
