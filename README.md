# Coderbyte programming challenges - my solutions

These are my solutions to the programming challenges found on http://coderbyte.com/

My language of choice is Javascript

Table of contents
=========
* [Easy challenges](#easy-challenges)
    * [Challenge 1 - Reverse a string](#user-content-challenge-1---reverse-a-string)
    * [Challenge 2 - Determine factorial](#user-content-challenge-2---determine-factorial)
    * [Challenge 3 - Determine longest word](#user-content-challenge-3---determine-longest-word)

## Easy challenges

### Challenge 1 - Reverse a string

```javascript
function FirstReverse(str) {
    var reverseString = "";
    for (var i = (str.length - 1); i >= 0; i--) {
        reverseString += str.substring(i+1, i);
    }
    return reverseString;
}

FirstReverse(readline());
```

### Challenge 2 - Determine factorial

```javascript
function FirstFactorial(num) {
    var product = 1;
    for (var i = num; i > 0; i--) {
        product *= i;
    }
    return product;
}

FirstFactorial(readline());
```

### Challenge 3 - Determine longest word

function LongestWord(sentence) {
    sentence = sentence.replace(/[^a-zA-Z ]/g, "")
    var words = sentence.split(" ");

    var largestWord = "";

    for (var i = 0; i < words.length; i++) {
        if (words[i].length > largestWord.length) {
            largestWord = words[i];
        }
    }

    return largestWord;
}

LongestWord(readline());
```
