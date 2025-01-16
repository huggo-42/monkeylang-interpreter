todo after:
    [ ] Vaughan Pratt in his “Top Down Operator Precedence”

# monkeylang-interpreter
Implementation of the book Writing An Interpreter In Go by Thorsten Ball

Steps to recognize more token
1. modify the input of our test case to include these characters


Parsing
2.1 - Parsers

Here is a little bit of JavaScript:
```js
> var input = '{"name": "Thorsten", "age": 28}';
> var output = JSON.parse(input);
> output
{ name: 'Thorsten', age: 28 }
> output.name
'Thorsten'
> output.age
28
>
```
Our input is just some text, a string. We then pass it to a parser hidden 
behind the JSON.parse function and receive an output value. This output is the 
data structure that represents the input: a JavaScript object with two fields 
named name and age, their values also corresponding to the input. We can now 
easily work with this data structure as demonstrated by accessing the name and 
age fields.


2.4 - Parser's first steps: parsing let statements
```monkeylang
let x = 10;
let y = 15;

let add = fn(a, b) {
    return a + b;
}
```
Form:
let <identifier> = <expression>;
>expressions produce values, statements don’t

2.5 - Parsing Return Statements
Steps:
1. define the necessary structures in the `ast` package with which we can 
represent return statements in our AST.
2. write test that fails
3. add necessary code to make test pass (parser.go)


2.6 - Parsing Expressions

# Implementing the Pratt Parser


2.7 - How Pratt Parsing works
