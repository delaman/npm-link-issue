

1) git clone

2) npm install

3) node app.js


The above works with npm <=1.4.14

The correct output using npm 1.4.14 is as follows:

npm: 1.4.14
```
$ node -v
v0.10.29
$ 
$ npm -v
1.4.14
$ 
$ npm install
npm WARN package.json mainPackage@ No repository field.
 
> mainPackage@ preinstall /home/delaman/git/npm-link-issue
> rm -rf node_modules

 
> mainPackage@ postinstall /home/delaman/git/npm-link-issue
> npm --prefix node_modules link a/ b/

/home/delaman/git/npm-link-issue/node_modules/lib/node_modules/aPackage -> /home/delaman/git/npm-link-issue/a
/home/delaman/git/npm-link-issue/node_modules/lib/node_modules/bPackage -> /home/delaman/git/npm-link-issue/b
/home/delaman/git/npm-link-issue/node_modules/aPackage -> /home/delaman/git/npm-link-issue/node_modules/lib/node_modules/aPackage -> /home/delaman/git/npm-link-issue/a
/home/delaman/git/npm-link-issue/node_modules/bPackage -> /home/delaman/git/npm-link-issue/node_modules/lib/node_modules/bPackage -> /home/delaman/git/npm-link-issue/b
request@2.40.0 node_modules/request
├── json-stringify-safe@5.0.0
├── forever-agent@0.5.2
├── aws-sign2@0.5.0
├── oauth-sign@0.3.0
├── stringstream@0.0.4
├── tunnel-agent@0.4.0
├── qs@1.0.2
├── node-uuid@1.4.1
├── mime-types@1.0.2
├── tough-cookie@0.12.1 (punycode@1.3.1)
├── hawk@1.1.1 (cryptiles@0.2.2, sntp@0.2.4, boom@0.4.2, hoek@0.9.1)
├── http-signature@0.10.0 (assert-plus@0.1.2, asn1@0.1.11, ctype@0.5.2)
└── form-data@0.1.4 (mime@1.2.11, async@0.9.0, combined-stream@0.0.5)
$
$ node app.js
a
b
$
```


npm: 1.4.21
```
$ node -v
v0.10.30
$    
$ npm -v
1.4.21
$ 
$ npm install
npm WARN package.json mainPackage@ No repository field.

> mainPackage@ preinstall /home/delaman/git/npm-link-issue
> rm -rf node_modules

-
> mainPackage@ postinstall /home/delaman/git/npm-link-issue
> npm --prefix node_modules link a/ b/

/home/delaman/git/npm-link-issue/node_modules/lib/node_modules/aPackage -> /home/delaman/git/npm-link-issue/a
/home/delaman/git/npm-link-issue/node_modules/lib/node_modules/bPackage -> /home/delaman/git/npm-link-issue/b
/home/delaman/git/npm-link-issue/node_modules/node_modules/aPackage -> /home/delaman/git/npm-link-issue/node_modules/lib/node_modules/aPackage -> /home/delaman/git/npm-link-issue/a
/home/delaman/git/npm-link-issue/node_modules/node_modules/bPackage -> /home/delaman/git/npm-link-issue/node_modules/lib/node_modules/bPackage -> /home/delaman/git/npm-link-issue/b
request@2.40.0 node_modules/request
├── json-stringify-safe@5.0.0
├── forever-agent@0.5.2
├── aws-sign2@0.5.0
├── oauth-sign@0.3.0
├── stringstream@0.0.4
├── tunnel-agent@0.4.0
├── qs@1.0.2
├── node-uuid@1.4.1
├── mime-types@1.0.2
├── tough-cookie@0.12.1 (punycode@1.3.1)
├── form-data@0.1.4 (mime@1.2.11, async@0.9.0, combined-stream@0.0.5)
├── hawk@1.1.1 (cryptiles@0.2.2, sntp@0.2.4, boom@0.4.2, hoek@0.9.1)
└── http-signature@0.10.0 (assert-plus@0.1.2, asn1@0.1.11, ctype@0.5.2)
$ 
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
$ node -v
v0.10.31
$ 
$ npm -v 
1.4.23
$ 
$ npm install
npm WARN package.json mainPackage@ No repository field.

> mainPackage@ preinstall /home/delaman/git/npm-link-issue
> rm -rf node_modules

|
> mainPackage@ postinstall /home/delaman/git/npm-link-issue
> npm --prefix node_modules link a/ b/

/home/delaman/git/npm-link-issue/node_modules/lib/node_modules/aPackage -> /home/delaman/git/npm-link-issue/a
/home/delaman/git/npm-link-issue/node_modules/lib/node_modules/bPackage -> /home/delaman/git/npm-link-issue/b
/home/delaman/git/npm-link-issue/node_modules/node_modules/aPackage -> /home/delaman/git/npm-link-issue/node_modules/lib/node_modules/aPackage -> /home/delaman/git/npm-link-issue/a
/home/delaman/git/npm-link-issue/node_modules/node_modules/bPackage -> /home/delaman/git/npm-link-issue/node_modules/lib/node_modules/bPackage -> /home/delaman/git/npm-link-issue/b
request@2.40.0 node_modules/request
├── json-stringify-safe@5.0.0
├── forever-agent@0.5.2
├── aws-sign2@0.5.0
├── oauth-sign@0.3.0
├── stringstream@0.0.4
├── tunnel-agent@0.4.0
├── qs@1.0.2
├── node-uuid@1.4.1
├── mime-types@1.0.2
├── form-data@0.1.4 (mime@1.2.11, async@0.9.0, combined-stream@0.0.5)
├── tough-cookie@0.12.1 (punycode@1.3.1)
├── http-signature@0.10.0 (assert-plus@0.1.2, asn1@0.1.11, ctype@0.5.2)
└── hawk@1.1.1 (cryptiles@0.2.2, sntp@0.2.4, boom@0.4.2, hoek@0.9.1)
$ 
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
