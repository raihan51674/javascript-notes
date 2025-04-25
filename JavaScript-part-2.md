# Dom

## 1.Traversing dom
### getElementById("") use for only one element and getElementsByClassName("") for many
```js
const HtmlData = document.getElementsByTagName("li"); //child use,all excecs 
for(const li of HtmlData){
  if(li.innerText === "1.Raihan"){
    console.log(li.innerText);
  }
}
const Select = document.getElementById('section') //parent use,not working loop
console.log(Select); 

const dhor = document.getElementsByClassName("classUse") //child use
for(const item of dhor){
  console.log(item.innerText);
}
const TextChange = document.getElementById("title")
 const data = TextChange.innerText ="This a Big Data Information"
 console.log(data);
 
//id use # and class use .
const somelist =document.querySelectorAll("#section")
for(const li of somelist){
  console.log(li.innerText);
}
```
### style and element add :
```js
// 1.where to add
const placeList =document.getElementById("places-list")
//2.what to be add
const li = document.createElement("li")
li.innerHTML = `<h1>Akta new li added</h1>`
//3 .add the child
placeList.appendChild(li)

const styleAdd = document.getElementsByClassName("classUse")
for (const li of styleAdd) {
  li.style.backgroundColor = "red";
  li.style.padding = "10px"
  li.style.border ="2px solid steelblue"
}
console.log(styleAdd);
```

## Bom :

