
# Reverse Words Algorithm


* Every word in the string should be reversed but the string as a whole should not be reversed
     * ex. 'this is a strong of words' = siht si a gnirts fo sdrow' not 'sdrow fo gnirths a si siht'

* Can't use array reverse method so we can solidify our skills with our array and string manipulation.
    * We will do this by looping through every letter in our wordArr backwards

    * for (let i = word.length -1; i>=0; i--) {
        * using a for loop to go backward instead of forward. then we will add a new letter to each string

            * reversedWord += word[i];

```javascript
function reverseWords(string) {

    // define reverseWords as a function that takes in a string as a parameter

    // reverse every word in the string

let wordsArr = string.split(' ');

    // create an array of all the words in our string (on every space character (' '))

let reversedWordsArray = [];

    // define an empty array to push all of our reversed words into after we have reversed each of them

wordsArr.forEach(word => {

    // wordsArr.forEach(function(word)) {}

    // loop through every word in the wordsArr, reverse that word

    // and push it into the new reversedWordsArray using forEach loop.

    // Now we have access to each word of the array

let reversedWord = '';

    // first, define an empty string to build our reversed word from

for (let i = word.length -1; i>=0; i--) {

    // now we want to loop through every word in our string backwards and add it to our empty string
    using a for loop to go backward instead of forward.

    // our loop is starting on the last character in our string and we are moving backward to the first
    character of the string (index 0)

    // we want to decrement i by 1 on every iteration (i--)

    reversedWord += word[i];

    // inside our loop, we will add (+=) the current letter to our reversed word
    then we will add a new letter to each string.

    // That will add the letter at position i (word[i]) to the reversed word
}
reversedWordsArray.push(reversedWord);

// outside of the for loop, after all the letters have been added to our reverseWord string, but still
inside of our forEach loop, we want to push our completed reversedWord string into our reversedWord array
(reversedWordsArray.push(reversedWord);)

});

return reversedWordsArray.join(' ');
// we want to return our final reversedWords array as a string and pass in a space character (' ')
}

console.log(reverseWords('this is a string of words'));
```

## Compressed version of Reverse Words Algorithm

```javascript
function reverseWords(string) {

var wordsArr = string.split(' ');

var reversedWordsArr = [];

wordsArr.forEach(word => {

var reversedWord = '';

for (var i = word.length - 1; i >= 0; i--) {
    reversedWord += word[i];

}

reversedWordsArr.push(reversedWord);

});

return reversedWordsArr.join(' ');

}

reverseWords('this is a string of words');
    ```