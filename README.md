
# Angular QuickStart Source

This repository is a fork from [angular/quickstart](https://github.com/angular/quickstart).


## Changelog
### 0.0.1 (2017-03-18)
* Delete non-essentials files
* js and js.map files are generated in dist folder
```
.
└──src
│  └──app
│  │  │  app.component.ts
│  │  │  app.module.ts
│  │
│  └──dist
│  │  └──app
│  │     │  app.component.js
│  │     │  app.component.js.map
│  │     │  app.module.js
│  │     │  app.module.js.map
│  │  main.js
│  │  main.js.map
│  index.html
│  main.ts
```
If you want to undo this change, please, follow the next steps

``` 
index.html
System.import('dist/main.js').catch(function(err){ console.error(err); });
by
System.import('dist/main.js').catch(function(err){ console.error(err); }); 
```
``` 
systemjs.config.js
app: 'dist/app'
by
app: 'app' 
```
``` 
tsconfig.json
remove
"outDir": "dist"
```
 