># Interpolation

- for dynamic value we can use `{{property}}`.
- define property in class.

```js

import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    <div>
      <h2>Welcome {{name}}</h2>
      <h2>{{2+2}}</h2>
      <h2>{{"Welcome " + name}}</h2>
      <h2>{{name.length}}</h2>
      <h2>{{name.toUpperCase()}}</h2>
      <h2>{{greetUser()}}</h2>
      <h2>{{url}}</h2>
    </div>
  `,
  styles: []
})
export class TestComponent implements OnInit {

  public name = "Parth";
  public url = window.location.href;

  constructor() { }

  ngOnInit() {
  }

  greetUser(){
    return "Hello " + this.name;
  }

}

```

>## Don't
- can't assign expression to variable
- can't call global variable like window object. for call window object we can bind in as a class property and then we can use.