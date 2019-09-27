# Is Palindrome Algorithm

- Palindrome: any word or phrase that is spelled the same way both backward and forward
  // ex. race car, Madam, I'm Adam

- one way to solve is using JavaScript regular expressions (not used in this example)
- instead we will use String and Array manipulation and String and Array methods

```javascript
function isPalindrome(string) {
  // takes in a string as a parameter
  // we ignore any punctuation characters

  string = string.toLowerCase();

  // first thing is we turn everything into lowercase using toLowerCase method
  // set string = string.lowerCase() invoked

  var charactersArr = string.split('');

  // turn string into an array of characters
  // use string.split method and pass in empty string

  var validCharacters = 'abcdefghijklmnopqrstuvwxyz'.split('');

  // make array of any characters that will be allowed in our string
  // we need an array of every lowercase letter in the alphabet by defining array and
  // placing every letter in the alphabet in our array

  var lettersArr = [];

  // we define a new letters array to place only the letters of our charactersArray

  charactersArr.forEach(char => {
    // we will use forEach array helper method

    if (validCharacters.indexOf(char) > -1) lettersArr.push(char);

    // indexOf is an array method that returns the array of the argument passed in
    // if we pass the letter "a" it would return number 0 using indexOf because a is 0ith index of validCharactersArray "b" would return 1
    // -1 means the argument passed in is not present in the array ( if we try to pass , or ' ) indexOf would return -1
    // we want to check each character and push it into our lettersArr only if it is a letter
    // this is how we end up with our lettersArray with no special characters in it
  });

  if (lettersArr.join('') === lettersArr.reverse().join('')) return true;
  // return true because it's the same forward as backward
  else return false;
}
// we convert our lettersArray back into a string and we compare the new lettersArr backward and forward to see if they are the same
// if they are the same then our original string is a palindrome.
// returns true if the string is a palindrome false if it is not

console.log(isPalindrome(`Madam I'm Adam`));
console.log(isPalindrome(`race car`));
```

## condensed and cleaned up version

```javascript
function isPalindrome(string) {
  string = string.toLowerCase();
  var charactersArr = string.split('');
  var validCharacters = 'abcdefghijklmnopqrstuvwxyz'.split('');

  var lettersArr = [];
  charactersArr.forEach(char => {
    if (validCharacters.indexOf(char) > -1) lettersArr.push(char);
  });

  return lettersArr.join('') === lettersArr.reverse().join('');
}

isPalindrome(`Madam, I'm Adam`); // true
```
