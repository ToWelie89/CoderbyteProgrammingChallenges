# Coderbyte programming challenges - my solutions

#### Table of contents
=========

* [Easy challenges](#easy-challenges)
    * [Challenge 1 - Reverse a string](#user-content-challenge-1---reverse-a-string)

These are my solutions to the programming challenges found on http://coderbyte.com/

My language of choice is Javascript

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
