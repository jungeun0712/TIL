# @Input
- 부모컴퍼넌트 => 자식컴퍼넌트로 상태전달하기

```javascript
//부모컴포넌트
import {component} from '@angular/core';

@Component({
    selector : 'app-root',
    tamplate : `<app-son [title]="title"></app-son>`,
})

export class AppComponent {
    title = 'app';
}
```

```javascript
//자식컴포넌트
import {component, OnInit, Input} from '@angular/core';

@Component({
    selector : 'app-son',
    template : `<p> son works! {{title}} </p>`,
})

export class SonComponent {
    @Input() title: string;
}
```

- 부모 컴포넌트에서는 [@input 속성] = "속성값"을 이용해 값 할당
- 자식 컴포넌트에서는 클래스에서 @Input 속성;을 이용해 값 받기


# @Output
- 자식컴포넌트 => 부모컴포넌트로 상태전달하기

```javascript
//부모컴포넌트
import {component} from '@angular/core';

@Component({
    selector : 'app-root',
    tamplate : `<app-son [title]="title" (addContent)="addItem($event)"><app-son>`,
})

export class AppComponent {
    title = 'app';
    addItem(event) {
        this.title = event;
    }
}
```
```javascript
//자식컴포넌트
import {component, OnInit, Input} from '@angular/core';

@Component({
    selector : 'app-son',
    template : `<h1>{{title}}</h1>
                <button (click)="addContent.emit(content)">클릭</button>`,
})

export class SonComponent {
    content = "hello";
    @Input() title: string;
    @Output() addContent = new EventEmitter();
}
```

- 값이 전달될 때까지 기다리는 것이 아니라, 이벤트가 일어나 값이 전달되면 그때 그에 맞는 일을 처리
- 이벤트 일으키기 위해 EventEmitter 사용
