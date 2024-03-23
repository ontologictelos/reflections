# Week 9

## Homework 23/03/24

1. Whats up with `undefined` Vs `null` Vs `not defined`
   1. `undefined` : is when a variable has been declared but no value given to it. In philosophical terms this means a variable exists but it has no being, a body but without a brain or soul (whatever it is that animates bodies).

   2. `null` : is no value.

   3. `not defined` : this is when we reference something that just doesn't exist in our code or memory. In the video you reference variable t and get an error. This is because the computer searched itself to find the variable t and found nothing. I think this is really just a logic error. Nothing as a concept exist's because we use the idea to describe the absence of something but Nothing in reality does not exist. The computer is literally searching for nothing a thing that has no being or root in reality.

2. How do collection types treat `undefined`? What are collection/composite data types?

   1. firstly, collection and composite data types are objects. But what is an object? An object is a collection of relational data. The relational data must be defined or put into relation to a `const` otherwise the data has no value attached to it.

        ```javascript
        const coffeeTypes = ["cortado", "cappuccino", "latte"];
        //Here cortado, cappuccino and latte are being 
        //put in relation to coffee types.

        ```

   2. secondly, collection types treat `undefined` just as it is...undefined. It will tell us "hey you asked me for hair color but thats not defined within the collection data so instead of what you asked for im going to give you undefined because i don't know what you are asking for".

3. When does `const` not mean constant?
   1. `const` doesn't mean constant when it is tied to an object. If we use `const name = Mark` const is constant because it is a primitive data type where name will always equate to Mark. But if `const` is tied to an object then `const` does not really mean constant. `const` in the case below really just grounds the values into relation with each other.

   2. Think of const in this case as actual espresso. Espresso can be an ethiopia, colombia, brazil etc. It can be anything. If we redefine the index number (the order by which the coffee is listed in espresso) then it is no longer ethiopia but then becomes mexico.`const` in this way becomes more like `let` but put into relation with other variables.

        ```javascript
        const espresso [
        "ethiopia",
        "colombia",
        "brazil"
        ]

        console.log(espresso[0]) //ethiopia

        espresso[0]= "mexico"
        console.log(espresso[0]) //mexico
        ```

4. How do we use variables as function arguments? What happens when we pass a variables that's bound to a primitive data type as a function argument?
   1. variables are kind of place holders for values to be used in the function. In the below example, within the function `x` and `y` are variables that are just placeholders for arguments (num1, num2). Now num1 and num2 are also names containing the value of 2 and 4. When we pass a primitive data type into an function the value of that primitive data type is copied into the function. The reason for this is because num1 and num2 are married to the values 2 & 4. They themselves cannot be put into the function because they are a primitive data type where num1 will always be attached to 2. const in this case means constant.

        ```javascript
        // arguments
        const num1 = 2;
        const num2 = 4;

        // here is our function with x and y as variables
        function add(x,y){
        return x + y;
        }

        const sum = add (num1,num2) //the values of num1 & num2 are copied into the function

        console.log(sum) //3

        ```

5. Whats the deal with object literals? How do we reference their properties? What's the difference between dot notation and bracket notation?
   1. `object literals` are quite literally objects that are literal. While that statement needs some translating when someone uses the phrase object literal in this context we create objects that are strings and we give that string a name and the name is literally representing the string. I really like your example with explanation. Explanation is LITERALLY "We just make up our own STRING keys....". Where as with an array we are referencing an index number object literals reference strings. We reference object literal properties (the string) by calling on their name. In this case myString would be used to get the property "string".

        ```javascript
       const myObj = {
        myString: "String",
        myNum: 23,
        myBoo: true,
        explanation:
            "We just make up our own STRING keys, and assign whatever value we want. All the while this is all wrapped up under 1 VARIABLE that REFERENCES this OBJECT LITERAL (literal just signifies that we made this OBJECT - it's not 'built in').",
        };
        ```

   2. The difference between dot notation and bracket notation is really just how you format your request of information.
      1. bracket notation `console.log(coffee.espresso);`
         1. here we see the name of the element name (coffee) and we are requesting the information in the named index 'espresso'
         2. also notice no quotations.
      2. bracket notation `console.log(coffee["espresso"]);`
         1. Here same general lay out element name (coffee) and the named index but instead of a '.' we enclose it with `[ ]` and put the named index in `" "`.

6. What about function scope? What's the deal with variable shadowing?

   1. function scope is when a variable is defined within a function. Doing this makes that variable accessible within that function.

   2. Variable shadowing is when we declare a variable within a function and also use the same name to reference a variable outside of the function.

   ```javascript
     //function scope

     function getCoffee(){
        const espresso = "ethiopia"
        console.log (espresso);
     }
     console.log (espresso); // espresso is locked inside the function

     //variable shadowing

     const espresso = "ethiopia"

     function getCoffee(){
        const espresso = "colombia"
     }
     // espresso is both ethiopia and colombia 
     //(which technically espresso can be both in real life)
     // but in this case we don't want to do this for our own sake.
   ```
