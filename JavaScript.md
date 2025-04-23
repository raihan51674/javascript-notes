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
``
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


#### $\textcolor{orange}{ Var\ :\}$
var is function or global scope and is hoisted to the top of its scope.
```js
var x = 10;
if (true) {
    var x = 20;
}
console.log(x); // 20
```
