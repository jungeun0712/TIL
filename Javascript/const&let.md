# var, let, const 차이점 

- **항상 제일먼저 const, 가끔 필요시 let, var은 사용금지**

/|재선언|재할당
---|---|---|
var|O|O|
let|X|O|
const|X|X|



```javascript
// let 
let a = 5**;
let b = 2;
let myName = "K";

//값을 재할당 가능
a = 10;
myName = "new K";

// const 
const a = 5**;
const b = 2;
const myName = "K";

//값을 재할당 불가능
a = 10; (x)
myName = "new K"; (x)
```

