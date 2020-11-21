># Components
- Components are building block of angular applications.
>## Component made up 3 parts
1. Template
   - View
   - HTML

2. Class
   - Code
   - Typescript
   - Data & Methods

3. Metadata
   - Information
   - Decorator

```js
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html',
  styleUrls: ['./app.component.css']
})
export class AppComponent {
  title = 'app';
  public name = "Parth";
  public message = "";

}
```

- Create a new component
  - `ng g c component_name`

>## 3 ways to define selectors
1. custom element
  - `selector: 'app-test'`
  - `<app-test></app-test>`

2. class 
  - `selector: '.app-test'`
  - `<div class="app-test"></div>`

3. Enclosing [] brackets and use as attribute
  - `selector: '[app-test]'`
  - `<div app-test></div>`


>## Templates

1. External
-  `templateUrl: './app.component.html'`

2. Inline
- `template: '<h1>Hello</h1>'  `

>## Styles

1. External
-  `styleUrls: ['./app.component.css']`

2. Inline
- `styles: [ div{ color : red} ] `