## Installation

    npm install koa-authentication

## Usage

    This library is based on cas-authentication, and the interface is the same. You can refer to that documwnt.

## usage

````javascript
// variable declaration
const CasAuthentication = require('koa-cas-authentication');

const casConfig = require('../config/cas');

const cas = new CasAuthentication(Object.assign(casConfig, {
    session_info: 'user',
    session_name: 'username'
}));

...
// controller code
const isLogin = await cas.bounce(ctx);

if (isLogin) {
    await ctx.render('index');
}

````