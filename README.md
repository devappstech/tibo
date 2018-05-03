# Tibo
> The best Tinder bot!
## Installing
To install, just run:
```bash
npm install --save tibo
```
## Getting your token
Go to [tinder.com](https://tinder.com) and enter with your account. Once you've done that, you'll need to track the network using Chrome's console. In every request made by Tinder, there's a header parameter named "**x-auth-token**", you need that token in order to use Tibo.
## Configure a blacklist
Tibo likes/denies users based on a blacklist. A blacklist must be an array of words (can even be empty, if you just want to use the bot), in which every word is searched in the user's bio, then, if the word is found, the user is denied.
## Make things work
```js
const tibo = require('tibo')

const blacklist = [
     'cats',
     'drugs',
     'fruits'
] // Every user with these words in their bio will be denied.

tibo('your-x-auth-token', blacklist)
```