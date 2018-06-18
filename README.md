## Installation

    npm install koa-authentication

## Document

    This library is based on cas-authentication, and the interface is the same. You can refer to that documwnt.

## Usage

````javascript
// variable declaration
const CasAuthentication = require('koa2-cas-authentication');

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