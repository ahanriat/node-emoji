# node-emoji

[![NPM version (1.0.3)](https://img.shields.io/npm/v/node-emoji.svg?style=flat-square)](https://www.npmjs.com/package/node-emoji) [![NPM Downloads](https://img.shields.io/npm/dm/node-emoji.svg?style=flat-square)](https://www.npmjs.com/package/node-emoji) [![Build Status](https://img.shields.io/travis/omnidan/node-emoji/master.svg?style=flat-square)](https://travis-ci.org/omnidan/node-emoji) [![Dependencies](https://img.shields.io/david/omnidan/node-emoji.svg?style=flat-square)](https://david-dm.org/omnidan/node-emoji) [![Code Climate](https://img.shields.io/codeclimate/github/omnidan/node-emoji.svg?style=flat-square)](https://codeclimate.com/github/omnidan/node-emoji)

_simple emoji support for node.js projects_

![node-emoji example](http://i.imgur.com/RgFj97V.png) 

## Installation
To install `node-emoji`, you need [node.js](http://nodejs.org/) and [npm](https://github.com/npm/npm#super-easy-install). :rocket:

Once you have that set-up, just run `npm install --save node-emoji` in your project directory. :ship:

You're now ready to use emoji in your node projects! Awesome! :metal:

## Using the class
```javascript
var emoji = require('node-emoji');
console.log(emoji.get('coffee')); // returns the emoji code for coffee (displays emoji on terminals that support it)
console.log(emoji.which(emoji.get('coffee'))); // returns coffee
console.log(emoji.get(':fast_forward:')); // also supports github flavored markdown emoji (http://www.emoji-cheat-sheet.com/)
console.log(emoji.emojify('I :heart: :coffee:!')); // replaces all :emoji: with the actual emoji, in this case: returns "I ❤️ ☕️!"
```

## Using the object
```javascript
var emoji = require('node-emoji').emoji;
console.log(emoji.coffee); // returns the emoji code for coffee (displays emoji on terminals that support it)
console.log(emoji.fast_forward); // returns the emoji code for fast_forward (displays emoji on terminals that support it)
```

## Adding new emoji
Emoji come from js-emoji (Thanks a lot :thumbsup:). You can get a JSON file with all emoji here: https://github.com/omnidan/node-emoji/blob/master/lib/emoji.json

To update the list or add custom emoji, clone this repository and put them into `lib/emojifile.js`.
Then run `npm run-script emojiparse` in the project directory or `node emojiparse` in the lib directory.
This should generate the new emoji.json file and output `Done.`.

That's all, you now have more emoji you can use! :clap:

## Support / Donations
If you want to support node-emoji development, please consider donating (it helps me keeping my projects active and alive!): [![https://gratipay.com/omnidan/](https://img.shields.io/gratipay/omnidan.svg?style=flat-square)](https://gratipay.com/omnidan/)
