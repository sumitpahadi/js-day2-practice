# js-day2-practice

#Question1=Difference between "==" and "===" operators:
The "==" operator is a loose equality operator in JavaScript, which means it performs type coercion before making a comparison. It converts the operands to a common type and then compares them. For example, "5" == 5 would be true because the string "5" is coerced to the number 5 before comparison.


#question2=>Differences between var, let, and const:
In JavaScript, var, let, and const are used for variable declaration, but they have some differences:
var: Variables declared with var have function scope or global scope, depending on where they are declared. They are hoisted to the top of their scope and can be accessed before they are declared. Additionally, var allows redeclaration and can be reassigned new values.

let: Variables declared with let have block scope, which means they are only accessible within the block they are declared in. They are not hoisted, so you need to declare them before using them. Unlike var, let does not allow redeclaration of the same variable within the same scope, but it can be reassigned new values.

const: Variables declared with const also have block scope and must be assigned a value at the time of declaration. They cannot be reassigned a new value once they are assigned. However, for objects and arrays, the properties or elements can be modified, even though the variable itself cannot be reassigned.



#question3=>Hoisting:
Hoisting is a JavaScript behavior where variable and function declarations are moved to the top of their containing scope during the compilation phase. This means that you can use variables and call functions before they are declared in the code. However, only the declarations are hoisted, not the initializations or assignments.



console.log(x); // Output: undefined
var x = 5;


#Question4=>Temporal Dead Zone:
The Temporal Dead Zone (TDZ) is a behavior that occurs when using variables declared with let and const. It refers to the time span between the start of a block scope and the point at which a variable is declared. During this period, trying to access the variable will result in a ReferenceError.

console.log(x); // Output: ReferenceError: x is not defined
let x = 5;


#Question 5=>First-class functions:
In programming, first-class functions refer to the concept of treating functions as first-class citizens, meaning they can be assigned to variables, passed as arguments to other functions, and returned as values from other functions. In other words, functions can be treated just like any other data type.
Assign a function to a variable:


const add = function(a, b) {
  return a + b;
};



#Question 6=>Pure functions:
Pure functions are functions that always produce the same output given the same inputs and do not cause any observable side effects outside the function. They have two main characteristics:
They do not modify the values of variables outside their scope.
They do not rely on or modify the state of external resources, such as databases or global variables.
Pure functions have several benefits, such as improved code maintainability, testability, and the ability to reason about their behavior more easily. Since pure functions have no side effects, they are less prone to bugs and can be safely parallelized.



function multiply(a, b) {
  return a * b;
}
