# 📚 JES-6 Notes (Interview)

## 1.Basic ES6
### 1.let (changing), const(only value change)
```js
//DEfault parameter
function sum(num1=0,num2=0){
  const result=num1 + num2
  return result
}
const data= sum(10)
console.log(data);

//Template string
const Said =`Allah please
help me`
console.log(Said)

//Arrow function
const add=()=>{
  const result =2 + 3
  return result
}
console.log(add());
const squre=x=>x*x
squre(10)
```
### 2.Spread Optional Chaining and Destructure :(arry element exces not arry)
```js
//Spread oparator
const friend=["Raihan","siam","mukit"]
const NewArray=["Torikul", ...friend]
console.log(NewArray);
//Array max identify
const numbers =[1,4,6,78,92,45,234]
console.log(Math.max(...numbers));

//destructure obj and array
const person ={
  name : "hena",
  age :23,
  friends : ["raihan","rifat","siam"],
  status :"Not Found"
}
const {name,status,age,friends}=person
console.log(age,name);
//Array
const friend=["Hero Alom",{name :"raihan"},"hena"]
const [nayok,obj,Name]=friend //must sequenc follow
console.log(nayok);

//Optional Chaining
const person={
  name:"hena",
  age: 34,
  status: "Not Found",
  details:{
    job :"yess",
    name : "mina",
    isValited : true,
  }
}
console.log(person?.details?.job); //or
console.log(person["details"]["job"]); //use 1,true exces

```

### 3.JavaScript Objects and Loop – keys, values, entries, seal, and freeze
```js
//keys,values,entries,seal,freeze
const person={
  name:"hena",
  age: 34,
  status: "Not Found"
}
Object.seal(person) //only change value
Object.freeze(person) //not change
console.log(Object.keys(person));
console.log(Object.values(person));
console.log(Object.entries(person));
//loop throght an object
const person={
  name:"hena",
  age: 34,
  status: "Not Found"
}
for(let key in person){
  console.log(`key : ${key} and values ${person[key]}`);
}

```
## 2.ES-6 Concept :
### 1.Map (not use obj)
```js
const number =[2,3,4,54,23,67,6,5,4,78,89,5]
const mapp=number.map(value=>value+1)
console.log(mapp);
//{} use must be return 
const mapping=number.map((value)=>{
   return value+1
})
console.log(mapping);

const products =[
  {id :1, name: "iphone", color: "black", price:1100},
  {id :2, name: "samsange", color: "gold", price:1500},
  {id :3, name: "iphone", color: "black", price:5000},
  {id :4, name: "Nokia", color: "gold", price:1000},
]
//iphone ber kore 100 taka barai dici
const newProdut=products.map(p=>{
  if(p.name=="iphone"){
    p.price = p.price + 100
  }
  return p
})
console.log(newProdut);
```
### 2. find() and filter() and forEach() fau
```js
//Filter and Find and forEach (not return)
const products =[
  {id :1, name: "iphone", color: "black", price:1100},
  {id :2, name: "samsange", color: "gold", price:1500},
  {id :3, name: "xoami", color: "black", price:5000},
  {id :4, name: "Nokia", color: "gold", price:1000},
]
//not return value fau
products.forEach(product=>{
  if(product.color === "gold"){
    console.log(product);
  }
})
//find out product
const findProduct =products.find(product=>product.id===4)
console.log(findProduct);
//filter category show
const FilterProduct= products.filter(product=>product.price >=1500)
console.log(FilterProduct);

```
### 3.0 Premative (akta, String) and Non Premative(onk,obj)-not compare js
### 3.1 Non-Zero-Value , 0 ,Null, Undefined =>tisu
### 3.2 Truthy(all) and Falsey (0,null,"",undefined,NaN,false) Values
### 3.3 == (value check) and === (data type check)-use
### 3.4 Block Scope and Global Scope and Hoisting(var use exces)
### 3.5 Closure (two function with relation)
### 3.6 CallBack Function (function inside to function call)
### 3.7 Function Arguments and pass by Reference and pss by value
### 3.8 Pre/Post increment and Decrement
```js
//Closure
function sum(){
  let counter =0
  return function (){
    counter ++
    console.log(counter);
  }
}
const result=sum() //new
result()
result()
result()
const result2 =sum() //new
result2()
result2()
result() //again

//callback function
function gotak(patri, name){
  patri(name)
}
const patri=(name)=>{
  console.log(`patri khuje paici josna : ${name}`);
}
const patri2=(name)=>{
  console.log(`patri khuje paici bela sokina : ${name}`);
}
gotak(patri, "masud")
gotak(patri2, "Hero Alom")

//function arguments
function sum(){
  const arry =[...arguments]
  console.log(arry);
}
sum(10,20,30,40)
//pass by value and pass by reference
const person={name:"raihan",age:67}
function sum(obj){
  obj.name ="Hero Alom"
}
console.log(person); //no change name
sum(person)
console.log(person); //change name

//True and false value
const name ="raihan"
if(!name){ //false return
}
if else(!!name) //true return
```
## API and JSON :
### JSON convert:
```js
//JSON
const person={
  name :"raihan",
  age:"30",
  friends:["karim","jarim"],
  status :true
}
//convert json
const ConvertSjon=JSON.stringify(person)
console.log(ConvertSjon);
//convert obj
const ConvertObj=JSON.parse(ConvertSjon)
console.log(ConvertObj);
```

