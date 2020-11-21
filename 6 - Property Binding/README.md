># Property Binding

>## Attribute vs Properties
- Attributes and properties are not the same.
- Attributes are define by HTML.
- Properties are define by DOM.
- Attributes initialize DOM properties and then they are done. Attributes values cannot change once they are initialized.
- Properties value however change.

- Limitation of interpolation is it can only works with string value.


```js
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    <div>
      <h2>Welcome {{name}}</h2>
      <input [id]="myId" bind-disabled="isDisabled"  type="text" value="Parth">
      <input id="{{myId}}" [disabled]="isDisabled"  type="text" value="Parth">
    </div>
  `,
  styles: []
})
export class TestComponent implements OnInit {

  public name = "Parth";
  public myId = "testId";
  public isDisabled = true;
 
  constructor() { }

  ngOnInit() {
  }
}

```
>## Syntax
- `[property] = "value"`
- `bind-property = "value"`