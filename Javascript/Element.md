# Element
- getElementsByClassName() : 많은 element을 가져올때 (array 형식으로 보여줌)

```javascript
<div class="hello">
    <h1>hi!</h1>
</div>
<div class="hello">
    <h1>hi!</h1>
</div>
<div class="hello">
    <h1>hi!</h1>
</div>

const hellos = document.getElementsByClassName("hello");
console.log(hellos);
// HTMLCollection(3) [div.hello, div.hello, div.hello]
```

- getElementsByTagName() : 태그 이름으로 가져올때

```javascript
<div class="hello">
    <h1>hi!</h1>
</div>

const hello = document.getElementsByTagName("h1");
console.log(hello);
// HTMLCollection [h1]
```

- querySelector() : selector 안의 조건에 맞는것들 중에 단 한개의 첫번째 element만 가져옴.

```javascript
<div class="hello">
    <h1>hi!</h1>
</div>
<div class="hello">
    <h1>hi!</h1>
</div>
<div class="hello">
    <h1>hi!</h1>
</div>

const hello = document.querySelector(".hello h1");
console.log(hello);
// <h1>hi!</h1>
```

- querySelectorAll() : selector 안의 조건에 부합하는 모든 element을 가져옴.

```javascript
<div class="hello">
    <h1>hi!</h1>
</div>
<div class="hello">
    <h1>hi!</h1>
</div>
<div class="hello">
    <h1>hi!</h1>
</div>

const hello = document.querySelectorAll(".hello h1");
console.log(hello);
// NodeList(3) [h1, h1, h1]
```

- querySelector("#hello")와 getElementById("hello")는 같다.

```javascript
<div id="hello">
    <h1 id="hi">hi!</h1>
</div>

const hello = document.querySelector("#hi");
console.log(hello);
// <h1 id="hi">hi!</h1>
```