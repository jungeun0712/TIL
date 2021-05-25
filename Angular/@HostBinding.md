# @HostBinding
- 속성을 호스트 요소에 설정할 수 있다는 뜻이다.
- 호스트란 컴포넌트가 연결된 요소를 가리키는 말이다.

```javascript
@Component({
    selector: 'product-row',
    tempateUrl: './product-row.component.html',
})

export class ProductRowComponent {

@HostBinding('attr.class') cssClass = 'item';

}
```

- CSS 클래스인 item을 호스트 요소(product-row 태그)에 연결한다는 의미

## 참고자료
- 앵귤러 마스터북