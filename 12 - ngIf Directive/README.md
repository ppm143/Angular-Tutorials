># ngIf Directive

>## Structural Directives
- Directives let you `add or remove HTML elements from DOM`.
- 3 Common Built in Directives
  - ngIf
  - ngSwitch
  - ngFor
- `ngIf and ngSwitch for conditional rendering` and `ngFor for lists of HTML elements`. 

```js

import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `

    <h2 *ngIf="true">
      ngIf true
    </h2>

    <h2 *ngIf="displayName; else nameElseBlock">
      Parth
    </h2>

    <ng-template #nameElseBlock>
      <h2>
        Name is hidden
      </h2>
    </ng-template>

    <div *ngIf="displayName; then thenBlock; else elseBlock"></div>

    <ng-template #thenBlock>
      <h2>Parth</h2>
    </ng-template>

    <ng-template #elseBlock>
      <h2>Hidden</h2>    
    </ng-template>
    
    </div>
  `,
  styles: []
})
export class TestComponent implements OnInit {

  public displayName = false;
  constructor() { }

  ngOnInit() {
  }
}

```
