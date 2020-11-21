>## Template Reference Variables
- Some data may flow from view to class so to easily access DOM element and properties angula provide template reference variable.

```js

import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    <div>
      <h2>Welcome {{name}}</h2>
      <input #myInput type="text">
      <button (click)="logMessage(myInput.value)">Log</button>
      {{name}}
    </div>
  `,
  styles: []
})
export class TestComponent implements OnInit {

  public name = "Parth";

  constructor() { }

  ngOnInit() {
  }

  logMessage(value){
    console.log(value)
  }

}

```