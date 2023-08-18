# JSLecture
Added the notes for javascript



/* Loops
 1. For loop 
 2. while loop 
 3. do while loop 
 */
// function print(count){
//   do{
//   console.log(count)
//   count++
//   }
//   while(count < 4)
    
//  for (var i= 0;i<15;i++){
//    console.log(count)
//    i = count ++
//  }
// }
// print(6);

// -> Function 
// function print(){
//   console.log("print the name")
// }
// function withParams(one, two){
//   console.log("print", one, two)
// }
// print();
// withParams("five", true);


let a = false   //object (non primitive)
let b = null //string (primitive ) 
// console.log(a==b);
// in case of double equalto if one value is primitive and another is object 
// then it runs the command toPrimitive to convert object to primitive 
// object will be converted to number
// a -> object -> number 
// b -> string -> number 
// a = [5]-> 5 

// Until data type is not same the js conditional operator can't check the value
// if  (a == b){
//   console.log("both are false")
// } else {
//   console.log("value of b is null")
// }
// < -> Array in JS 
// Write a code to check if a number is pallindrome or not

// a =545
// for ( a ==0){
//   b =  b *10 + a%10
//   a = a/10;
// }
// if (a == b){
//   " number is palindrome"
// }
// }

//  let firstVariable = "546"; -> ['5','4', '6']-> ['6','4','5']-> "645"
//  let secondVariable = firstVariable.split('').reverse().join('');
// if(firstVariable == secondVariable){
//   console.log("firstVariable is palindrom")
// }


// 1. To reverse an array -> array.reverse();
// 2. To convert a string to array -> array.split('');
// 3. To sort an array -> array.sort();



// Array in Javascript
// 1. We don't have to define size of an array unlike java.
// let arr = [1,"2",null,true]
// // 2. We don't have type restriction in array. 
// // We have different kind of methods for array.
// console.log(arr.reverse());
// // Sorting in JS array.
// //1. arr.sort()-> it sorts as per string (same as dictionary)
// let stringArray = ["cat", "ball", "ship","mango","kite"]
// console.log(stringArray.sort())
// // In case of number the normal .sort() function also sort it as per string. 
// // so 125 comes  before 15
// let numArray = [23, 15, null,15, 10, 123, 786, 10]
// console.log(numArray.sort())
// // We use compare function to sort as per number

// // sortedArray = numArray.sort((a,b)=> b-a);
// // sortedArray = numArray.sort((a,b) => a-b);
// // sortedArray = numArray.sort((a,b) => (b+a)-(a+b))
// // We can't define time complexity in case JS as it is not assured which method will be used for sorting.
// // How to convert a string into character array.
// let word = "numbebr is greater"
// word.split('')
// split() function breaks the variable into elements and convert it to an array as per the input provided.

// numArray.map(Number).includes(15)
// numArray.map(Number).map(a => a+5)
 let student = {
                "name": "prince",
                "roll": 15,
                "student": true
              }

// Map -> Map works as a for loop and operates the given function on all the elements of an array.
//Filter -> Filter works on an array and provide only those elements which satisfies the given condition
 // numArray.filter(a => a%2 !=0) 
//Reduce -> Reduce operates the operations on all the elements and keep storing them as one element and provides the end product as one element.
// numArray = [23, 15, null,15, 10, 123, 786, 10]
// numArray.map(Number).filter(a=> a%2 ==0).reduce((a,b)=> a+b)
// [23,15,null,15,10,123,786,10] -> [23,15,0,15,10,123,786,10]
// -> [0,10,786,10] -> 806
//       10,796,806

// Javascript is single threaded 
// Java is multithreaded 
//  In js only one statement is executed at a time.
// Hoisting -> 

// 1.var token = 8;
// 2.isEven(token)
// 3.function isEven(number){
// 4.  if (number%2==0){
// 5.    return true;
// 6.  } else {
// 7.   return false;
// 8.  }
// 9.}
// 1. Functional hoisting -> In JS when we run code , then it first copies the code to golobal execution context and while copying the code it replaces all the fuctional code to the top , if it is not present on the top. 
//       That's why order of calling a function does not matters in JS.
// 2. Variable hoisting ->  Whenever a variable is hoisted then it stores the undefined value.
 // it is hoisted when variable is declared using the 'var' keyword in case of 'let' it is not hoisted.
//  console.log(token)
//  let  token = 15;
// console.log(token)
 
// JS Object : 
// -> Objece is a key value pair in JS where key is always unique. 
 
 var students = {
   name: "Mohan",
   rollNo: 14,
   class: 10,
   attendence: 45
 }
 // -> key of an object is always an stringified version. 

