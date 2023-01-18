# Limesharp Developer Test

Please, **don't fork this repo**, clone it or download it locally and then commit changes after each task into a new repo of your own, and send us the link. We will get back to you shortly. 

Languages accepted: Javascript or PHP. 

### Task 1: 
Make this work (repeat 3 times the contents of an array):
```javascript
repeat([1,2,3]) //[1,2,3,1,2,3,1,2,3]
```
Your solution:

```
function repeat(arr) {
    return arr.concat(arr, arr);
}
console.log(repeat[1,2,3]);
```

###### If we type in our console your function and repeat([1,2,3]) then the result should be [1,2,3,1,2,3,1,2,3] 

### Task 2:
Make this work (no vowels, lowercase except the first letter):
```javascript
reformat("liMeSHArp DeveLoper TEST") //Lmshrp dvlpr tst
```
Your solution:

```
function reformat(content) {
    //define vowels
    let vowels = "aeiou"

    //make string lowercase 
    let lowercaseContent = content.toLowerCase();

    //replace vowels with nothing ''
    let removedVowels = lowercaseContent.slice(0, 1) + lowercaseContent.slice(1).replace(/[aeiou]/gi, '');

    // not sure if you mean't just first letter, or each first letter so I did both
    return removedVowels.charAt(0).toUpperCase() + removedVowels.slice(1);

    //Or for multiple
    //return removedVowels.split(' ').map(word => word.charAt(0).toUpperCase() + word.slice(1)).join(' ');
}

test = reformat("liMeSHArp DeveLoper TEST");

console.log(test);
```

###### If we type in our console your function and reformat("liMeSHArp DeveLoper TEST") then the result should be Lmshrp dvlpr tst


### Task 3 (optional, for bonus points):
Make this work (without using any built in functions, only a `for` loop, return the next binary number in a string or as an array)
```javascript
next_binary_number([1,0]) // [1,1]

// possible test cases:
// [1,0] => [1,1]
// [1,1] => [1,0,0]
// [1,1,0] => [1,1,1]
// .......
// [1,0,0,0,0,0,0,0,0,1] => [1,0,0,0,0,0,0,0,1,0]
```
Your solution:

```
function next_binary_number(numbers) {

    //loop through from back of numbers
    for (let i = numbers.length-1; i >= 0; i-- ) {

        //check if its 0 or else change it and exit the loop
        if (numbers[i] == 0) {
            numbers[i] = 1;
            break;
        } else {
            numbers[i] = 0;
        }
    }

    //if the first number is a 0 add 1 to the beginning
    if (numbers[0] === 0) {
        numbers.unshift(1);
    }
    return numbers;
}

test = next_binary_number([1,0,0,0,0,0,0,0,0,1]);

console.log(test);
```

###### If we type in our console your function and next_binary_number([1,0,0,0,0,0,0,0,0,1]) then the result should look like 1,0,0,0,0,0,0,0,1,0 (or as an array).

---

If you get invited to the first interview read the "What to expect.md" file.