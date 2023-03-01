## March 1st, 2023

# Javascript Objects

![Objects](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fstatic.skillshare.com%2Fuploads%2FparentClasses%2F17abe69859d068286c56e7bd03294415%2Fb0876504&f=1&nofb=1)

## Lesson Overview

In this lesson, we'll discuss Objects and how they are essential data structures in JavaScript.

## Getting Started

- `fork` this respository
- Open a new CodePen project



## Lesson Objectives

_After this lesson, students will be able to:_

1. Explain the difference between arrays and objects
2. Store key-value pairs inside an object
3. Access values by key-name
4. Add Object Properties
5. Change Object Properties
6. Explain why we use an object instead of an array
7. Manipulate objects and arrays declared as `const`
8. List common errors made with objects
9. Use object properties with conditionals

## Explain the difference between arrays and objects

We have seen the following datatypes:

- String
- Number
- Boolean

Arrays are a **data structure**. We use them to organize our data: in the case of arrays, we can organize our data into a **sequential list** data structure.

- We can use arrays to store multiple pieces of data as a sequential list:

```js
const car = ['blue', 4000, 1989]
```

- Each element has a corresponding index (or place), in sequence.

But with the array above, we don't know what the values mean. Does "blue" refer to the color of the vehicle? To the mood of the owner? Is it the model of the vehicle?

- An object is also a **data structure**, but we can use objects to store data with greater specificity.

- In JavaScript, **objects** are what we use to represent **key-value** pairs.

## Store key-value pairs inside an object

Key-value pair syntax:

```js
const car = {
  color: 'blue',
  hp: 4000,
  year: 1989
}
```

- Unlike arrays, objects use _named keys_ rather than ordered indexes. Each piece of data is _bound_ to its key, rather than assigned an index. The data is not _sequential_.

- In Javascript, an object is a way to group many pairs of keys and values together

We can console.log the entire object:

```js
console.log(car)
```

## Access values by key-name

We can access the values stored in key using dot notation:

```js
console.log(car.color)
```

We can even store these variables as new ones to re use as we need

```
const carColor = car.color

```


We also can have functions attached to our Objects, which are referred to as "Methods"

`js

const car = {
make: "Ferrari",
model: "F450",
color: "Red",
mileage: 15,
drive () {
  console.log('Vroom vroom!')
}
```

Which can be accessed by simply calling them as :

```
car.drive()
```

## DIFFERENCES BETWEEN ARRAYS AND OBJECTS

- Arrays are declared using the square brackets `const arr = []`
- Objects are declared using the curly braces `const obj = {}`

Objects contain _key-value pairs_. They are are the **properties** of the object.

A **key** is like an **index** in an array, but it has:
- a name
- it is unique

A key is really a string but we can omit the quotes.

A **value** is what a key _refers to_, and can be *any* datatype.

## Add Object Properties

You can easily add more properties to a previously declared object:

```js
const house = {
  doors: 9
}

console.log(house)
```

> => { doors: 9 }

Add properties to the `house` object by simply adding a key using dot notation and the value using an equals `=`. Our house has no windows. Let's add some in _without_ writing them straight into the object:

```js
house.windows = 30
```

When we do it this way, the `windows` key is added to the object.

```js
console.log(house)
```

> => { doors: 9, windows: 30 }

Add another property `hasGarden`:

```js
house.hasGarden = true
```

## Change Object Properties

Changing the value of an existing key has the same syntax as creating a new key-value pair:

```js
const recipe = {
  isYummy: false
}
```

```js
recipe.isYummy = true
```

## Why We Use An Object Instead of an Array

When designing your programs, it is up to you to **choose** how to model your data. We can represent real-life things with our datatypes, but it's a matter of choosing the appropriate datatypes.

If the thing you want to model is just a list, use an **array**.

If the thing want to model has properties, use an **object**.

Using what we know about datatypes so far, which datatype would we use to model:

1. The name of your cat
2. The age of your cat
3. A list of your cat's favorite things
4. Whether your cat is asleep
5. Your cat

## Manipulate objects and arrays declared as `const`

`const` only prevents you from reassigning a variable; it doesn't prevent you from adding or changing elements of arrays or properties of objects.

You can do this:

```js
const cat = {}

cat.name = 'Gizmo'
```

Cannot do this:

```js
const cat = {}

cat = { name: 'Gizmo' }
```

## List common errors made with objects

### Unique Keys

It just makes sense that keys ought to be unique within an object. Values, however, can be repeated.

An object cannot have more than one key with the same name. If it does, the value will default to the last key with the same name, and the prior properties will be excluded on creation.

```js
const borough = {
  name: 'Brooklyn',
  name: 'The Bronx'
}
```

```js
console.log(borough)

=> { name: "The Bronx" }
```

Conclusion: keys should be unique within an object. Values, however, do not have to be unique.






## Use object properties with conditionals

