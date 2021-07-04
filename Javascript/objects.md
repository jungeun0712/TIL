# Object
- 설명이 필요한 정보가 담긴 데이터 리스트
- property를 가진 데이터 저장, {}로 표현

```javascript
const player = {
    name : "K",
    points : 10,
    win : true
};

console.log(player); // {name: "K", points: 10, win: true}
```

- const 값을 변경하는건 불가능하지만, object의 property 값을 변경하는건 가능
```javascript
player.win = false;
console.log(player); //{name: "K", points: 10, win: false}
```

- object에 새로운 property 추가
```javascript
player.lastName = "A";
console.log(player); //{name: "K", points: 10, win: true, lastName: "A"}
```