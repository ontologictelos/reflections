# Week-8 Homework

## Tuesday 05/03/ 2024 Reflections

### Translating human language into binary

In response to the UTF-8 or the translation of human language into 0 & 1's. Firstly this was kind of confusing but I think I get the jest of what he was talking about. If I am not misunderstanding, the issue that UTF-8 solves is an issue of translating english into binary in a way that is efficient and doesn't take up too much space.

It also seems like the issue was one of backwards compatibility with other I guess binary encoding systems. In the video he gave the example that Japan has three or four that are incompatible with each other. ASCII works well with english sense it has been made based off of the previous encoding system and is backwards compatible.

Where this becomes relevant to us besides learning the historical context of our own field of study, I would assume UTF-8 is what reads our code and translates it into binary or machine language. When working in HTML we have to define what character set we are using (in my intro to HTML & CSS we exclusively used UTF-8). I am unsure why in `js` we do not define our charset? Perhaps it is assumed by vs.code by how we save our document as a .md or a .js?

### Data types and notes

I feel pretty comfortable with `js` and the data types, they seem pretty self explanatory or at least the way you've explained them leaves little room for misunderstanding as to their function.

### syntax breakdown/ the grammar of `js`

#### Examples of `const`, `=`, strings, template literals, and concatenation

fig.1

``` JavaScript

// declare variable and assign value
const name = "Mark's";
const noun = "Bike";
const verb = "Running";

// reference variable
console.log (
    name + noun
);

// an additional form of concatenation

console.log (
    name + "favorite" + noun
);

// template literal example

console.log (
    `${name} favorite activity is riding his ${noun}.`
);

```

`const`: In fig.1 const is 'marrying' `name` and `"Mark's` together. In no other case can name mean something else UNLESS we use `let`.

`=` : is used to assign value to a variable. In fig.1  `name` is the variable and `"Mark's"` is the value being assigned to `name`.

`strings` : anythings encapsulated by ' ' or " "; however, typically the linter will want us to use "". In fig.1 `"Mark's"`, `"Bike"` and `"Running"` are all strings.

`concatenation` : essentially adding two strings together with the operant `+`. Bellow we see `name` and `noun` being concatenated together to form "Mark's Bike".

`${variable}` : this is a template literal. Using this instead of `concatenation is really helpful in the way of ease of reading.

#### Examples of `+`, `-`, `/` and `*`

fig.2

``` JavaScript

    // numbers through addition 4 should show up in the terminal
    console.log (
        2 + 2
    );

    // numbers through subtraction 1 should show up in the terminal
    console.log (
        2 - 1
    );

    // numbers through multiplication that should show 4 in the terminal
    console.log (
        2 * 2
    );

    // numbers through division that should show 1 in the terminal
    console.log(
        2 / 2
    );

    // example of implicit conversion that should result in 37 showing up in the terminal
    console.log(
        40 - "3"
    );

    // this will result in "22" and not four sense one is a number and the other is a string
    console.log (
        2 + "2"
    );

    // example of %
    console.log (
        5%6
    );

```

`numbers` : numbers are strict numbers when not contained within " ". Once a number is contained within " " or ' ' it becomes a string and is no longer seen as a number.

`+` `-` `/` `*` : self explanatory.

`%` : the percent sign indicates a remainder of a division problem. It looks as though we do not have to write out the division problem but just the two numbers joined together by the percent symbol to get the remainder.

#### Booleans and logical operators

```JavaScript
    // the following are all boolean expressions

    // example of &&
    const isCool = true
    const isDark = true

    const canHaveABonfire = isCool && isDark //true

    // example of ||
    const isSunny = false
    const isDark = true

    const canHaveABonfire = isSunny || isDark //true

    // example of !
    const isRaining = false

    const canHaveABonfire = !isRaining //true

    // example of ===
    const num1 = 50;
    const num2 = 59;

    console.log(
        num1 === num2
    ); //false

    const num1 = 20;
    const num2 = 20;

    console.log (
        num1 === num2
    ); //true

```

`booleans` = are characterized by being true or false statements.

`&&` : means and. Using this operant the result will be true if both operants are true other wise the result will return false.

`||` : means or. Returns true if one of the operants is true even if the other is false. Only when both operants are false will it return false.

`!` : equates to not. Returns true if the operant is false. Returns false if the operant is true.

`===` : this logical operant is a strict equality comparison of data types.

`==` : this logical operant is a loose comparison. This operant will compare just about anything. Logically this will not result in accurate true or false statements.

`=` : this operant is strictly used to assign value to a variable

## Thursday 07/03/2024 Reflections

### Eloquent JavaScript

Firstly, based off of reading the intro and the first chapter, I really appreciate this text. The text categorically presents information in a way that is coherent and easy to understand, i've also found this to be how I remember things best.

As for my actual reflections, it seems as though this goes over in more detail what tuesdays homework goes over. That being said I will go into more detail on things that we either did not discuss or things that were covered that I thought were not as important but have a new understanding of.

Interestingly, the author also introduces this idea of "defensive" coding (though not explicitly). Which is an interesting thought, I would figure this is akin to something of "best practices" that sort of save us from dumb problems that can be avoided. I got this "defensive" coding idea from the section Automatic Type Conversion in the last paragraph.

>" I recommend using the three character comparison operators defensively to prevent unexpected type conversions tripping you up"

A very useful tip. Although you eluded to this tip in your video when going over comparison operators.

#### Unary operators

The text introduces the `typeof` operator.

> "...the `typeof` operator, which produces a string value naming the type of value you give it"

``` JavaScript
    console.log (
        typeof 4.5
    ) // this produces the number 4.5

    console.log (
        typeof "x"
    ) //this produces a the string x
```

What confuses me on this is why does it even exist? we can just define strings and numbers anyway. I am just unsure of what use this actually is considering it can only take one operant.

#### Boolean values, comparisons

While reading the text I actually was wondering if strings could be compared considering each character is translated into binary giving it a numerical value. Seeing how strings can be compared is really  interesting. While this is just for the computer to compare and store values as letters into memory I imagine there is some interesting stuff one can do with this information. I would imagine ai does something with this in regards of storing words as numbers and assigning value to them such as verb, noun, or adjective in order to generate sentences. Probably wrong on this but an interesting thought.

notes: Upper case letters are worth less than lowercase letters

#### Short circuiting of logical operators

This was something I feel I skimmed over with Tuesdays homework. This is just a logical breakdown of the steps `js` goes through when using logical operators. Super interesting.

When using the `||` operator it reads left to right. Once `js` evaluates the left value, if that value is true then it just returns true without even evaluating the value to it's right. Only when the value to the operants left is false will it evaluate the right value.

While using the `&&` operator it still reads left to right but if the value to its left is false it returns false without ever evaluating the value to it's right. If the value to it's left is evaluated as true then and only then does it evaluate the value to it's right. Both must be true to give the return as a true statement otherwise it will be false.

> "Another important property of these two operators is that the expression to their right is evaluated only when necessary"
