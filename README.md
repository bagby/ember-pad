# Ember-pad [![Build Status](https://travis-ci.org/topaxi/ember-pad.svg?branch=master)](https://travis-ci.org/topaxi/ember-pad)

This README outlines the details of collaborating on this Ember addon.

## Addon Installation

* `ember install ember-pad`

## Addon usage

As util function

```javascript
import { padStart } from 'ember-pad/utils/pad'
import { padEnd   } from 'ember-pad/utils/pad'

console.log(padStart(5, 2))        // '05'
console.log(padStart('a', 5, ' ')) // '    a'

console.log(padEnd(5, 2))        // '500'
console.log(padEnd('a', 5, ' ')) // 'a    '
```

As handlebars helper

```handlebars
<input type="text" value={{pad-start value 2}}>
<input type="text" value={{pad-end value 2}}>
```

As template literal function:

```javascript
import { padStartTpl } from 'ember-pad/utils/pad'

console.log(padStartTpl`${4}:${2}`(2)) // '04:02'
// OR
console.log(padStartTpl(2)`${4}:${2}`) // '04:02'
```

## Installation

* `git clone` this repository
* `npm install`
* `bower install`

## Running

* `ember server`
* Visit your app at http://localhost:4200.

## Running Tests

* `npm test` (Runs `ember try:testall` to test your addon against multiple Ember versions)
* `ember test`
* `ember test --server`

## Building

* `ember build`

For more information on using ember-cli, visit [http://www.ember-cli.com/](http://www.ember-cli.com/).