You can use object properties with conditionals, loops, etc...

```js
const planet = {
  name: 'Saturn',
  rings: 9
}

if (planet.name == 'Saturn') {
  console.log('Saturn is the 6th planet from the Sun!')
}

for (let i = 0; i < planet.rings; i++) {
  console.log(i)
}
```

You can test to see if a property exists on an object:

```js
const planet = {
  name: 'Mars'
}

if (planet.name) {
  console.log('This key exists within the object')
}

if (planet.distance) {
  console.log('This key exists within the object')
} else {
  console.log('This key does not exist within the object')
}
```

This is because accessing a property that doesn't exist on an object gives you `undefined` which is a `falsy` value.


## OOP - Object Oriented Programming

OOP is a paradigm in coding that languages like Python, Ruby, and Java strictly follow. Javascript can use OOP, but as we've seen, it does not always have to.


#### Why might we use an OOP approach to programming?

Object-oriented programming (OOP) provides us with opportunities to clean up our procedural code and model it more-closely to the external world.

OOP helps us to achieve the following...
  * **Abstraction:** hiding all but the relevant data about an object in order to reduce complexity and increase efficiency
  * **Encapsulation:** is the process of combining data and functions into a single unit
  * **Inheritance:** Enables new objects to receive or inherit the properties and methods of existing objects
  * **Polymorphism**: Allows for many forms of the same type of object through inheritance

OOP becomes **very** important as our front-end code grows in complexity. Even a simple app will have lots of code on the front-end to do things like...
* Send requests to a back-end to fetch / update / destroy data
* Update the state of the page as data changes
* Respond to events like clicking buttons



An object encapsulates related data and behavior in an organized structure.

We've already gotten exposure to Javascript objects using **object literal notation**. We could define a car object in this way:

```js
const car = {
  make: 'Honda',
  model: 'Civic',
  color: 'red',
  drive() {
    console.log('vroom vroom');
  },
  gps(location) {
    console.log(`Beep boop, driving to ${location}`);
  },
  paint(newColor) {
    console.log(`Your car has been painted ${newColor}`);
    this.color = newColor;
  },
};
 ```

Even though we're technically using objects to organize our code, we can see a noticeable amount of duplication. Just imagine if we needed a hundred cars in our app! Our code would certainly not be considered "DRY".

As you may have noticed, some of these properties change between cars, and others stay the same. In the example above, while the `model` and `color` properties may vary, the `fuel` property and `drive` and `refuel` functions are the same for every car.

Making all of these similar objects by hand is just tedious. What if we could build a function that makes them for us?

### Create a `makeCar` Function

Define a function `makeCar` that takes two parameters - `model` and `color` - and returns an object literal representing a car using those params.

```js
// This should return a car object just like the previous example
const celica = makeCar('Toyota Celica', 'limegreen');
```

<details>
  <summary><strong>Solution...</strong></summary>

  ```js
  const makeCar = function(model, color){
    return {
      model: model,
      color: color,
      fuel:  100,
      drive: function() {
        this.fuel--;
        return 'Vroom!';
      },
      refuel: function() {
        this.fuel = 100;
      }
    }
  }
  ```

</details>




## Classes

It's so common that we need to make objects with similar properties and methods that programming languages usually have some features to help with this.

In Javascript, ES6 added a feature called **classes** to accomplish this. A class serves as a **blueprint** for instantiating new objects.

Let's take a look the following `Car` class:

```js
class Car {
  constructor(model, color) {
    this.model = model;
    this.color = color;
    this.fuel = 100;
  }
  drive() {
    this.fuel--;
    return 'Vroom!';
  }
  refuel() {
    this.fuel = 100;
  }
}


const celica = new Car('Toy-Yoda Celica', 'limegreen');
const civic = new Car('Honda Civic', 'lemonchiffon');
```

Classes work a lot like the `makeCar` function we just created, but are a more performant and offer more robust features.  
 We use the `new` keyword to generate **instances** of a class (just like our earlier `celica` and `civic` examples).

> Note that classes typically are capital case to make it obvious
that they are classes. This isn't necessary, but is a convention you should follow.


#### Lets Make a Person Class


```js
class Person {
  // We use the constructor method to initialize properties for a class instance.
  // It takes whatever arguments we want to pass into an instance.
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
  // We define any methods accessible to an instance outside of the constructor
  speak(){
    return `Hello! I’m ${this.name} and I am ${this.age} years olf`;
  }
}

const jeremy = new Person('Jeremy', 36);
jeremy.speak(); // "Hello, I'm Jeremy and I am 36 years old"
```



## Lesson Recap

We will use objects in JavaScript every day, and you will have plenty of time to practice creating and using them. There are a lot of resources available on the web for you to dive deeper, but the most detailed and understandable one is probably [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object).

## Resources

- [JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
- [Intro to Object-Orientated Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)
- [Objects in Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)
