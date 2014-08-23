

1) git clone

2) npm install

3) node app.js


The above works with npm <=1.4.14

The correct output using npm 1.4.14 is as follows:

npm: 1.4.14
```
$ node app.js
a
b
$
```


npm: 1.4.21
```
$ node app.js

module.js:340
    throw err;
          ^
Error: Cannot find module 'aPackage'
    at Function.Module._resolveFilename (module.js:338:15)
    at Function.Module._load (module.js:280:25)
    at Module.require (module.js:364:17)
    at require (module.js:380:17)
    at Object.<anonymous> (/home/delaman/git/npm-link-issue/app.js:2:1)
    at Module._compile (module.js:456:26)
    at Object.Module._extensions..js (module.js:474:10)
    at Module.load (module.js:356:32)
    at Function.Module._load (module.js:312:12)
    at Function.Module.runMain (module.js:497:10)
$ 
```

npm: 1.4.23
```
$ node app.js

module.js:340
    throw err;
          ^
Error: Cannot find module 'aPackage'
    at Function.Module._resolveFilename (module.js:338:15)
    at Function.Module._load (module.js:280:25)
    at Module.require (module.js:364:17)
    at require (module.js:380:17)
    at Object.<anonymous> (/home/delaman/git/npm-link-issue/app.js:2:1)
    at Module._compile (module.js:456:26)
    at Object.Module._extensions..js (module.js:474:10)
    at Module.load (module.js:356:32)
    at Function.Module._load (module.js:312:12)
    at Function.Module.runMain (module.js:497:10)
$ 
```
