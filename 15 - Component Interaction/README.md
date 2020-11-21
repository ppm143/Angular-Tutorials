># Component Interaction
- component interact with decorators.
- img 7
- `@input` child can accept input from parent.
- `@output` child send event to parent.
  
>## Parent Component
```js
  
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  template: `
    <h1>{{message}} </h1>
    <app-test (childEvent)="message=$event" [parentData]="name"></app-test>
  `,
  styles: []
})
export class AppComponent {
  title = 'app';
  public name = "Parth";
  public message = "";
}

```

>## Child Component
```js
  
import { Component, OnInit, Input, Output, EventEmitter } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    <h2>
      {{"Hello " + name}}
    </h2>
    <button (click)=fireEvent()>Send Event</button>
  `,
  styles: []
})
export class TestComponent implements OnInit {

  @Input('parentData') public name;
  @Output() public childEvent = new EventEmitter();
  constructor() { }

  ngOnInit() {
  }

  fireEvent(){
    this.childEvent.emit('Hey Parth');
  }
  ```