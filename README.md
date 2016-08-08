# ang2-parallax

### What Am I?!
An easy way to implement parallax scrolling for Angular2 components.  (There's also an [Angular 1.x](https://github.com/allenRoyston/ng-parallax "Angular 1.x") directive for those that need it.)
  - No dependencies
  - Responsive
  - Simple
  - Works for mobile!  (Well, iPhones at least - haven't tested on an Android yet)
  - Tiny

### Installation
First, alter your systemjs.config.js to include the right pathing.<br>
```
  var map = {
    'app':                        'app', // 'dist',
    '@angular':                   'node_modules/@angular',
    'angular2-in-memory-web-api': 'node_modules/angular2-in-memory-web-api',
    'rxjs':                       'node_modules/rxjs',
    'NG2_parallax':               'node_modules/ang2-parallax'
  };
  
  var packages = {
    'app':                        { main: 'main.js',  defaultExtension: 'js' },
    'rxjs':                       { defaultExtension: 'js' },
    'angular2-in-memory-web-api': { main: 'index.js', defaultExtension: 'js' },
    'NG2_parallax':               { defaultExtension: 'js' }
  };

```
Then include the module in your scripts.<br>
```

import { Component } from '@angular/core';
import { ng2Parallax  } from '../../../node_modules/ang2-parallax/ng2parallax';

@Component({
  selector: 'my-component',
  directives: [ng2Parallax],
  template:`
  
  <div style='width: 200; height: 200px'>
    <div parallax speed="5" src="path/to/image.jpg"></div>
  </div>
  
  `
})
export class componentName { }

```

### Version
1.0.0


### Live Demo 
[Check it out](https://ng2-parallax-demo.herokuapp.com/ "ng2 Parallax Demo")


### Dependencies
- None!

### NPM / Bower
```
npm install ang2-parallax --save
bower install ang2-parallax --save
```




### Parameters
```
speed = 0 to xx (the higher the number, the slower the effect).  This part requires some tinkering since different image sizes will respond differently.

src = path to image
```

License
----

MIT - go nuts y'all.