var teachers = {
  name: "Manjeet",
  id15: 1342,
  seniority: "mid",
  subject: {
    fifth: "Maths",
    sixth: "Science",
    seventh: "Physics",
    Eigth: "Chemistry",
    ninth: {
      first: "maths",
      second: "science",
      third: "bio"
      }
  },
  homeTution: true,
  visitingFaculty: false,
  attendenceInSem: [50, 60, 75, 89, 98, 85]
}
// console.log(teachers.id15)
// console.log(teachers.subject.ninth.first)
// console.log(teachers.attendenceInSem[1])
// console.log(teachers.subject.ninth.first)
// How to access any value in string.
// 1. using "." operator
// 2. using "[]" operator 

// "." operator

// console.log(teachers.subject.fifth) //-> teachers.name 
// we write the key name after "<object>."  i.e. <objectName>.<key>
// the key name which is coming after "." is automatically regarded as string. 
// let keyVar = "name"
// we can only access the value using "." operator when.
// 1. key is of string type
// 2. key should not be an integer
// 3. key should follow the rules of a variable 
// i.e. key should either start with a character or "_"
// 4. There should not be any special character within e.g. !,@,#,$

// 2. Usage of [] operator
// teachers[keyVar]
// teacher["name"]
// We can access the value of an object using a variable under '[]' operator.
// For accessing value using the normal key we need to add string notation under the [] operator. e.g. teacher["name"]
// For accessing any element array we use [<index>] where [] treats index as the key of an array object.

// let bike = {
//   company: "Honda",
//   model: "activa",
//   engineInCC: 125,
// }

// // We should always add the key using [] operator
// bike.colour = "red" // wrong way of adding key
// bike["milage"]= "30kmpl" // right way of adding key 
// console.log(bike)


// Variable declaration: 
// 1. var 
// 2. let 
// 3. const 

var first = 10;
var second; // undefined 
// -> Scope of var is functional 
// Var is only accessible under a function 
function example(){
  var third = 15;
  console.log(third)
}
// example();
// console.log(third)

//[[varNames]] -> It is a special property of variables declared using the var keyword. It turns the scope of variable to global once it is declared outside a function,

// var keyword can have the duplicate declaration
var first = true
var first = "mohan"


// 2. let -> 
// -> scope of let : Block scope { }
// -> Any variable decalred using let keyword inside a block (i.e. {}) will only be accessible through out that block. 
function summon(){
  let alpha = 5;
  var beta =7;
  {
    let gamma = 15;
    var delta =1
  }
  console.log(alpha+beta+delta);
}
// console.log(alpha-beta);
// summon()

// Hoisting in let 
// Hoisting of variables declared using the let keyword also takes place but JS doesn't assign any value to it(not event undefined like var), which is known as incomplete hoisting.
// For the time interval in which it is incompletely hoisted without the vlue and it's proper value is assigned is known as temporal dead zone(TDZ).
// Until it is inside TDZ it won't be accessible.

// console.log(hi); // TDZ start
let hi = "hi everyone" // TDZ end
// It doesn't have the property of duplicate declaration. (Achhi baat)
// let hi = "true"

// 3. const
// -> Once a value is assigned inside a variable using the "const" declaration , it can't be changed further.

const sigma = "ram dayal"
// sigma = true; //TypeError: Assignment to constant variable.

// -> All of it's other properties are similar to "let".

// -> We keep JS at last while linking it to HTML file , because JS is a very big file and html , css are also synchronous and if we keep at top then it will block rendering. 
// -> "differ" and 'async' are the attributes used to direct html to execute the specific element after rendering. 

// -> Functions
// 1. Normal function
// 2. function expression
// 3. Arrow function
// 4. Higher order functions
// 5. callback function

// Normal function
function print(){
  // function body {}
  console.log("print")
}
// print();

//Function expression
// value()
var value = function printNew/*(Now this name has no value)*/(){
  console.log("printNew")
}
// printNew() 
// value()
// variable hoisting happens in the case of function expression but after seeing the paranthesis "()" it throws error. 
// As a result we can say that function expressions are not hoisted.

// 3. Arrow function (fat arrow function)
// -> normal arrow
// => fat arrow
var printTwo = () => {console.log("two")}
// It is also not hoisted due to same reason.
// arrow function doesn't have it's own name.
// when arrow meter has only one parameter then '()' is not necessary while defining parameter e.g.
// let printThree = text => {console.log(text)}
// printThree("ram")
// But when arrow function has more then one parameter than adding the bracket "()" is mandetory. e.g.
// let printFour = (one,two) => {console.log(one+two)}
// printFour(5,6)
// var arrNew = [5,6,7]
// arrNew.map(element => element+1)
// console.log(arrNew)
// printTwo()

// 4. Higher order function
 
