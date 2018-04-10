# DiceBear Avatars

![license](https://img.shields.io/github/license/dicebear/avatars.svg)
[![npm](https://img.shields.io/npm/v/@dicebear/avatars.svg)](https://www.npmjs.com/package/@dicebear/avatars)
![Bower](https://img.shields.io/bower/v/dicebear-avatars.svg)

Avatars is a free pixel-art avatar placeholder library with HTTP-API.  
Test in your Browser: <https://avatars.dicebear.com/>

<img src="https://avatars.dicebear.com/v2/male/1.svg" width="60" />
<img src="https://avatars.dicebear.com/v2/femalemale/2.svg" width="60" />
<img src="https://avatars.dicebear.com/v2/identicon/3.svg" width="60" />
<img src="https://avatars.dicebear.com/v2/male/4.svg" width="60" />
<img src="https://avatars.dicebear.com/v2/femalemale/5.svg" width="60" />
<img src="https://avatars.dicebear.com/v2/identicon/6.svg" width="60" />
<img src="https://avatars.dicebear.com/v2/male/7.svg" width="60" />
<img src="https://avatars.dicebear.com/v2/femalemale/8.svg" width="60" />
<img src="https://avatars.dicebear.com/v2/identicon/9.svg" width="60" />

## Usage

### HTTP-API

Our free HTTP-API is the easiest way to use Avatars. Just use the following URL as image source.

    https://avatars.dicebear.com/api/v2/:sprites/:seed.svg

Replace `:sprites` with `male`, `female` or `identicon`. The value of `seed` can be anything you like.

### CDN

Choose the CDN if you want to use a spriteCollection that is not available via the HTTP-API.

Add the following line to the end of the document body.

    <script type="text/javascript" src="https://unpkg.com/@dicebear/avatars@2.0.0/dist/avatars.min.js"></script>

You also need to add a sprite collection. In our example, we will use the male sprite collection.

    <script type="text/javascript" src="https://unpkg.com/@dicebear/avatars-male-sprites@1.0.0/dist/sprites.min.js"></script>

Now you are ready to create your first Avatar.

    var avatars = new Avatars(Avatars.sprites.male);
    var svg = avatars.create('custom-seed');

### NPM

Choose NPM if you want to use Avatars server-side or with webpack.

Install the Avatars package with the following command.

    npm install --save @dicebear/avatars

You also need to add a sprite collection. In our example, we will use the male sprite collection.

    npm install --save @dicebear/avatars-male-sprites

Now you are ready to create your first Avatar.

    const Avatars = require('@dicebear/avatars').default;
    const IdenticonSprites = require('@dicebear/avatars-male-sprites').default;

    let avatars = new Avatars(IdenticonSprites);
    let svg = avatars.create('custom-seed');

Or with ES6-Modules:

    import Avatars from '@dicebear/avatars';
    import IdenticonSprites from '@dicebear/avatars-male-sprites';

    let avatars = new Avatars(IdenticonSprites);
    let svg = avatars.create('custom-seed');

## Further informations

You can find the complete documentation at [avatars.dicebear.com](https://avatars.dicebear.com)
