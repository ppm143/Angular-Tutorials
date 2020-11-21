># Two Way Binding
- Angular provide `ngModel` for two way binding
- img6
- `[]` data flow from class to view
- `()` data flow from view to class
- `[()]` bi-directional data flow
- For `ngModel` we have to import `FormModule` in `app.module.ts`.

```js

import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    <div>
      <input type="text" [(ngModel)]="name">
      {{name}}
    </div>
  `,
  styles: []
})
export class TestComponent implements OnInit {

  public name = "";
  constructor() { }
  ngOnInit() {
  }
}

```


