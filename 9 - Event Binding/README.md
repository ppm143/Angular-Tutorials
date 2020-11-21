># Event Binding
- In data binding data flow goes from `component to class`. But sometimes response of user event like click we need to data flow from `other directions`. So, for this we need `event binding`.

![](https://github.com/ppm143/AllProjectImages/blob/master/Angular/5.JPG)


```js
import { Component, OnInit } from '@angular/core';

@Component({
  selector: 'app-test',
  template: `
    <div>
      <h2>Welcome {{name}}</h2>
      <button (click)="onClick($event)">Greet</button>
      <button (click)="greeting = 'Welcome Parth'">Greet Parth</button> 
     {{greeting}}
    </div>
  `,
  styles: []
})
export class TestComponent implements OnInit {

  public name = "Parth";
  public greeting = "";
  
  constructor() { }

  ngOnInit() {
  }

  greetUser(){
    return "Hello " + this.name;
  }

  onClick(event){
    console.log(event)
    this.greeting = event.type;
  }
  
}

```
>## Syntax
- `$event` event variable in angular
