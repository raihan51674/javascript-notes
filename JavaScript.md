# $\textcolor{yellow}{ JavaScript\ .\}$


# Module-17 Introduction to JavaScript
### 1. JavaScript created by Brendan Eich only 10 Days,High level language,pretty mush everything else
### 2.Variable,error(undefined,NaN,null,)  special type:conveter { parseInt(x),parseFloat(x) , Number(x)} and { total.toFixed(2) }
### 3.Methmathical operation (+,-,*,/,%) and (+=,-=, *=)

# Module-18 Concept of Conditions :

### 1.Comparisom : { <,>,>=,<=,==,===,!=,&&(all),||(single), }
### 2.Condition-2 :(if,if else,else)
#### simple
```js 
const salary = 5000;
const paroBCS =true;
const height = 68;
if((salary>=4000 && paroBCS==true) || height>=96){
  console.log("Ami biyer jonno raji");
}else if(salary>=6000 && height>=66){
  console.log("patro chole kono rokom");
}else if(salary>=4000 || paroBCS==true){
  console.log("sure nah"); 
}else{
  console.log("default"); 
}
```
#### mid
```js
const price =3000;
if(price>=5000){
  const discount = price *10/100;
  const payAmount =price-discount
  console.log(payAmount);
}else if(price<=5000){
  const discount =price*5/100;
  const payAmount =price-discount;
  console.log(payAmount);
}else{
  console.log(price); 
}
```
### 3. Ternary Operator: (condition ? do something when true : do something false;
#### if(!isLeader) //false return
```js
 let price = 500;
const isLeader = false;
if(isLeader===true){
  price =0;
}else{ 
    price = price+100
  }
console.log(price);
//ternary
isLeader==true ? 0 : console.log(price+100);
```
 ## Module -18.5 Concept of Array
 ### 1.Array  {kind of tool box differnt type element store}
 #### * arry.length , arry.includes(4) ,arry.indexOf(4) ,arry.join("|"), arry.concat(arry1) , arry.slice(2,4), arry.splice(5,2) 
 ```js

  const arry = [2,3,5,1,6,7,4,2]
const arry1 = [2,3,5,1,6,7,4,2]
console.log(arry.length);
console.log(arry.includes(4)); //array search return true or false
console.log(arry.indexOf(4)); // get this value
console.log(arry.join("|")); //each element add this symbol
console.log(arry.concat(arry1)); //two array element add new total arry 
console.log(arry.slice(2,6)); //index 2 to 6 all element cut
console.log(arry.splice(4,2)); // 4 index to how much remove element(2)

 ```


## Module -19 Concept of loop :
### 1.for of
```js
const numbers = [2,3,5,1,6,7,4,2]
for(const num of numbers){
  let  num1 = num + 3
  console.log(num1); 
}
//
for(let i=0; i<=10; i++){
  console.log(i); 
}
```
### 2.while
```js
let num =1
while(num<=10){
  console.log("invest 6 day per single day");
  num++
}
```
### 3. Break(done this loop) and Continue(skip rest of the code for this iteration)
```js
for(let i=0; i<20; i++){
  console.log(i);
  if(i>=10){
    break
  }
}
//
for(let i=1; i<10; i++){
  if(i%2 == 1){
   continue;
  }
  console.log(i);
}

```
## Module-20 String & Objects :

### 1.String Compare : school.toLowerCase() , toUpperCase() , trim() and split(' ,') , reverse() , join("@")
```js
const drink ="this water";
 const liquid ="  this water"
 if(drink=== liquid.trim()){
  console.log("milce");
 }else{
  console.log("mele nai");
 }
```
### 2. Object : student explain,
```js
const person ={
  profession : "Developer",
  salary : 2500,
  maried : false,
  places : ["cox","sajek","radison"],
  unique :{
    color : "blue",
    result :{
      gpa : 5,
    }
  }
}
person.salary = 3000; //update
delete person.maried; //delete
console.log(person["places"]);
console.log(person.places[2]);
console.log(person.unique.color);
console.log(person.unique.result.gpa);
console.log(Object.keys(person)); //show porparty
console.log(Object.values(person)); //all value 
for(const prop in person){ //for in use only object
  console.log(prop); //show key
  console.log(person[prop]); //show value
}
```






















 

#### $\textcolor{orange}{ Var\ :\}$
var is function or global scope and is hoisted to the top of its scope.
```js
var x = 10;
if (true) {
    var x = 20;
}
console.log(x); // 20
```
