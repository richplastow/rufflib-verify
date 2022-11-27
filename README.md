# ruffLIB Verify

__A ruffLIB library for succinctly validating JavaScript values.__

▶&nbsp; __Version:__ 0.0.1  
▶&nbsp; __Homepage:__ <https://richplastow.com/rufflib-verify>  
▶&nbsp; __NPM:__ <https://www.npmjs.com/package/rufflib-verify>  
▶&nbsp; __Repo:__ <https://github.com/richplastow/rufflib-verify>  
▶&nbsp; __Tests:__ <https://richplastow.com/rufflib-verify/test/run-browser-tests.html>  


### Typical usage:

```js
import { vNum } from 'rufflib-verify';

function sayOk(n) {
    if (vNum('sayOk()', 'n', n, 100)) return vNum.err;
    return 'ok!';
}

sayOk(123); // ok!
sayOk(null); // sayOk(): 'n' is null not type 'number'
sayOk(3); // sayOk(): 'n' 3 is < 100
```


## Dev, Test and Build

Run the test suite in ‘src/docs/’, while working on this library:  
`npm test --src`  
`npm start --src --open --test`  

Build the minified and unminified bundles in ‘dist/’ and ‘docs/’:  
`npm run build`

Run the test suite in ‘docs/’, after a build:  
`npm test`  
`npm start --open --test`  
