```js
function beginAdding(inputValue) {
	return function(secondValue) {
		return inputValue + secondValue;
	}
}

let gimmeFive = beginAdding(5);
console.log(gimmeFive(3)) // "8"
```

The most foundational concept for functional programming, and one of my favorite things in programming.

## What makes closures so special?
The main thing to understand about closures is that they allow you to wrap code in a block, optionally with some parameters coming from outside, and then interact with that internal code in a controlled manner.

Another neat thing about closures is that ***any language that has [[First Class Functions]] can do closures.*** That means that if you learn how to think using closures, you will immediately find yourself at home in any of those languages.

## Why is that a useful thing?
If you think about the way I described closures up above, I'm essentially describing an interface to interact with some private state, right? That's literally what classes do in most other programming languages, but since we have [[First Class Functions]], we get that behavior for free.

This allows you to do pretty cool things, like:
- iterators
- generators [[Javascript References#Generators]]
- classical behavior for objects [[Javascript References#Private members]]
- currying [[Functional Programming References#Currying]]

## But do people actually use closures?
Yes, and here's a list of things that utilize closures:
- ***CALLBACKS!!!*** (the inner function is being passed in from the outside, but it's being called in the context of the function it was passed into.)
- [[Functional Programming]]
- SolidJS's signals: [[SolidJS References#Signals explanation]]
- Promises: [[Javascript References#Promise Explanation]]