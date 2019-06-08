# monkey
A simple programming language. This repo contains a compiler for it. Based on `Writing an Intrepretea` by Thorsten Ball.

## Language Features
- C-like syntax
- variable bindings
- integers and booleans
- arithmetic expressions
- built-in functions
- first-class and higher-order functions
- closures
- a string data structure
- an array data structure
- a hash data structure

## Syntax
### Assigning variables
```javascript
let age = 1;
let name = "Monkey";
let result = 10 * (20 / 2);
```

### Arrays and hashes
```javascript
let myArray = [1, 2, 3, 4, 5];
let user = {"name": "Ricky", "age": 28};

myArray[0]       // => 1
thorsten["name"] // => "Ricky"
```

### Functions
```javascript
let add = fn(a, b) { return a + b; };
let add2 = fn(a, b) { a + b; }; // return can be left out

// Calling functions
add(1,2); //  => 3
add2(1,2); // => 3

// More complex recursive function example
let fibonacci = fn(x) {
  if (x == 0) {
    0
  } else 
    if (x == 1) {
      1
    } else {
      fibonacci(x - 1) + fibonacci(x - 2);
    }
  }
};

// Higher order functions
let twice = fn(f, x) {
  return f(f(x));
};

let addTwo = fn(x) {
  return x + 2;
};
twice(addTwo, 2); // => 6
```

## To dos
- [ ] Lexer
- [ ] Parser
- [ ] AST
- [ ] internal object system
- [ ] evaluator