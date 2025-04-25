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
 

```

