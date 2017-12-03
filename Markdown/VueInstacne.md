# Vue Instance

<br />

> Vue 생성자로 인스턴스 생성, 화면에서 사용할 옵션 (데이터, 속, 메서드 등등)을 포함하여 화면단위를 생성하는 요소

<br />

```javascript
var vm = new Vue({
    template : template, 
    el: el,               
    method : method,
    created : {
        
    }
}); 
```

# Vue Instance 라이프 사이클 

Vue 객체가 생성될 때 아래의 초기화 작업을 수행

* 데이터 관찰
* 템플릿 컴파일
* DOM에 객체 연결
* 데이터 변경시 DOM 업데이트

<br />

> 초기화 작업 이외에도 개발자가 의도하는 커스텀 로직을 추가할 수 있음


```javascript
var vm = new Vue({
    dta : {
        a: 1
    },
    created : function() {
      //...
    }
})
```


![mvvm](https://github.com/banziha104/Vue.js/blob/master/Markdown/img/component-lifecycle.png)


