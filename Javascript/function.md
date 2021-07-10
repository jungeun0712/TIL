# function
- 계속 반복해서 사용할 수 있는 코드 조각

```javascript
//ex1)
function sayHello(name, age) {
    console.log("Hello my name is " + name + " and I'm " + age);
}

sayHello("A", 1);
sayHello("B", 2);
sayHello("C", 3);
```

```javascript
//ex2)
function plus(a, b) {
    console.log(a + b);
}

plus(8, 60);
```

```javascript
//ex3)
const player = {
    name : "K",
    sayHello: function(name){
        console.log("hello! " + name);
    }
}

player.sayHello("S");
```

- 계산기 예제
```javascript
// object와 console 사용
const calculator = {
    add : function (a, b) {
        console.log(a + b);
    },
    minus : function (a, b) {
        console.log(a - b);
    },
    div : function (a, b) {
        console.log(a / b);
    },
    powerof : function (a, b) {
        console.log(a ** b);
    }
}

calculator.add(1, 2);
calculator.minus(1, 2);
calculator.div(1, 2);
calculator.powerof(1, 2);

// return 사용
// return을 하면 function은 작동을 멈추고 결과 값을 return하고 끝남.
const calculator = {
    add : function (a, b) {
        return a + b;
        console.log("hello"); // return 종료때문에 console.log는 나오지 않음.
    },
    minus : function (a, b) {
        return a - b;
    },
    div : function (a, b) {
        return a / b;
    },
    powerof : function (a, b) {
        return a ** b;
    }
}

const addResult = calculator.add(2, 3);
const minusResult = calculator.minus(addResult, 3);
const divResult = calculator.div(minusResult, addResult);
const powerofResult = calculator.powerof(divResult, minusResult);
```