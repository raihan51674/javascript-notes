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
### 2.Spread Operator and Destructure :(arry element exces not arry)
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
