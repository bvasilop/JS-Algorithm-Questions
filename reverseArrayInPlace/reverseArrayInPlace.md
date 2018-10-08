    function reverseArrayInPlace(arr) {

        // define function passing in array as parameter // reverse arr

    for (let i = 0; i < arr.length / 2; i++) {

        // first we want to switch the first element of the array with the last element of the array, then we want to switch the second element of our array with the second to last element of the array.

        // Reason we divide by two is as we go through the first half of the array, we are correctly reassigning each element but then as we continue through the second half of the array we are switching every element back again ex. [1,2,3,4],[4,2,3,1],[4,3,2,1],[1,2,3,4]. That's why we go half way and divide by 2 [4,3,2,1].

    let tempVar = arr[i];

        // loop through first half of array

        // declare and assign a temporary variable

        // first store element at position [i]. We now have our i-th element of our array stored in our temp variable

        // now we want to set our i-th element of our array equal to its counterpart (if this would be first iteration, i = 0)

    arr[i] = arr[arr.length - 1 - i];

        // arr at position i  = arr at position [arr.length - 1 = last element in the array) - i ( this i makes this whole element the counterpart of this element( arr[i] ) takes us back places from the end of the array opposite of the beginning of the array. IE if third iteration then 3 places from the beginning of array and three places from the end of the array

    arr[arr.length - 1 - i] = tempVar;

        // we rewrite its counterpart (arr[arr.length - 1 - i]) to be equal to the current element the element that was originally at position [i] // arr at position [arr.length - 1 - i] = our tempVar which has element at position [i] stored in it

    }

    return arr; // return reversed arr

    }

    let words = ['the', 'cow', 'jumped', 'over', 'the', 'moon'];

    let newArrayInPlace = reverseArrayInPlace(words);

    let newWords = newArrayInPlace.join(' ');

    // console.log(newWords);

    function capitalizeFirstLetter(newWords) {
    // function for capitalizing first word of new sentence

    return newWords.charAt(0).toUpperCase() + newWords.slice(1);

    }

    console.log(capitalizeFirstLetter(newWords));

  /**************************************** */

    function reverseArrayInPlace(arr) {

    for (let i = 0; i < arr.length / 2; i++) {

    let tempVar = arr[i];

    arr[i] = arr[arr.length - 1 - i];

    arr[arr.length - 1 - i] = tempVar;

    }

    return arr;

    }

    let words = ['the', 'cow', 'jumped', 'over', 'the', 'moon'];

    let newArrayInPlace = reverseArrayInPlace(words);

    let newWords = newArrayInPlace.join(' ');

    function capitalizeFirstLetter(newWords) {

    return newWords.charAt(0).toUpperCase() + newWords.slice(1);

    }

    console.log(capitalizeFirstLetter(newWords)); // Moon the over jumped cow the
