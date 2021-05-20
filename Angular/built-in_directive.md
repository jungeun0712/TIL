# NgIf
- 조건의 값에 따라 true이거나 false를 판별하여 결과 표시

```html
<div *ngIf="false"></div> <!-- 표시되지 않음 -->
<div *ngIf="a > b"></div> <!-- a가 b보다 크면 표시 -->
<div *ngIf="str == 'yes'"></div> <!-- str이 "yes"이면 표시 -->
<div *ngIf="myFunc()"></div> <!-- myFunc가 참을 리턴하면 표시 -->
```
# NgSwitch
- 조건에 따라 서로 다른 표시를 해주어야 할 경우

```html
<div class="container" [ngSwitch]="myVar">
    <div *ngSwitchCase="'A'">Var is A</div>
    <div *ngSwitchCase="'B'">Var is B</div>
    <div *ngSwitchDefault>Var is something else</div>
</div>
```

# NgStyle
- html에서 CSS 프로퍼티 설정
- 구조 : [style.cssproperty]="value"

```html
<div [ngStyle]="{color: 'white', 'background-color': 'blue'}">
    Uses fixed white text on blue background
</div>
```

# NgClass
- CSS 클래스를 동적으로 설정하고 변경

```css
.bordered {
    border: 1px dashed black;
    background-color: #eee;
}
```
```html
<div [ngClass]="{bordered: false}">This is never bordered</div>
<div [ngClass]="{bordered: true}">This is always bordered</div>
```

# NgFor
- 반복하여 배열의 값을 전달

```html
this.cities = ['Miami', 'Sao Paulo', 'New York'];

<div *ngFor="let c of cities">
    {{ c }}
</div>
```
- 중첩 배열도 가능
- 인덱스 사용 가능

# NgNonBindable
- 페이지 중 특정 구역을 컴파일하지 않거나 바인딩하지 않을 때 사용

## 참고
- 앵귤러 마스터북