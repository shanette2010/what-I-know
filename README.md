# What I Know

### Undefined vs Null vs Not defined
  *Undefined: Represents a variable that has been declared but not assigned any value.
  
  *Null: Represents an intentional absence of any object value

  *Not defined: refer to situations where a variable hasn't been declared or assigned any value.

### How do collection types treat undefined? What are collection/composite data types?
    *Collection types, such as arrays and objects can contian undefined values.

    *Collection or compite data types are data types that can hold multiple vaules.

Examples: 

//composite

const numbers = [1, 2, 3, 4, 5];
const fruits = ['apple', 'banana', 'orange'];
const mixedArray = [1, 'apple', true, [2, 4, 6]];

//collection

const nestedObject = {
    key1: {
        subkey1: 'value1',
        subkey2: 'value2'
    },
    key2: ['a', 'b', 'c'],
    key3: {
        subObject: {
            nestedKey: 'nestedValue'
        }
    }
};



### When does const not mean constant?

    *In Java script declares variables that cannot be reassigned. Like for an example,
    when varibales holds an array or an object. 

### How do we use variables as function arguments? What happens when we pass a variable that's bound to a primitive data type as a function argument?
    *Variables can be passed as a function arguments by putting it in parenthese. 

    *Like a string or a number when you add it to a primitive data type in a functional argument. The function 
    gets the same vaule.

### What's the deal with object literals? How do we reference their properties? What's the difference between dot notation and bracket notation?
    *Object literals are a way to create objects in JavaScript using curly braces {}.

    *Properties of an object can be referenced using dot notation (object.property). 
    Dot notation is simpler. Bracket notation allows for dynamic property access using variables or expressions.

Examples:


//dot notation 

const person = {
    name: "John",
    age: 30,
    occupation: "Engineer"
};

console.log(person.name); // Output: "John"
console.log(person.age); // Output: 30
console.log(person.occupation); // Output: "Engineer"

//bracket notaion

const person = {
    name: "John",
    age: 30,
    occupation: "Engineer"
};

console.log(person['name']); // Output: "John"
console.log(person['age']); // Output: 30
console.log(person['occupation']); // Output: "Engineer"

// Bracket notation allows for dynamic property access
const propertyName = 'age';
console.log(person[propertyName]); // Output: 30

### What about function scope? What's the deal with variable shadowing?
    *Function scope means that variables declared inside a function are only accessible within that function.

    *Variable shadowing occurs when a variable declared within a certain scope has the same name as a variable in an outer scope. 

Examples:


//function scope
function outerFunction() {
    // Variable declared inside the function scope
    var innerVariable = "I am inside the function";
    
    console.log(innerVariable); // Output: "I am inside the function"
}

//variable shadowing 
var outerVariable = "I am outside the function";

function outerFunction() {
    // Declaring a variable with the same name as the outer variable
    var outerVariable = "I am inside the function";

    console.log(outerVariable); // Output: "I am inside the function"
}



