># Dependency Injection

>## 3 Parts
1. Code without DI - drawbacks

```js
class Engine{
    constructor(){}
}

class Tiers{
    constructor(){}
}

class Car{
    engine;
    tires;
    constructor(){
        this.engine = new Engine();
        this.tires = new Tires();
    }
}
```
- in this case suppose if Engine or Tires class accept parameters then Car class will broken.
- Not suitable for testing.  
2. DI as a design pattern

- DI is a coding pattern in which a class receives its dependencies from external source rather than creating them itself.
  
>### Without DI
```js
class Car{
    engine;
    tires;
    constructor(){
        this.engine = new Engine();
        this.tires = new Tires();
    }
}
```
>### With DI

```js
class Car{
    engine;
    tires;
    constructor(engine,tires){
        this.engine = engine;
        this.tires = tires;
    }
}
```

- Using this we can resolve our previous drawback

3. DI as a framework
    1. Define the EmployeeService class
    2. Register with injector
    3. Declare as dependency in EmpList and EmpDetail