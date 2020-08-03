# what-i-learned-week11

### **__dirname**  
- directory 
- the path name for whatever directory we're currently in
- dynamic and decided when the file is run
- present location of file in directory
```javascript
const file = fs.readFileSync(__dirname + '../backend/todos.json', 'utf-8')
```
<hr>
<hr>

### JSON.parse()

Examples
Using JSON.parse()
```javascript
JSON.parse('{}');              // {}
JSON.parse('true');            // true
JSON.parse('"foo"');           // "foo"
JSON.parse('[1, 5, "false"]'); // [1, 5, "false"]
JSON.parse('null');            // null
```
<hr>

## METHODS
- functions used as properties of an object.
- functions assigned to a property as an object.
```javascript
const doggo = {
    name: 'Ralph',
    ageInHumanYears: 4,
    likes :  ['catch', 'squirrels'],

    bark: function(isLoud){
      console.log('woof')
}    

doggo.name;              // Ralph
doggo.ageInHumanYears;   // 4
doggo.likes;             // ['catch', 'squirrels']
doggo.bark();            // woof
```
<hr>


## this
- think of it as my property
- pertains to the current object that the function lays in.

EXAMPLE using ' this ':

```javascript
const doggo2 = {
    name: 'Oscar',
    ageInHumanYears: 5,
    likes :  ['tug of war', 'squirrels'],
    isLoud : false,

    bark: function(){
        if(this.isLoud){
            return 'WOOF'
        }
        return 'Woof';
    },

    speak: function() {
        // return 'hi! My name is ' + this.name + " I'm " + this.ageInHumanYears + '.'
        return `hi! My name is ${this.name} I'm ${this.ageInHumanYears}.`
    }
}    
console.log(doggo2.speak())     // hi! My name is Oscar I'm 5.
```
<hr>


## Making a BLUEPRINT for an OBJECT.
## (There's an App for that!)

- making a template.
- pre - building an object in order to just insert the characters that we need filled as values.
- design a schema/ blueprint of how this thing looks.
- object oreinted programming.
  
  **FACTORY FUNCTION**
- a function that spits out functions



<hr>
## METHODS INTRODUCED

### unshift()

- The unshift() method adds one or more elements to the beginning of an array and returns the new length of the array.

**Examples**
**Using unshift**

```javascript
let arr = [1, 2]

arr.unshift(0)               // result of the call is 3, which is the new array length
// arr is [0, 1, 2]

arr.unshift(-2, -1)          // the new array length is 5
// arr is [-2, -1, 0, 1, 2]

arr.unshift([-4, -3])        // the new array length is 6
// arr is [[-4, -3], -2, -1, 0, 1, 2]

arr.unshift([-7, -6], [-5])  // the new array length is 8
// arr is [ [-7, -6], [-5], [-4, -3], -2, -1, 0, 1, 2 ]
```

## Object.keys()
- gives all the keys in an object



## foreach()
- runs that function on every element of the array.
- for each character, run the function
- helper function
- takes in a callback
- take that call back on evvery single element
- 
<hr>

## .filter()
- don't change anything.
- if it passes the test, push it in.
- The filter() method creates a new array with all elements that pass.
the test implemented by the provided function.
- if we run the function on the element and its true. return the element
- give me only the certain ones.
<hr>


-Array.prototype 


## .map()
- push it in changed, whether it's true or not 

```javascript
const map = function (arr, func) {
    const newArr = [];
    for (const element of arr) {
        const transformedElement = func(element):
        newArr.push(transformedElement);
    }
    return newArr;
}
```
<hr>