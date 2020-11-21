># Style Binding
- Use to apply inline styles to HTML elements and similar to class binding.


```js
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    <div>
      <h2>Welcome {{name}}</h2>
      <h2 [style.color]="'orange'">Style Binding 1</h2> 
      <h2 [style.color]="hasError ? 'red' : 'green'">Style Binding 2</h2>            
      <h2 [style.color]="highlightColor">Style Binding 3</h2>
      <h2 [ngStyle]="titleStyles">Style Binding 4</h2>
     
    </div>
  `,
  styles: []
})
export class TestComponent implements OnInit {

  public name = "Parth";
  public hasError = false;
  public isSpecial = true;
  public highlightColor = "orange";
  public titleStyles = {
    color: "blue",
    fontStyle: "italic"
  }


  
  constructor() { }

  ngOnInit() {
  }

}

```
># Syntax
- Same as class Binding