// function multiplyAndReturn(arr){
//   let newArray =[]
//   for(let i =0;i<arr.length;i++){
//     newArray.push(arr[i]*2)
//   }
//   return newArray;
// }
// let arr2=multiplyAndReturn([5,8,9])
// function addAndReturn(arr){
//   let newArray =[]
//   for(let i =0;i<arr.length;i++){
//     newArray.push(arr[i]+2)
//   }
//   return newArray;
// }
// let arr3 = addAndReturn(arr2)
// function subsAndReturn(arr){
//   let newArray =[]
//   for(let i =0;i<arr.length;i++){
//     newArray.push(arr[i]-5)
//   }
//   return newArray;
// }
// subsAndReturn(arr3)

// It is used when we need to copy the same code everytime while writing another new fuction with some minimal changes, we can devide it into two parts.

function operateAndReturn(arr,mathFunction){ // higher order function
  let newArray =[]
  for(let i =0;i<arr.length;i++){
    newArray.push(mathFunction(arr[i]))
  }
  return newArray;
}
// mathfunction
let add = element=> element+2 // callback function
let subs= element => element-2
let multiply = ele=> ele*2
// when a function accepts another function as a parameter then we call the parent function as a higher order function and the child fuction as callback function
// operateAndReturn([5,10,15],subs)
// operateAndReturn([5,10,15],add)
// operateAndReturn([5,10,15],multiply)

// -> We can't call any function without invocation except arrow function. 
// 5. IIFE (immediately invoked function expression)

(function(){
  console.log("iife")
})();

// This function is invoked or called just after declaration and it is an expression hence it is called immediately invoked function expression.
// It is too fast.
// -> Anonymous function : A function without name is called as anonymous function.

// var array = []
// array = ["monah","monika","manisha"]

// array[2]
// //length of an array
// array.length
// // reverse an array
// array.reverse()
// // push an element in array from right
// array.push("muskan")
// // pop an element in array from right
// console.log(array)
// array.pop()
// console.log(array)
// // shift(remove) an element in array from left 
// array.shift()
// // unshift(add) an element in array from left
// array.unshift("minakshi")
// console.log(array)
// // slice any array
// array.slice(0,3)
// // splice any array
// array.splice(0)
// // join any array
// let manu =array.join('')
// console.log(manu)

 // CLOSURE
 
 function returnChild(){
   let garden = "jubilee garden"
   function child(){
     console.log(garden)
   }
   return child;
 }
let newFunction = returnChild();
newFunction()

// whenever a parent function returns a child function then it also returns it's local memory in a bag named as scope with it's child function. So that later if child function will be called then it can use it's parents variable even after the parent's functional execution context is destroyed. This process is called as closure. 

// closure ek aisa punarjanm hai jisme bachche ko apne pichhle janam ki chize yaad rahti hain. 

// Object
// -> key value pair
// -> key should always follow the rule of variable for '.' operator
// -> [] operator can be used to access other key types.
var newObj = {             // singleton method
  "my name": "prince",
  gender: "male",
  age: 15
}
newObj.gender // . operator treats the key as already as string
newObj['my name']  // [] operator ko batana parta hai ki key string hai

// In java -> Object oriented programing oops 
// In javascript -> object linked over object oloo

// officially javascript is named as Ecmascript ES 
// The current most used version of JS is ES 6. 
// The class was introduced in JS after ES 6.

// using the create function

var secondObj = Object.create({})
secondObj.name = "ravi"
secondObj.class = "economy"
secondObj.company = "Vistara"
console.log(secondObj)
// will take one use case of school class where we need to save all the student details with functions to get specific information.
// the basic way is to create a saperate object for each student with it's fuction. 
var aditya = {
  name: "aditya",
  age: "21",
  rollNo: "1",
  branch: "civil",
  batch: 2024,
  getAdmissionYear: function(){
    return aditya.batch-4
  }
}

// this method will be too hectic to record the data for all students
// As we need to create too many objects exclusively (ek ek kar ke)
var chhatra = aditya ;
chhatra.getAdmissionYear()
// The more advanced way is to make a function which will take student information as input and trasform it into object with functions and then return it to us.
function createObject(name, age, rollNo, branch, batch){
  var vidyarthi = Object.create({})
  vidyarthi.name = name;
  vidyarthi.age = age;
  vidyarthi.rollNo = rollNo;
  vidyarthi.branch = branch;
  vidyarthi.batch = batch;
  vidyarthi.getAdmissionYear = function(){
    return vidyarthi.batch - 4
  }
  return vidyarthi
}
// this way is easier then previous use case but still every object will have it's own fuction in memory which will occupy a lot of memory space. 

const aalok = createObject("alok",22,2,"civil",2024)
console.log(aalok)
aalok.getAdmissionYear()

// The more advanced way is to create a object using function but we will attact all the objects to one common function. We will study it in next class. 



































