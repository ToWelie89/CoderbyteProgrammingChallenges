# Coderbyte programming challenges - my solutions

These are my solutions to the programming challenges found on http://coderbyte.com/

My language of choice is Javascript

Table of contents
=========
* [Easy challenges](#easy-challenges)
    * [Challenge 1 - Reverse a string](#user-content-challenge-1---reverse-a-string)
    * [Challenge 2 - Determine factorial](#user-content-challenge-2---determine-factorial)
    * [Challenge 3 - Determine longest word](#user-content-challenge-3---determine-longest-word)
    * [Challenge 4 - Letter changes](#user-content-challenge-4---letter-changes)
    * [Challenge 5 - Simple adding](#user-content-challenge-5---simple-adding)
    * [Challenge 6 - Letter capitalize](#user-content-challenge-6---letter-capitalize)
    * [Challenge 7 - Simple symbols](#user-content-challenge-7---simple-symbols)

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
```javascript
function LongestWord(sentence) {
    sentence = sentence.replace(/[^a-zA-Z0-9]/g, "")
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

### Challenge 4 - Letter changes
```javascript
function LetterChanges(str) {
    var vowels = ["a", "e", "i", "o", "u"];
    var stringAsArray = str.split("");
    for (var i = 0; i < stringAsArray.length; i++) {
        var pos = stringAsArray[i].charCodeAt(0);
        if ((pos >= 97 && pos < 122) || (pos >= 65 && pos < 90)) {
            stringAsArray[i] = String.fromCharCode(pos + 1);
        } else if (pos == 122) {
            stringAsArray[i] = String.fromCharCode(97);
        } else if (pos == 90) {
            stringAsArray[i] = String.fromCharCode(65);
        }

        if (vowels.indexOf(stringAsArray[i]) >= 0) {
            stringAsArray[i] = stringAsArray[i].toUpperCase();
        }
    }

    var newString = stringAsArray.join("");
    return newString;
}

LetterChanges(readline());
```

### Challenge 5 - Simple adding
```javascript
function SimpleAdding(num) {
    var totalSum = 0;

    for (var i = 1; i <= num; i++) {
        totalSum += i;
    }

    return totalSum;
}

SimpleAdding(readline());
```

### Challenge 6 - Letter Capitalize
```javascript
function LetterCapitalize(line) {
    var words = line.split(" ");
    for (var i = 0; i < words.length; i++) {
        var lettersInWord = words[i].split("");
        lettersInWord[0] = lettersInWord[0].toUpperCase();
        var newWord = lettersInWord.join("");

        words[i] = newWord;
    }
    var newString = words.join(" ");
    return newString;
}

LetterCapitalize(readline());
```

### Challenge 7 - Simple Symbols
```javascript
function SimpleSymbols(str) { 
    var letters = str.split('');
    for (var i = 0; i < letters.length; i++) {
        var letter = letters[i].toLowerCase();
        var charCode = letter.charCodeAt(0);
        if (charCode >= 97 && charCode <= 122) {
            if (!((letters[i - 1] && letters[i - 1] === '+') && (letters[i + 1] && letters[i + 1] === '+'))) {
                return false;
            }
        }
    }
    return true;
}

SimpleSymbols(readline());
```
