## Tuesday, April 6, 2021, 2:22:12PM -03 <1617729732>

- Remove all the vowels

```bash
function disemvowel(str) {
  return str.replace(/[aeiou]/gi, '');
}
```

## Sunday, March 28, 2021, 5:19:20PM -03 <1616962760>

### Regex tag +

/\w matches any word character (equivalent to [a-zA-Z0-9\_])
+ matches the previous token between one and unlimited times, as many times as possible, giving back as needed (greedy)

## Sunday, March 28, 2021, 5:10:54PM -03 <1616962254>

### String.prototype.trim()

The trim() method removes whitespace from both ends of a string. Whitespace in this context is all the whitespace characters (space, tab, no-break space, etc.) and all the line terminator characters (LF, CR, etc.).

```javascript
const greeting = '   Hello world!   ';

console.log(greeting);
// expected output: "   Hello world!   ";

console.log(greeting.trim());
// expected output: "Hello world!";
```

## Thursday, March 25, 2021, 2:39:57PM -03 <1616693997>

### Insert things in the middle of an array

```javascript
const months = ['Jan', 'March', 'April', 'June'];
months.splice(1, 0, 'Feb');
// inserts at index 1
console.log(months);
// expected output: Array ["Jan", "Feb", "March", "April", "June"
```

```javascript
let arrDeletedItems = arr.splice(start[, deleteCount[, item1[, item2[, ...]]]])
```

> deleteCount: An integer indicating the number of elements in the array to remove from start.

### Insert an array in an array

- Insert array values

> ...array

- Insert the whole array

> array

## Thursday, March 25, 2021, 11:20:22AM -03 <1616682022>

### find()

The find() method returns the value of the **first element in the provided
array** that satisfies the provided testing function. If no values satisfy the
testing function, **undefined** is returned.

## Wednesday, March 17, 2021, 2:11:37PM -03 <1616001097>

### Match Beginning String PatternsPassed

In an earlier challenge, you used the caret character (^) inside a character set to create a negated character set in the form [^thingsThatWillNotBeMatched]. Outside of a character set, the caret is used to search for patterns at the beginning of strings.

```javascript
let firstString = "Ricky is first and can be found.";
let firstRegex = /^Ricky/;
firstRegex.test(firstString);
let notFirst = "You can't find Ricky now.";
firstRegex.test(notFirst);
```
### Match Ending String Patterns

You can search the end of strings using the dollar sign character $ at the end of the regex.

```javascript
let theEnding = "This is a never ending story";
let storyRegex = /story$/;
storyRegex.test(theEnding);
let noEnding = "Sometimes a story will have to end";
storyRegex.test(noEnding);
```

## Wednesday, March 17, 2021, 8:28:09AM -03 <1615980489>

Searching for a literal match of the string

```javascript
let testStr = "freeCodeCamp";
let testRegex = /Code/;
testRegex.test(testStr); // True

let wrongRegex = /kevin/;
wrongRegex.test(testStr); // False
```
You can search for multiple patterns using the *OR* operator: **|**

> /yes|no|maybe/

**i** flag ignores letter case

> /ignorecase/i
> ignorecase, igNoreCase, and IgnoreCase

To search or extract a pattern more than once, you can use the **g** flag.

```javascript
let repeatRegex = /Repeat/g;
testStr.match(repeatRegex);
```

The wildcard character **.** will match any one character. The wildcard is also
called **dot** and **period**.

```javascript
let humStr = "I'll hum a song";
let hugStr = "Bear hug";
let huRegex = /hu./;
huRegex.test(humStr);
huRegex.test(hugStr);
```

You want to match bag, big, and bug but not bog. You can create the regex
**/b[aiu]g/** to do this. The **[aiu]** is the character class that will only match the characters a, i, or u.

```javascript
let bigStr = "big";
let bagStr = "bag";
let bugStr = "bug";
let bogStr = "bog";
let bgRegex = /b[aiu]g/;
bigStr.match(bgRegex);
bagStr.match(bgRegex);
bugStr.match(bgRegex);
bogStr.match(bgRegex);
```

Match Numbers and letters of the Alphabet
Using the hyphen (**-**) to match a range of characters is not limited to letters. It also works to match a range of numbers.

For example, **/[0-5]/** matches any number between 0 and 5, **including** the 0 and 5.

```javascript
let jennyStr = "Jenny8675309";
let myRegex = /[a-z0-9]/ig;
jennyStr.match(myRegex);
```

The closest character class in JavaScript to match the alphabet is \w. This
shortcut is equal to **[A-Za-z0-9_]**.

```javascript
let longHand = /[A-Za-z0-9_]+/;
let shortHand = /\w+/;
let numbers = "42";
let varNames = "important_var";
longHand.test(numbers); // True
shortHand.test(numbers); // True
longHand.test(varNames); // True
shortHand.test(varNames); // True
```

\W = [^A-Za-z0-9_]

Match number = \d
Math Non-Numbers = \D

To create a negated character you place a caret character (^) after the opening bracket and before the characters you do not want to match.

> /[^aeiou]/gi

```javascript
let firstString = "Ricky is first and can be found.";
let firstRegex = /^Ricky/;
firstRegex.test(firstString);
let notFirst = "You can't find Ricky now.";
firstRegex.test(notFirst);
```

You can search the end of strings using the dollar sign character **$** at the end of the regex.

```javascript
let theEnding = "This is a never ending story";
let storyRegex = /story$/;
storyRegex.test(theEnding);
let noEnding = "Sometimes a story will have to end";
storyRegex.test(noEnding);
```
