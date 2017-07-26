# Promesify
## What is it?
This is a really simple and naive library that transforms a typical node asynchronous function into a promise.

Example:
```JavaScript
fs.readdir('directory', (err, data) => {
  if(err){
    return console.log(err);
  }
  console.log(data);
});
// becomes
readdir('directory')
  .then(console.log)
  .catch(console.log)
```
## Usage
```JavaScript
import {promesify} from 'promesify-js';
const newFunction = promesify(yourAsyncFunction);
newFunction(all, your, args, except, the, callback)
  .then(console.log)
  .catch(console.log);
```
