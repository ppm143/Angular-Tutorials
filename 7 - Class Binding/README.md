># Class Binding
- if use both regular class attribute and class binding then regular class attribute become dummy in presence of class binding. So, don't use both.

```js
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    <div>
      <h2>Welcome {{name}}</h2>
     
      <h2 class="text-success">Parth</h2>
      <h2 [class]="successClass">Parth</h2>
      <h2 class="text-special" [class]="successClass">Parth</h2>
      <h2 [class.text-danger]="hasError">Parth</h2>
      <h2 [ngClass]="messageClasses">Message</h2>
      
    </div>
  `,
  styles: [`
    .text-success{
      color: green;
    }
    .text-danger{
      color: red;
    }
    .text-special{
      font-style: italic;
    }
  `]
})
export class TestComponent implements OnInit {

  public name = "Parth";
  public successClass = "text-success";
  public hasError = false;
  public isSpecial = true;
  public messageClasses = {
    "text-success": !this.hasError,
    "text-danger": this.hasError,
    "text-special": this.isSpecial
  }

  
  constructor() { }

  ngOnInit() {
  }


}


```

>## Syntax

- `[class]="classname"`
- `[class.text-danger]="hasError"` is conditional class apply if hasError value true then class text-danger will apply.
- if you apply conditionally multiple classes then angular provide `[ngClass]=classes` directive