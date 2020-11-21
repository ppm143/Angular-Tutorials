># Pipes
- Pipes allows to transform data before displaying in the view.


```js
import { Component, OnInit, Input, Output, EventEmitter } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    
    <h2>{{"Parth Patel" | lowercase}}</h2>
    <h2>{{"Parth Patel" | uppercase}}</h2>
    <h2>{{"hello parth patel" | titlecase}}</h2>
    <h2>{{"Parth Patel" | slice:3:6}}</h2>

    <h2>{{person | json}}</h2>

    <h2>{{5.678 | number:'1.2-3'}}</h2>
    <h2>{{5.678 | number:'3.4-5'}}</h2>
    <h2>{{5.678 | number:'3.1-2'}}</h2>
    
    
    <h2>{{0.25 | percent}}</h2>

    <h2>{{0.25 | currency}}</h2>
    <h2>{{0.25 | currency:'GBP'}}</h2>
    <h2>{{0.25 | currency:'GBP':'code'}}</h2>
    
    <h2>{{date}}</h2>
    <h2>{{date | date:'short'}}</h2>
    <h2>{{date | date:'shortDate'}}</h2>
    <h2>{{date | date:'shortTime'}}</h2>
    
  `,
  styles: []
})
export class TestComponent implements OnInit {

  
  public person = {
    "firstName": "John",
    "lastName": "Doe"
  }

  public date = new Date();
  constructor() { }

  ngOnInit() {
  }

```
