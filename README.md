# Easy BEM class name generator

> Simple and fast [BEM](https://en.bem.info/) class names generator.

[![NPM](https://img.shields.io/npm/v/easy-bem.svg)](https://www.npmjs.com/package/easy-bem)


Fork of [bem-cn-fast](https://github.com/GREENpoint/bem-cn-fast) that uses another delimiters (personally I like them more):

- The element name is separated from the block name by a double underscore (`__`)
- The modifier name is separated from the block or element name by a double dash (`--`)
- The modifier value is separated from the modifier name by a single underscore (`_`)

## Install

```bash
npm install --save easy-bem
```

```bash
yarn add easy-bem
```

## Usage

```javascript
import bem from 'easy-bem';
const b = bem('block');

b(); // -> 'block'
b('element'); // -> 'block__element'
b({ mod1: true, mod2: 'some-value' }); // -> 'block--mod1 block--mod2_some-value'
b('element', { mod1: true }); // -> 'block__element--mod1'
```
