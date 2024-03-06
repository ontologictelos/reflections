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
