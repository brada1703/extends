## `extends` keyword



*   The `extends` keyword is used in class declarations or class expressions to create a class which is a child of another class.
*   Note the syntax in the following example:

```
class ChildClass extends ParentClass { ... }
```


*   Here is more complete example:
*   In this example, we start with the Animal parent class. Here you have the function “run” and a construtor which accepts a name variable and starts the speed out at zero.
*   The Bear class, because it extends the Animal class, inherits the functions and attributes within the Animal class. The Bear will inherit the speed and name attributes from the constructor in the Animal class as well as the `run()` function, which accepts the `speed` parameter. Then, in the Bear class, it will add the number of pups that it has as well as add the function `hibernate()`.
*   In JavaScript, classes can only extend one class at a time.

```
class Animal {
  constructor(name) {
    this.speed = 0;
    this.name = name;
  }
  run(speed) {
    this.speed = speed;
    console.log(`${this.name} runs with speed ${this.speed}.`);
  }
}

class Bear extends Animal {
  constructor(name, pups){
    super(name);
    this.pups = pups;
  }
  hibernate() {
    console.log(`${this.name} hibernates!`);
  }
  howManyPups(){
    console.log(`${this.name} has ${this.pups} pups!`)
  }
}
```
*   Then we can call the Bear class by calling `new Bear()`:
*   We can then call the functions, whether they are inherited or otherwise, through dot notation.

```
let bear = new Bear("Winnie", 5);

bear.run(1); // Winnie runs with speed 1.
bear.hibernate(); // Winnie hibernates!
bear.howManyPups();
```


*   Note that Internet Explorer does not currently [support](https://caniuse.com/#search=extends) Classes or their respective keywords, including `extends`.

Resources:

[Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes/extends)
